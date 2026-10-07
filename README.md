# Enterprise Network Design & Simulation

## Project Overview

This project focuses on designing and implementing an enterprise network using Cisco Packet Tracer.

The network connects multiple departments through switches and a router. VLANs are used to provide logical separation between departments, while Router-on-a-Stick enables communication between different VLANs.

## Problem Statement

Design and simulate an enterprise network that provides separate network segments for different departments while allowing controlled communication between them.

The network should use VLANs, IP addressing, trunking, and inter-VLAN routing to provide reliable communication between departments and the server network.

## Objectives

* Design an enterprise network topology.
* Connect PCs, switches, router, and server.
* Create separate VLANs for different departments.
* Assign appropriate IP addresses.
* Configure access and trunk ports.
* Configure inter-VLAN routing using Router-on-a-Stick.
* Test connectivity between different VLANs.
* Verify network communication using ping.

## Tools and Technologies

* Cisco Packet Tracer
* Cisco 2911 Router
* Cisco Switches
* PCs
* Server
* VLAN
* IPv4 Addressing
* Trunking
* Router-on-a-Stick

## Network Topology

The project contains:

* 1 × Cisco 2911 Router
* 4 × Switches

  * Core-SW
  * HR-SW
  * Finance-SW
  * IT-SW
* 6 × PCs
* 1 × Server

### Departments

* HR Department
* Finance Department
* IT Department
* Server Network

## VLAN and IP Addressing

| VLAN    | Department | Network         | Gateway      |
| ------- | ---------- | --------------- | ------------ |
| VLAN 10 | HR         | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 | Finance    | 192.168.20.0/24 | 192.168.20.1 |
| VLAN 30 | IT         | 192.168.30.0/24 | 192.168.30.1 |
| VLAN 40 | Server     | 192.168.40.0/24 | 192.168.40.1 |

### Device IP Addresses

| Device | IP Address    |
| ------ | ------------- |
| PC0    | 192.168.10.10 |
| PC1    | 192.168.10.11 |
| PC2    | 192.168.20.10 |
| PC3    | 192.168.20.11 |
| PC4    | 192.168.30.10 |
| PC5    | 192.168.30.11 |
| Server | 192.168.40.10 |

**Subnet Mask:** `255.255.255.0`

## Configuration

### Switch Configuration

* Created VLANs 10, 20, 30, and 40.
* Assigned department PC ports to their respective VLANs.
* Configured connections between switches as trunk ports.
* Configured the server port as an access port in VLAN 40.

### Router Configuration

Router-on-a-Stick was configured on the Cisco 2911 router.

Subinterfaces were created for:

* VLAN 10
* VLAN 20
* VLAN 30
* VLAN 40

Gateway IP addresses were assigned to each subinterface to enable communication between different VLANs.

## Testing

Network connectivity was tested using the `ping` command.

Example tests:

```text
PC0 → 192.168.10.1
PC0 → 192.168.20.10
PC0 → 192.168.30.10
PC0 → 192.168.40.10
```

Successful ping responses confirm connectivity between the devices and different VLANs.

## Project Files

```text
Enterprise-network-and-design-simulation/
│
├── README.md
├── Network_Project_Final.pkt
│
├── screenshots/
│   ├── network-topology.png
│   ├── vlan-configuration.png
│   
│
└── docs/
    └── Problem-Statement.pdf
```

## Contributors

| Name                 | Role                           |
| -------------------- | ------------------------------ |
| **Prapul Rajakumar** | Team Lead / Network Design     |
| **Praveen Wali**     | Configuration & Implementation |
| **Manvith Kumar N**  | Testing & Documentation        |

## Conclusion

The project successfully demonstrates the design and implementation of an enterprise network.

VLANs provide logical separation between departments, while inter-VLAN routing enables communication between different networks. The network was tested using ping to verify connectivity between devices and VLANs.
