# Week 3: Branch Office, Routing and Network Services

**Project:** TechYaren Solutions – Enterprise Network Infrastructure  
**Environment:** Cisco Packet Tracer  
**Week:** 3

## Overview

This phase extends the existing headquarters network by introducing a branch office and integrating routing and network services. The objective is to establish communication between the headquarters and branch office while enabling internal DNS resolution and web server access.

All configurations are implemented in a simulated environment for educational purposes.

## Objectives

- Extend the network topology with a branch office.
- Establish routing between headquarters and the branch office using OSPF.
- Configure DNS resolution for the internal web server.
- Deploy an internal web service.
- Configure NAT/PAT for network address translation.
- Verify connectivity and service accessibility through testing.

## Network Components

- **Headquarters:** Existing HQ router and switch infrastructure.
- **Branch Office:** Branch router, branch switch, and end devices.
- **Routing Protocol:** Open Shortest Path First (OSPF).
- **Network Services:** DNS and HTTP.
- **Address Translation:** NAT/PAT.

## Implementation

### 1. Branch Office Connectivity

The branch office network is connected to the headquarters through a WAN link. The router and end-device configurations provide the foundation for inter-site communication.

### 2. OSPF Routing

OSPF is used to exchange routing information between the headquarters and branch office. Routing tables and neighbor relationships are checked to verify the routing configuration.

### 3. DNS and Web Server

An internal DNS service is configured to resolve the hostname `www.techyaren.local` to the web server's IP address. The web server hosts an internal portal that can be accessed by authorized devices within the simulated network.

### 4. NAT/PAT

NAT/PAT is configured to demonstrate address translation for internal network traffic. Where implemented, static port forwarding allows HTTP traffic to reach the internal web server through the designated public-facing address.

## Verification and Testing

The following checks are used to validate the implementation, where applicable:

- `show ip ospf neighbor` — verify OSPF neighbor relationships.
- `show ip route` — inspect learned and connected routes.
- `show ip nat translations` — inspect NAT translations.
- `ping` — test connectivity between network devices.
- `nslookup` — verify DNS name resolution.
- Web browser testing — verify access to the internal portal.

Screenshots and device configuration files are organized in the corresponding folders.

## Repository Contents

- `TechYaren_Week3.pkt` — Cisco Packet Tracer project file.
- `screenshots/` — Network configuration and verification screenshots.
- `configs/` — Router and switch configuration files.

## Troubleshooting

During implementation, connectivity, routing, DNS resolution, and address translation are checked systematically. Any issues encountered are documented alongside the relevant verification results.

## Project Scope

This project is an educational network simulation based on the fictional company TechYaren Solutions. It does not represent a production network or disclose real organizational network configurations.
