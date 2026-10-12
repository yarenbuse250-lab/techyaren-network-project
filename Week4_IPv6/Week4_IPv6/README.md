# Week 4: IPv6 Dual-Stack Migration

**Project:** TechYaren Solutions – Enterprise Network Infrastructure  
**Environment:** Cisco Packet Tracer  
**Week:** 4  
**Status:** In Progress

## Overview

This phase focuses on introducing IPv6 into the existing enterprise network while maintaining IPv4 connectivity. The dual-stack approach allows network devices to operate with both IPv4 and IPv6 during the transition.

## Objectives

- Introduce IPv6 addressing into the existing network topology.
- Configure IPv6 addresses on the relevant routers, switches, and end devices.
- Enable IPv6 routing where required.
- Maintain existing IPv4 functionality.
- Verify connectivity using IPv4 and IPv6 testing tools.

## Implementation

### 1. IPv6 Addressing

IPv6 address assignments are planned for the relevant network segments and interfaces. Addressing is documented to support consistent configuration and troubleshooting.

### 2. Dual-Stack Configuration

IPv4 and IPv6 are configured to coexist on supported network devices. Existing IPv4 services are retained while IPv6 connectivity is introduced.

### 3. Routing and Connectivity

IPv6 routing is enabled where required by the topology. Interface status, routing information, and end-to-end connectivity are checked during implementation.

## Verification and Testing

The following commands can be used where applicable:

- `show ipv6 interface brief` — inspect IPv6 interface addresses and status.
- `show ipv6 route` — inspect the IPv6 routing table.
- `ping` — test IPv4 connectivity.
- `ping ipv6-address` — test IPv6 connectivity where supported by the device CLI.

Screenshots and configuration files will be added as implementation and verification progress.

## Repository Contents

- `TechYaren_Week4.pkt` — Cisco Packet Tracer project file.
- `screenshots/` — Configuration and verification screenshots.
- `configs/` — Relevant device configuration files.

## Project Scope

This project is an educational simulation using the fictional company TechYaren Solutions. It does not represent a production network.

