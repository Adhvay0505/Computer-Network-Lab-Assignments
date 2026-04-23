# 🌐 Basic Enterprise Connectivity Simulation

## 📌 Student Details

* **Name:** Adhvay Banerjee
* **roll no:** 2301410002 


---

# 📖 1. Objective

The objective of this assignment is to design and implement a basic enterprise network using routers, switches, and PCs. The network demonstrates **IP addressing, DHCP configuration, and dynamic routing using RIP v2**, ensuring end-to-end connectivity.

---

# 🧠 2. Concepts Covered

* IPv4 Addressing
* DHCP (Dynamic Host Configuration Protocol)
* WAN Connectivity (Serial Link)
* Routing using RIP v2
* End-to-End Network Communication

---

# 🏗️ 3. Network Topology

The network consists of:

* 2 Routers (R1, R2)
* 2 Switches
* 4 PCs (2 per LAN)
* WAN connection between routers

### 🔹 Logical Diagram

```id="topo_ent"
PC0   PC1          PC2   PC3
 |     |            |     |
SW1               SW2
 |                 |
R1  -----------  R2
        (WAN)
```
<img width="1390" height="492" alt="Screenshot_2026-04-23_11-47-26" src="https://github.com/user-attachments/assets/51c13bc3-a931-4586-8754-6b33ffe70b19" />


---

# 🔌 4. Network Configuration

## 📍 IP Addressing Scheme

### LAN 1 (R1 Side)

* Network: 192.168.1.0/24
* Gateway: 192.168.1.1

### LAN 2 (R2 Side)

* Network: 192.168.2.0/24
* Gateway: 192.168.2.1

### WAN Link

* Network: 10.0.0.0/30

| Device | Interface | IP Address  |
| ------ | --------- | ----------- |
| R1     | G0/0      | 192.168.1.1 |
| R1     | S0/3/0    | 10.0.0.1    |
| R2     | G0/0      | 192.168.2.1 |
| R2     | S0/3/0    | 10.0.0.2    |

---

## 🔗 Cabling

* PC ↔ Switch → Copper Straight-Through
* Switch ↔ Router → Copper Straight-Through
* Router ↔ Router → Serial DCE cable

---

# ⚙️ 5. Configuration Details

## 🔹 Router R1

* Configured LAN interface (192.168.1.1)
* Configured WAN interface (10.0.0.1)
* Enabled DHCP server
* Configured RIP v2

## 🔹 Router R2

* Configured LAN interface (192.168.2.1)
* Configured WAN interface (10.0.0.2)
* Configured RIP v2

---

## 🟢 DHCP Configuration (on R1)

* IP range assigned dynamically to PCs in LAN1
* Default gateway: 192.168.1.1
* DNS server: 8.8.8.8

---

## 🔁 Routing Configuration

* RIP version 2 used
* Auto-summary disabled
* Networks advertised:

  * 192.168.1.0
  * 192.168.2.0
  * 10.0.0.0

---

# 🧪 6. Verification

### 🔹 Connectivity Test

* Ping from PC0 (LAN1) → PC2 (LAN2)

✔ Result: **Successful**

---

### 🔹 Routing Verification

* Used `show ip route`
* Verified routes learned via RIP

---

# 📊 7. Observations

* DHCP successfully assigned IP addresses to LAN1 PCs
* Static IPs used for LAN2 PCs
* RIP v2 enabled communication between both LANs
* WAN link successfully carried traffic between routers

---

# ⚠️ 8. Challenges Faced

* Identifying correct serial interfaces
* Configuring clock rate on DCE side
* Ensuring all interfaces were enabled (`no shutdown`)

---

# 🚀 9. Improvements

* Implement DHCP relay for LAN2
* Add DNS server for name resolution
* Expand network with additional subnets
* Use more advanced routing protocols like OSPF

---

# 🧾 10. Conclusion

The simulation successfully demonstrated basic enterprise connectivity using routers, switches, and dynamic routing. End-to-end communication was achieved using RIP v2, and DHCP simplified IP address allocation.

---

# ▶️ 11. How to Run

1. Open `.pkt` file in Cisco Packet Tracer
2. Verify configurations
3. Use Command Prompt on PCs
4. Ping between LANs
5. Observe routing tables if needed

---

# 📁 12. Files Included

* `exp5_ack_observation.pkt`
* `README.md`
* `output_exp5.txt`
* `report_exp5.pdf`

---

