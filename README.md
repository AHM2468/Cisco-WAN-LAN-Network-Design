# Cisco WAN & LAN Network Topology Design

A simulated enterprise network topology designed and configured using Cisco Packet Tracer to achieve seamless end-to-end communication between multiple Local Area Networks (LANs) across two Wide Area Networks (WANs).

## 🌐 Network Architecture & Addressing Scheme

The network is split into two distinct WAN regions connected via a serial link interface:

### **WAN 1 (Router 0)**
* **LAN 1:** `192.168.5.0/24` | Default Gateway: `192.168.5.1`
* **LAN 2:** `192.168.10.0/24` | Default Gateway: `192.168.10.1`

### **WAN 2 (Router 1)**
* **LAN 3:** `192.168.15.0/24` | Default Gateway: `192.168.15.1`
* **LAN 4:** `192.168.20.0/24` | Default Gateway: `192.168.20.1`

### **WAN Serial Link**
* **Network Interconnect:** `10.0.5.0/8`
* **Router 0 (WAN Interface):** `10.0.5.1`
* **Router 1 (WAN Interface):** `10.0.5.2`

## 🚦 Routing Protocol
- **Method:** Dynamic Routing via **RIP (Routing Information Protocol)**.
- **Why RIP?** Chosen for its automated routing table updates and efficient convergence topology management, suitable for optimal path selection in small-to-medium network architectures.

## 🛠️ Configuration Challenges & Solutions
1. **IP Conflict Errors:** Resolved unexpected address duplication within LANs by re-mapping unique host identifiers.
2. **Packet Transmission Failures:** Debugged end-to-end packet delivery failures across WAN links by resetting RIP routing advertisements to ensure all edge networks were correctly propagated.
3. **Disabled Interfaces:** Resolved a physical layer link failure by manually activating the default-disabled serial interfaces on both boundary routers.

## 📂 Repository Content
- `Network_Topology.pkt`: The original Cisco Packet Tracer design file for verification and live simulation testing.
