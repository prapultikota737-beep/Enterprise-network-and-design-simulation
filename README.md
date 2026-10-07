Enterprise Network Design & Simulation
Project Overview

This project focuses on designing and implementing an enterprise network using Cisco Packet Tracer. The network connects multiple departments through switches and a router and uses VLANs, IP addressing, trunking, and inter-VLAN routing for communication.

Objectives
Design an enterprise network topology.
Connect PCs, switches, router, and server.
Create separate VLANs for different departments.
Assign IP addresses to network devices.
Configure trunk and access ports.
Configure inter-VLAN routing using Router-on-a-Stick.
Test connectivity between different networks.

Network Topology

The project contains:

1 × Cisco 2911 Router
4 × Switches
Core-SW
HR-SW
Finance-SW
IT-SW
6 × PCs
1 × Server
Departments
HR Department
Finance Department
IT Department
Server Network

VLAN & IP Addressing
VLAN	Department	Network	Gateway
VLAN 10	HR	192.168.10.0/24	192.168.10.1
VLAN 20	Finance	192.168.20.0/24	192.168.20.1
VLAN 30	IT	192.168.30.0/24	192.168.30.1
VLAN 40	Server	192.168.40.0/24	192.168.40.1

Device IP Addresses
PC0 → 192.168.10.10
PC1 → 192.168.10.11
PC2 → 192.168.20.10
PC3 → 192.168.20.11
PC4 → 192.168.30.10
PC5 → 192.168.30.11
Server → 192.168.40.10

All devices use a /24 subnet mask (255.255.255.0).

Configuration
Switch Configuration
Created VLANs 10, 20, 30, and 40.
Assigned department PC ports to their respective VLANs.
Configured connections between switches as trunk ports.
Configured the server port as an access port in VLAN 40.
Router Configuration
Enabled Router-on-a-Stick.
Created subinterfaces for VLAN 10, 20, 30, and 40.
Assigned gateway IP addresses to each subinterface.
Enabled communication between different VLANs.

Testing

Network connectivity was tested using the ping command.

Examples:

PC0 → 192.168.10.1
PC0 → 192.168.20.10
PC0 → 192.168.30.10
PC0 → 192.168.40.10

Successful ping responses confirm connectivity between the devices and networks.

Team Members

Team Lead:
PRAPUL RAJAKUMAR

Members:

PRAVEEN WALI
MANVITH KUMAR N

Tools Used
Cisco Packet Tracer
Cisco 2911 Router
Cisco Switches
PCs and Server
VLAN
IPv4
Router-on-a-Stick

Conclusion

The project successfully demonstrates the design and implementation of an enterprise network. VLANs provide logical separation between departments, while inter-VLAN routing enables communication between different networks. The network was tested using ping to verify connectivity.

## 👥 Contributors

- **PRAPUL RAJAKUMAR** — Team Lead / Network Design
- **PRAVEEN WALI** — Configuration & Implementation
- **MANVITH KUMAR N** — Testing & Documentation

- ## 👥 Contributors

| Name | Role |
|---|---|
| PRAPUL RAJAKUMAR | Team Lead / Network Design |
| PRAVEEN WALI | Configuration & Implementation |
| MANVITH KUMAR N | Testing & Documentation |
