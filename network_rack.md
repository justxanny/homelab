# Hook and Ladder 8 - Network layout.

## 📡 UCG Ultra – Rear Port Connections (Left → Right)
--------------------------------------------------
- Port 1 (LAN1): ASUS WiFi AP  
- Port 2 (LAN2): Keymaster (Proxmox host)  
- Port 3 (LAN3): Gatekeeper (Proxmox Backup Server)  
- Port 4 (LAN4): Uplink to TP-Link 8-port switch  
- WAN (2.5G): Internet connection  
- USB-C: Power

## 🗄 Rack – 12-Port Keystone Panel
--------------------------------
- Port 1: Uplink from UCG Ultra Port 4 → TP-Link Switch  
- Port 2: NAS Connection 1  
- Port 3: NAS Connection 2  
- Port 4: Uplink to 4-port switch → Spengler (Desktop)  
- Port 5–9: Available / Reserved  
- Port 10: ASUS Wifi AP  
- Port 11: Keymaster  
- Port 12: Gatekeeper  

## 🖥 Key Devices
--------------
- **Keymaster**: HP EliteDesk Mini, Proxmox host, VLAN 10 (Main)
- **Gatekeeper**: HP EliteDesk Mini, Proxmox Backup Server, VLAN 10 (Main)
- **NAS**: TerraMaster F2-221, dual connections to Rack Ports 2 & 3
- **Spengler**: Desktop PC via 4-port switch uplink (Rack Port 4)
- **ASUS WiFi AP**: RT-AX86U in AP mode, connected to UCG Ultra Port 1

🛡 Notes
--------
- UCG Ultra LAN4 can be reconfigured as WAN2 for failover
- NAS connected with dual Ethernet for redundancy or LAG
- Physical labels match Rack Port numbers for quick tracing
