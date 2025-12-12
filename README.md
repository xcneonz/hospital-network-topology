# Hospital Network Design – Cisco Packet Tracer

This repository contains the complete network design and configuration for a multi-branch hospital system, built using **Cisco Packet Tracer**.

The project simulates a solid network connecting four distinct hospital branches via a WAN mesh topology. It incorporates LAN design, VLSM subnetting, dynamic routing, server configuration (DHCP, DNS, Email) and IoT automations.

## 📍 Branch Breakdown

The network connects four specialized medical branches across different locations. Each branch features a custom LAN topology tailored to its operational needs.

   Branch        |         Functions 

Optic Centre    | LAN Design, VLSM, IoT (RFID, Fire System) 
Pharmacy        | Wired/Wireless LAN, DHCP Configuration |
Surgical Centre | Hybrid Topology, Access Point Setup, IP Scheme |
Main Hospita  l | WAN Mesh Design, Public IPs, Dynamic Routing (RIPv2) |


## Network Features

### 1. LAN Design & Switching
- **Topologies:** Utilizes Star, Tree, and Hybrid topologies for scalability.
- **Subnetting:** Department-based segmentation using **VLSM** (Variable Length Subnet Masks).
- **Wireless:** Secure wireless access points configured with **WPA2-PSK**.

### 2. WAN Connectivity
- **Topology:** Full Mesh topology connecting all four branches for maximum redundancy and fault tolerance.
- **Routing:** Dynamic routing configured using **RIPv2** to handle path selection.
- **Addressing:** Public IP addressing scheme for WAN serial links.

### 3. IP Addressing (VLSM)
- Optimized IPv4 allocation based on department size (host requirements).
- Subnets range from `/27` to `/29` to minimize address wastage.
- Dedicated subnets for WAN serial connections.

### 4. Device Configuration & Security
- **Basic Config:** Hostnames, Console passwords, Enable/Secret passwords.
- **Interface Config:** IP addressing, Clock rates (DCE side).
- **Services:** DHCP Pools for dynamic host allocation.
- **Management:** Message of the Day (MOTD) banners, Configs saved to NVRAM.

### 5. Server & IoT Implementation
- **Servers:** Configured DNS, Email, and Web servers for hospital communication.
- **IoT Automation (Putrajaya Branch):**
  - **Access Control:** RFID Reader paired with a Smart Door.
  - **Safety System:** Smoke Detector linked to a Water Sprinkler and Siren.
  - **Management:** All IoT devices managed centrally via a Home Gateway.


## Technologies Used

- **Software:** Cisco Packet Tracer
- **Addressing:** IPv4, VLSM
- **Routing Protocols:** RIPv2, Static Routing
- **Services:** DHCP, DNS, SMTP/POP3 (Email), HTTP
- **Wireless Security:** WPA2-PSK
- **IoT:** Registration Server, Home Gateway, Sensors/Actuators


## Files Included

- `Hospital-Network.pkt`: The main Packet Tracer simulation file.
- `README.md`: Project documentation.


## How to Run

1. **Install:** Ensure you have **Cisco Packet Tracer** installed (Version 8.0 or newer recommended).
2. **Open:** Download and open the `Hospital-Network.pkt` file.
3. **Boot:** Allow the network a few minutes for STP convergence and RIP routing updates.
4. **Test:**
   - Use the `Simple PDU` tool or `ping` command to test connectivity between branches.
   - Open a PC browser to test the web server.
   - Send an email between user PCs to test the Email server.
   - Interact with the IoT devices in the Optic Centre branch (Alt+Click).

