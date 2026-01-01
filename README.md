## Inter-VLAN-Routing-Using-Router-on-a-Stick

 **Project Overview**

This project demonstrates VLAN segmentation and inter-VLAN routing using a Router-on-a-Stick (ROAS) approach in Cisco Packet Tracer.

Multiple VLANs are created on a Layer-2 switch, end devices are assigned to their respective VLANs, and a single router interface is sub-divided into 802.1Q subinterfaces to enable communication between VLANs.

This lab focuses on fundamental Layer-2 and Layer-3 concepts commonly used in entry-level enterprise networks.

## Network Topology

- 1 × Cisco 1941 Router

- 1 × Cisco 2960 Layer-2 Switch

- 4 × End Devices (PCs)

- VLANs segmented by department

- Trunk link between switch and router



**VLAN Design**

| VLAN ID | Name | Subnet          |
| ------- | ---- | --------------- |
| 10      | HR   | 192.168.1.0 /24 |
| 20      | IT   | 192.168.2.0 /24 |

Each VLAN uses a dedicated default gateway configured on router subinterfaces.

## Configuration Summary

**Switch Configuration**

- VLANs created and named

- Access ports assigned to correct VLANs

- Trunk port configured toward router

 Key concepts:
- switchport mode access

- switchport access vlan

- switchport mode trunk

**Router Configuration (ROAS)**

- Physical interface enabled

- Subinterfaces created per VLAN

- 802.1Q encapsulation applied

- IP addresses configured as default gateways

Key concepts:

- encapsulation dot1q

- Subinterface-based routing

- Inter-VLAN traffic forwarding

**End Device Configuration**

- Static IPv4 addressing

- Subnet masks aligned with VLANs

- Default gateway pointing to router subinterface IP

## Verification & Testing

- ICMP ping tested between devices in different VLANs

- Successful end-to-end connectivity confirmed

- Packet flow verified using Simulation Mode

Example test:

- PC in VLAN 10 → PC in VLAN 20 → Success

## What This Project Demonstrates

- Understanding of VLAN segmentation

- Practical inter-VLAN routing using ROAS

- Layer-2 vs Layer-3 responsibilities

- Basic enterprise traffic flow

- Hands-on configuration and validation

## ⚠️ Limitations

- Single router introduces a single point of failure

- No redundancy or failover mechanisms

- No ACLs or security filtering implemented

(These are intentional to keep the lab focused on fundamentals.)

## Tools Used

- Cisco Packet Tracer

- Cisco IOS CLI

## Purpose

This project was created to strengthen networking fundamentals and to serve as a hands-on portfolio lab for entry-level roles such as:

- Network Support

- NOC Trainee

- Junior Network Engineer
