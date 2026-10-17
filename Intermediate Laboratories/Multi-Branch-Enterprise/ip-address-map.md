# IP Address Map

**Project:** CCNA 200-301 Enterprise Network Project  
**Author:** Zen  
**Platform:** Cisco Packet Tracer

## Addressing Convention

- IPv4 gateways use the **last usable address** in each LAN subnet.
- Network and broadcast addresses are not assigned to hosts.
- WAN subnet ranges are listed without assigning each subnet to a specific router interface, as the interface-to-link mapping is maintained in the Packet Tracer topology.
- Server addresses below are suggested examples; replace them if the actual `.pkt` file uses different addresses.

## HQ LANs

| Segment | VLAN | Network / Prefix | Usable host range | Default gateway |
|---|---:|---|---|---|
| HR | 10 | `192.168.10.0/26` | `192.168.10.1–192.168.10.62` | `192.168.10.62` |
| IT | 20 | `192.168.20.0/25` | `192.168.20.1–192.168.20.126` | `192.168.20.126` |
| Management | 30 | `192.168.30.0/28` | `192.168.30.1–192.168.30.14` | `192.168.30.14` |

**HQ interconnect:**

| Link | Network / Prefix | Usable addresses |
|---|---|---|
| HQ Core Router (R1) – MLS | `192.168.99.0/30` | `192.168.99.1–192.168.99.2` |

The exact `.1`/`.2` endpoint assignment on the R1–MLS link should match the configured interfaces in Packet Tracer.

## Branch A LAN

| Segment | Network / Prefix | Usable host range | Default gateway |
|---|---|---|---|
| Branch A LAN | `172.16.1.0/26` | `172.16.1.1–172.16.1.62` | `172.16.1.62` |

## Branch B LANs

| Segment | Network / Prefix | Usable host range | Default gateway |
|---|---|---|---|
| Branch B LAN 1 | `10.10.1.0/27` | `10.10.1.1–10.10.1.30` | `10.10.1.30` |
| Branch B LAN 2 | `10.10.2.0/26` | `10.10.2.1–10.10.2.62` | `10.10.2.62` |
| Server farm LAN | `10.10.3.0/28` | `10.10.3.1–10.10.3.14` | `10.10.3.14` |

### Suggested server addresses

Use these only if they match the actual Packet Tracer configuration; otherwise update this table to reflect the real addresses.

| Server | Suggested IP address | Default gateway |
|---|---|---|
| DNS | `10.10.3.2/28` | `10.10.3.14` |
| DHCP | `10.10.3.3/28` | `10.10.3.14` |
| Web | `10.10.3.4/28` | `10.10.3.14` |

## Router-to-Router WAN Subnets

These point-to-point subnets are taken from the project scenario. Each `/30` subnet provides two usable IPv4 addresses.

### Branch A / OSPF-side WAN links

| Link subnet | Network address | Usable addresses | Broadcast |
|---|---|---|---|
| WAN A1 | `10.0.0.0/30` | `10.0.0.1–10.0.0.2` | `10.0.0.3` |
| WAN A2 | `10.0.0.4/30` | `10.0.0.5–10.0.0.6` | `10.0.0.7` |

### Branch B / EIGRP-side WAN links

| Link subnet | Network address | Usable addresses | Broadcast |
|---|---|---|---|
| WAN B1 | `10.0.1.0/30` | `10.0.1.1–10.0.1.2` | `10.0.1.3` |
| WAN B2 | `10.0.1.8/30` | `10.0.1.9–10.0.1.10` | `10.0.1.11` |
| WAN B3 | `10.0.1.12/30` | `10.0.1.13–10.0.1.14` | `10.0.1.15` |

The scenario also lists `10.0.1.4/30` nowhere; no additional WAN subnet is assumed beyond those explicitly provided. Confirm the intended router-to-router link allocation against the topology.

## IPv6

| Link | IPv6 prefix | Endpoint addresses |
|---|---|---|
| R1–R4 | `2001:db8:1::/64` | R1: `2001:db8:1::1/64`; R4: `2001:db8:1::2/64` |

`2001:db8::/32` is reserved for documentation/examples, so these addresses are appropriate for a lab.

## Quick Subnet Reference

| Prefix | Total addresses | Usable IPv4 host addresses |
|---|---:|---:|
| `/25` | 128 | 126 |
| `/26` | 64 | 62 |
| `/27` | 32 | 30 |
| `/28` | 16 | 14 |
| `/30` | 4 | 2 |
