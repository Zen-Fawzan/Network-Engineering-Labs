documentation 

# Enterprise Network Design & Security Lab

An intermediate enterprise network lab built with Cisco Packet Tracer to practice network engineering, VLAN segmentation, inter-VLAN routing, and network access control.

## Technologies & Features

- VLAN segmentation for Administration, Sales, IT, Servers, DMZ, and Management
    
- Inter-VLAN routing using router subinterfaces (Router-on-a-Stick)
    
- DHCP for client addressing
    
- Access Control Lists (ACLs) for traffic filtering
    
- Dedicated management VLAN for network devices
    
- DMZ web server for externally accessible services
    
- Switch management using SSH
    

## Network Topology

See `topology.png`.

## Files

- `Enterprise-Network.pkt` — Packet Tracer project
    
- `topology.png` — Network topology diagram
    
- `addressing-vlans.md` — VLAN and IP addressing plan
    

## Validation Tests

The network should be tested for:

- DHCP address assignment
    
- Inter-VLAN connectivity
    
- Access restrictions between user VLANs and the management VLAN
    
- SSH access from the authorized IT subnet
    
- HTTP/HTTPS access to the DMZ server
    
- Restrictions on unauthorized traffic
    

Test results should reflect actual observed behavior in Packet Tracer.

## Purpose

Hands-on practice in enterprise network design, troubleshooting, segmentation, and access control.