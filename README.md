# VLAN Lab – Packet Tracer

## Overview
This lab demonstrates creating and testing VLANs on a Cisco 2960 switch.  
Two VLANs were configured:
- **VLAN 10:** PC0 and PC1
- **VLAN 20:** PC2 and PC3

PCs in the same VLAN can communicate successfully, while PCs in different VLANs cannot communicate without routing.

---

## Topology
![Topology](Topology.png)

---

## IP Configuration
| Device | VLAN | IP Address | Subnet Mask |
|--------|------|------------|-------------|
| PC0 | VLAN 10 | 192.168.10.10 | 255.255.255.0 |
| PC1 | VLAN 10 | 192.168.10.11 | 255.255.255.0 |
| PC2 | VLAN 20 | 192.168.20.10 | 255.255.255.0 |
| PC3 | VLAN 20 | 192.168.20.11 | 255.255.255.0 |

**PC Screenshots:**
- ![PC0 IP Config](PC0%20IP%20Config.png)
- ![PC1 IP Config](PC1%20IP%20Config.png)
- ![PC2 IP Config](PC2%20IP%20Config.png)
- ![PC3 IP Config](PC3%20IP%20Config.png)

---

## Switch Configuration
### VLAN Creation
![Configure VLAN](Configure%20VLAN.png)

### Assign Ports
- Ports `Fa0/1-2` → VLAN 10  
![Assign Ports 10](Assign%20Ports%2010.png)

- Ports `Fa0/3-4` → VLAN 20  
![Assign Ports 20](Assign%20Ports%2020.png)

---

## Test Results
✅ PC0 → PC1 (same VLAN): Successful  
✅ PC2 → PC3 (same VLAN): Successful  
❌ PC0 → PC2 (different VLANs): Fails as expected  

**Ping Results:**
- ![Ping PC0](Ping%20PC0.png)
- ![Ping PC2](Ping%20PC2.png)
- ![Failed Ping PC0](Failed%20Ping%20PC0.png)

---

## Packet Tracer File
[Download VLAN-Lab.pkt](VLAN-Lab.pkt)

---
*Created as part of my networking portfolio in Cisco Packet Tracer.*
