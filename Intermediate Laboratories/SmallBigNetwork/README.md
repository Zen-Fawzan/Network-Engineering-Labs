# CCNA Routing & Switching Lab

An enterprise-style networking lab built with Cisco Packet Tracer to practice essential CCNA routing, switching, network security, and troubleshooting skills.

## Technologies & Skills

- **VLANs & Trunking** — Network segmentation and VLAN transport between switches
- **Router-on-a-Stick** — Inter-VLAN routing using router subinterfaces
- **IP Addressing & Subnetting** — IPv4 addressing, subnet masks, and gateway configuration
- **DHCP** — Automatic IP address assignment for end devices
- **Routing** — Default gateways, router-to-router connectivity, and OSPF
- **Switch Security** — SSH management, basic switch hardening, and unused-port shutdown
- **Layer 2 Protection** — PortFast and BPDU Guard
- **Troubleshooting** — Ping, traceroute, and Cisco IOS show commands

## Objectives

- Configure VLANs and trunk links between switches.
- Enable communication between VLANs through Router-on-a-Stick.
- Configure addressing and DHCP for end devices.
- Establish routing between routers using OSPF.
- Secure network device management using SSH and basic switch security measures.
- Reduce Layer 2 risks by configuring PortFast, BPDU Guard, and shutting down unused ports.
- Diagnose connectivity problems using verification commands and systematic troubleshooting.

## Verification & Testing

The lab should be validated through practical tests, including:

- Correct VLAN membership and trunk operation
- Successful DHCP address assignment
- Successful inter-VLAN connectivity where permitted
- Router-to-router connectivity and OSPF neighbor establishment
- Reachability of remote networks through OSPF
- SSH access to network devices
- Verification of PortFast, BPDU Guard, and unused-port shutdown
- Troubleshooting using `show ip interface brief`, `show vlan brief`, `show interfaces trunk`, `show ip route`, and `show ip ospf neighbor`

## Tools

- Cisco Packet Tracer
- Cisco IOS command-line interface

## Purpose

This project demonstrates hands-on practice with foundational enterprise networking, routing and switching, device hardening, and network troubleshooting as part of CCNA preparation.
