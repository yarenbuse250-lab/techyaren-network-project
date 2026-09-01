# Week 2 Summary — Security Hardening

## Objectives

* Secure device passwords using encryption
* Enable **SSH** for secure remote management
* Configure **Port Security** to prevent unauthorized devices from accessing the network
* Isolate the **Guest VLAN** from internal networks using **ACLs**
* Configure a warning banner for unauthorized access

## Completed Tasks

1. **Password Encryption:** Enabled `service password-encryption` and configured `enable secret` on both the router and switch.

2. **SSH Configuration:** Generated an RSA key pair, created a local administrator account, and restricted the VTY lines to **SSH-only**, disabling Telnet access.

3. **Port Security:** Configured sticky MAC address learning with a maximum of **1 MAC address per access port**. The violation mode was set to `restrict`.

4. **Guest VLAN ACL:** Created an extended ACL named `GUEST_RESTRICTION` to prevent traffic from **Guest VLAN 99** from reaching internal networks while allowing outbound Internet traffic.

5. **Security Banner:** Configured a warning banner to notify users about unauthorized access.

## Issues Encountered & Resolutions

### 1. SSH Connection Failure

The initial SSH connection failed because `ssh -1 admin` (number **1**) was entered instead of `ssh -l admin` (lowercase **L**). The command was corrected, and the SSH connection was successfully established.

### 2. ACL Blocking DHCP

After applying the Guest VLAN ACL, **Guest_PC** was unable to obtain a DHCP lease and automatically assigned itself an APIPA address.

The issue occurred because DHCP Discover packets are sourced from `0.0.0.0` and did not match the existing permit rules, causing them to be blocked by the implicit deny rule.

**Resolution:** An explicit DHCP permit rule was added as the first line of the ACL:

`permit udp any eq bootpc any eq bootps`

After this change, Guest_PC was able to obtain a DHCP address successfully.

### 3. Interpreting ACL Test Results

When Guest_PC attempted to ping an internal server, the result was **`Destination host unreachable`** instead of a timeout.

This confirmed that the router was actively rejecting the packet according to the configured ACL, indicating that the Guest VLAN restriction was functioning as intended.

## Verification

* `show port-security` confirmed that all **6 access ports** had Port Security enabled with a maximum of **1 MAC address** per port.
* `show access-lists` displayed non-zero match counters for both the DHCP permit rule and the internal-network deny rule.
* **Guest_PC** was unable to access internal VLANs (**10, 20, 30, 40, and 50**) while maintaining DHCP and general Internet access.
* Other departments (**IT, HR, Accounting, and Sales**) retained access to the server, confirming that the ACL only restricted Guest VLAN traffic.
* All relevant command outputs and connectivity tests are available in the `/screenshots` directory.

## Key Takeaways

* Gained practical experience with Cisco network security configuration
* Learned how to configure and verify **SSH, Port Security, and ACLs**
* Improved troubleshooting skills by analyzing DHCP and ACL-related connectivity issues
* Learned how to verify security configurations using Cisco IOS commands
