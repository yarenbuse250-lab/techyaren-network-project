# Week 1 Summary — Basic Network Infrastructure

## Completed Tasks

* Created 6 VLANs: **IT, HR, Accounting, Sales, Server Farm, and Guest**
* Configured **access ports** on the switch and an **802.1Q trunk link** between the switch and the router
* Implemented **Router-on-a-Stick**, configuring a separate sub-interface and default gateway for each VLAN
* Configured **centralized DHCP**, with a separate and clearly named DHCP pool for each VLAN
* The **Server Farm VLAN** was configured with static IP addresses instead of DHCP

## Issues Encountered

* The cables connecting **GUEST_PC** and **HQ_Local_Server** to the switch appeared to be connected visually, but the interfaces showed **`notconnect`**, indicating that no physical link was established.
* The issue was resolved by deleting and reconnecting the cables.
* We learned to verify the actual interface status using the **`show interfaces status`** command instead of relying only on the visual connection status in Packet Tracer.

## Key Takeaways

* Gained hands-on experience with VLAN configuration and segmentation
* Learned how to configure Router-on-a-Stick and inter-VLAN gateways
* Practiced centralized DHCP configuration for multiple VLANs
* Learned how to troubleshoot physical connectivity issues in Cisco Packet Tracer
