# Multi-AS-BGP-Network-Topology
# BGP Multi-Autonomous System Network Simulation using Cisco Packet Tracer

## 📖 Overview
This project demonstrates the implementation of Border Gateway Protocol (BGP) in Cisco Packet Tracer. The network topology consists of three routers configured as separate Autonomous Systems (AS100, AS200, and AS300). Each AS contains its own local LAN, and external BGP (eBGP) is used to exchange routing information between the autonomous systems.

The project showcases how BGP enables communication between different networks by establishing neighbor relationships and advertising network prefixes.

---

## 🎯 Project Objectives
- Configure eBGP between multiple Autonomous Systems.
- Advertise local LAN networks using BGP.
- Verify BGP neighbor relationships.
- Test routing and end-to-end connectivity between all LANs.
- Understand inter-domain routing concepts.

---

## 🌐 Network Topology

### Autonomous Systems
| Router | Autonomous System | LAN Network |
|------|------|------|
| R1 | AS 100 | 192.168.10.0/24 |
| R2 | AS 200 | 192.168.20.0/24 |
| R3 | AS 300 | 192.168.30.0/24 |

### WAN Links
| Connection | Network |
|----------|----------|
| R1 ↔ R2 | 192.168.12.0/30 |
| R2 ↔ R3 | 192.168.23.0/30 |

---

## 🛠️ Technologies Used
- Cisco Packet Tracer
- Border Gateway Protocol (BGP)
- IPv4 Addressing
- Cisco IOS CLI
- Routing Verification Commands

---

## ⚙️ Key BGP Configuration


##  R1 (AS 100)
- router bgp 100
- neighbor 192.168.12.2 remote-as 200
- network 192.168.10.0 mask 255.255.255.0

##  R2 (AS 200)
- router bgp 200
- neighbor 192.168.12.1 remote-as 100
- neighbor 192.168.23.2 remote-as 300
- network 192.168.20.0 mask 255.255.255.0

##  R3 (AS 300)
- router bgp 300
- neighbor 192.168.23.1 remote-as 200
- network 192.168.30.0 mask 255.255.255.0

## 🚀 How to Run
1. Download and install **Cisco Packet Tracer**
2. Clone this repository:
git clone https://github.com/yourusername/BGP-Multi-AS-Network-Simulation.git
3. Open `BGP.pkt` in Cisco Packet Tracer
4. Use **Simulation Mode** to observe BGP packet flow
5. Test connectivity using `ping` between PCs across different AS networks

---

## 🧠 Concepts Covered
- BGP Autonomous Systems (AS)
- eBGP (External BGP) neighbor configuration
- Route advertisement between AS
- WAN serial link configuration
- IP subnetting (/30 for point-to-point links)

---

## 👤 Author  
Md Arif Shaikh  
B.Sc. in Computer Science & Engineering  
CCNA | MTCNA | Networking Enthusiast
