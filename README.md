# 🚇 The Metro Network Infrastructure Project

This project involves designing and configuring a **sustainable, secure, and efficient network infrastructure** for the **Dhaka Mass Transit Company Limited (DMTCL)**. The initiative supports free internet/Wi-Fi access for commuters and enables robust inter-station connectivity within the **MRT-6 Metro Rail Line**.

---

## 📍 Project Background
DMTCL has established a metro rail route from **Agargaon to Uttara**, which will eventually expand throughout Dhaka. The current MRT-6 line has **nine metro stations** across **Agargaon, Mirpur, and Uttara**.

To ensure efficient daily operations and commuter services, a reliable computer network must be constructed, following DMTCL’s specific requirements.

---

## 🏗️ Requirements & Specifications

### 📡 Stations Selected for Testing Internet Access
The six busiest stations and their expected maximum daily users:

- **Uttara-North** → 1200  
- **Uttara-Center** → 1700  
- **Agargaon** → 2250  
- **Mirpur-10** → 2500  
- **Shewrapara** → 700  
- **Pallabi** → 1100  

---

### 🏢 Network Design Constraints
- **Head Office**: Located in **Agargaon** (acts as center-point).  
- **Special Connections**:
  - Uttara-Center ↔ Uttara-North ↔ Agargaon must be interconnected.
  - Mirpur-10 ↔ Agargaon (direct connection required).
  - Mirpur-10 ↔ Shewrapara and Mirpur-10 ↔ Pallabi (cost-effective setup).  

---

### 🌐 IP Addressing & Subnetting
- Use **VLSM (Variable Length Subnet Masking)** to minimize IP wastage.  
- **Static IP addressing**:  
  - Uttara-Center  
  - Mirpur-10  
- **Dynamic IP addressing (via DHCP Server in Uttara-Center)**:  
  - Agargaon, Uttara-North, Shewrapara, Pallabi  

---

### 🖥️ Servers & Services
- **DHCP Server** → Uttara-Center  
- **Email Server** → Mirpur-10  
- **Web Server** → Uttara-Center  
  - Domain: `www.dhaka.metro`  
  - Webpage: *“Welcome to DMTCL!”*  
- **DNS Server** → Uttara-Center  
- **Printers** → Uttara-North & Pallabi  

*(All servers will be configured manually.)*

---

### 🚦 Routing Rules
- **Static Routing**:
  - Uttara-North and Uttara-Center  
  - Uttara-Center ↔ Agargaon (primary)  
  - Uttara-North communicates with Agargaon **via Uttara-Center**  
  - Backup static route: Uttara-North ↔ Agargaon  
- **Dynamic Routing**:
  - Mirpur-10, Shewrapara, Pallabi  
- ❌ **No default routes allowed** — only static or dynamic entries permitted.

---

### 🔧 Implementation Assumptions
- Each metro station is represented as a **router**, with enough **switches** to connect devices.  
- For user devices, **2 end devices per network** are sufficient to simulate the overall user base.  
- Network should allow **full station-to-station ping reachability** after configuration.  

---

## 📦 Deliverables
1. Cisco Packet Tracer project file (`.pkt`)  
2. Network topology diagram (with labels)  
3. Configuration commands for all routers  
4. VLSM tree  
5. IP/Network address table  
6. Documented assumptions  

---

## ✅ Outcomes
By the end of this project:
- All stations can **communicate securely**.  
- Users in selected stations receive free Wi-Fi/internet.  
- Required **servers & services** (Web, DNS, Email, DHCP, printers) are operational.  
- Routing is configured with **correct static and dynamic policies**.  

---
 
