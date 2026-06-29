# CCNA Lab 01 – Static Routing

## Overview

This project demonstrates the implementation of Static Routing using Cisco Packet Tracer. The lab focuses on enabling communication between two separate LANs through manual route configuration while reinforcing fundamental routing concepts, IP addressing, and network troubleshooting.

## Objectives

- Configure IPv4 addressing on routers and end devices.
- Implement static routes between two routers.
- Verify routing table entries.
- Establish end-to-end connectivity across different networks.
- Practice network verification and troubleshooting using Cisco IOS.

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- IPv4 Addressing
- Static Routing

## Network Topology

```
PC0 ---- SW1 ---- R1 ===== R2 ---- SW2 ---- PC2
```

## IP Addressing

### Network 1

| Device | Interface | IP Address |
|---------|-----------|------------|
| R1 | GigabitEthernet0/0 | 192.168.10.1/24 |
| PC0 | NIC | 192.168.10.2/24 |
| PC1 | NIC | 192.168.10.3/24 |

Default Gateway: **192.168.10.1**

### WAN Network

| Device | Interface | IP Address |
|---------|-----------|------------|
| R1 | GigabitEthernet0/1 | 10.10.1.1/24 |
| R2 | GigabitEthernet0/1 | 10.10.1.2/24 |

### Network 2

| Device | Interface | IP Address |
|---------|-----------|------------|
| R2 | GigabitEthernet0/0 | 192.168.20.1/24 |
| PC2 | NIC | 192.168.20.2/24 |
| PC3 | NIC | 192.168.20.3/24 |

Default Gateway: **192.168.20.1**

## Static Route Configuration

### Router R1

```bash
ip route 192.168.20.0 255.255.255.0 10.10.1.2
```

### Router R2

```bash
ip route 192.168.10.0 255.255.255.0 10.10.1.1
```

## Verification

The following commands were used to validate the configuration:

```bash
show ip route
show ip interface brief
show running-config
ping
traceroute
```

## Routing Table Codes

| Code | Description |
|------|-------------|
| C | Connected Route |
| L | Local Route |
| S | Static Route |

## Key Concepts

- Routing Fundamentals
- Connected Routes
- Local Routes
- Static Routing
- Next-Hop Routing
- Routing Table Analysis
- End-to-End Connectivity
- Basic Network Troubleshooting

## Troubleshooting Performed

- Verified interface status (`up/up`)
- Validated IP addressing
- Confirmed default gateway configuration
- Verified router-to-router connectivity
- Corrected next-hop IP configuration
- Configured static routes on both routers
- Validated routing table entries
- Tested end-to-end communication

## Project Structure

```
CCNA-Lab-01-Static-Routing/
│
├── Static-Routing.pkt
├── README.md
├── configurations/
└── screenshots/
```

## Learning Outcomes

After completing this lab, I gained practical experience in:

- Configuring static routes using Cisco IOS
- Understanding routing table operations
- Analyzing packet forwarding decisions
- Troubleshooting routing connectivity issues
- Verifying network communication using Cisco CLI tools

## Skills Demonstrated

- Cisco Networking
- Cisco IOS CLI
- Static Routing
- IPv4 Addressing
- Network Troubleshooting
- Packet Tracer
- Routing Table Analysis

## Author

**Gokulakannan V**

B.Tech Computer Science and Engineering
