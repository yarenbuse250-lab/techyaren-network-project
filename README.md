# TechYaren Corporate Network Project

A 4-week enterprise network simulation project built in Cisco Packet Tracer, covering VLAN segmentation, security hardening, multi-site connectivity, internet access, and IPv6 dual-stack migration.

## Project Overview

This project simulates a single-headquarters company (TechYaren) expanding to a branch office with full internet connectivity, built incrementally over 4 weeks.

**Topology includes:**
- HQ Router (Cisco 2901) with router-on-a-stick configuration
- HQ Switch (Cisco 2960) with 6 VLANs
- Branch Office (separate router, switch, 2 PCs) connected via WAN
- ISP Router simulating internet connectivity
- HQ Local Server (DNS + HTTP)

## Weekly Breakdown

| Week | Topic | Status |
|------|-------|--------|
| [Week 1](./Week1_VLAN_DHCP) | VLAN Segmentation, Trunking, DHCP | ✅ Complete |
| [Week 2](./Week2_Security) | Port Security, Encryption, SSH, ACLs | ✅ Complete |
| [Week 3](./Week3_Branch_DNS_NAT) | Branch Office, OSPF, DNS, Web Server, NAT/PAT | ✅ Complete |
| [Week 4](./Week4_IPv6) | IPv6 Dual-Stack Migration | ⏳ In Progress |

## IP Addressing Plan

| VLAN/Network | Subnet | Gateway |
|---|---|---|
| IT_Management (VLAN 10) | 192.168.10.0/28 | .1 |
| Human_Resources (VLAN 20) | 192.168.20.0/27 | .1 |
| Accounting_Finance (VLAN 30) | 192.168.30.0/27 | .1 |
| Sales_Marketing (VLAN 40) | 192.168.40.0/27 | .1 |
| Server_Farm (VLAN 50) | 192.168.50.0/28 | .1 |
| Guest_WiFi (VLAN 99) | 192.168.99.0/26 | .1 |
| Branch LAN | 192.168.100.0/24 | .1 |
| HQ-Branch WAN | 10.0.0.0/30 | — |
| HQ-ISP Link | 203.0.113.0/30 | — |

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI

## Author
Yaren Buse Akdoğan — Internship Project, 2026
