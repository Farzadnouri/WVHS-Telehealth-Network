# Western Victoria Regional Telehealth Network

Computer Networks, Victoria University (2026).

## Overview
Design and simulation of a regional telehealth network connecting three medical 
facilities across Western Victoria:
- **Ballarat** — Central Diagnostic Hub (16 devices, 4 departments)
- **Ararat** — Medical Clinic (7 devices)
- **Horsham** — Medical Clinic (9 devices)

## Network Design
- **Topology:** Full mesh WAN with serial links (WIC-2T modules)
- **Addressing:** VLSM applied to 10.7.6.0/24 base network (11 subnets)
- **Routing:** OSPF Area 0 across all 3 routers (4/4 ping success on all paths)
- **LAN:** Router-on-a-Stick inter-VLAN routing with 802.1Q on Cisco 2911 routers
- **Switching:** 9x Cisco 2960 switches with trunk/access port configuration
- **Security:** Enable secret (MD5), SSH, console passwords, VLAN segmentation

## Key Technical Challenges Solved
1. Subnet boundary misalignment — Horsham Clinical redesigned to 10.7.6.144/28
2. WAN link failure — resolved by switching to WIC-2T serial modules
3. WAN subnet overlap — resolved by selecting non-overlapping 10.7.6.140/30 block

## Tools
- Cisco Packet Tracer

## Role
Farzad Nouri — Full implementation, troubleshooting, report & presentation
