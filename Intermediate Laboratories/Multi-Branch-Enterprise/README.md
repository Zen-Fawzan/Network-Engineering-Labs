# CCNA 200-301 Enterprise Network Project

**Project by Zen**  
**Platform:** Cisco Packet Tracer

## Overview

This project designs and implements an enterprise network with a headquarters (HQ) and two branches. It combines VLAN segmentation, Layer 3 switching, dynamic routing, network services, access control, and Layer 2 security.

## Network Features

- HQ VLAN segmentation for HR, IT, and Management
- Inter-VLAN routing on the HQ multilayer switch (MLS)
- EtherChannel between HQ access switches
- OSPF multi-area routing and EIGRP
- OSPF/EIGRP route redistribution
- Administrative Distance tuning for route preference
- DHCP service and DHCP relay
- DNS and web services
- NAT overload for Internet access
- Standard and extended ACLs to enforce traffic policies
- SSH/Telnet remote management as required by the project
- Port Security, PortFast, BPDU Guard, and Root Guard
- IPv4 addressing and a limited IPv6 deployment
- Verification and troubleshooting with Cisco IOS show commands, ping, and traceroute

## Topology

See [`topology.png`](topology.png) for the network diagram, if included in this repository.

## Addressing Plan

See [`ip-address-map.md`](ip-address-map.md) for the IPv4 subnet plan, gateway convention, WAN subnet ranges, and IPv6 link address.

**Gateway convention:** The last usable IPv4 address in each LAN subnet is used as its default gateway. For example, `192.168.10.0/26` uses `192.168.10.62`; the broadcast address is `.63`.

## Device Inventory

- **Routers (6):** R1 (HQ Core), R2, R3, R4 (Core Interconnect), R5, R6 (Server Farm)
- **Switches:** SW1, SW2, SW-BA1, SW-BB1
- **Multilayer switch:** HQ MLS
- **End devices:** Approximately 15 PCs and 3 servers (DNS, DHCP, Web)

## Security Goals

- Prevent HR from accessing the Management VLAN.
- Restrict server-farm access to the authorized IT network where required.
- Apply ACLs in the appropriate direction and document them with remarks.
- Secure switch access ports with Port Security.
- Enable BPDU Guard on edge/access ports and Root Guard on appropriate distribution-facing ports.
- Use SSH for secure remote management wherever supported and required.

## Validation Checklist

Use these checks in Packet Tracer and report only results you have personally verified:

- [ ] End devices receive the expected DHCP settings.
- [ ] Devices can reach their configured default gateways.
- [ ] Required inter-VLAN communication succeeds.
- [ ] HR-to-Management traffic is blocked by the intended ACL.
- [ ] OSPF neighbors form on the intended links and routes are learned.
- [ ] EIGRP neighbors form on the intended links and routes are learned.
- [ ] Required routes are exchanged across the OSPF/EIGRP boundary.
- [ ] NAT overload provides the intended translated traffic.
- [ ] DNS and web services work from authorized networks.
- [ ] Unauthorized access to protected server or management subnets is blocked.
- [ ] SSH management access works from authorized devices.
- [ ] Port Security, PortFast, BPDU Guard, and Root Guard are configured as intended.
- [ ] IPv6 connectivity works across the configured R1–R4 link.

## Files

- `Enterprise-Network.pkt` — Packet Tracer project file
- `README.md` — Project overview and validation checklist
- `ip-address-map.md` — Subnets, gateway convention, WAN ranges, and IPv6 details
- `topology.png` — Optional topology screenshot

## Notes

The WAN subnets are documented as provided in the project scenario; this document does not assign individual WAN subnets to specific router interfaces. Server IPs in the addressing map are suggested examples if the actual Packet Tracer addresses differ.
