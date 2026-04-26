# 🌐 README.md

## Experiment 8: Network Performance Analysis Simulator (Packet Delay, Loss, Throughput & Routing Algorithms)

## 📌 Student Details

* **Name:** Your Name
* **Course:** Network Lab
* **Experiment:** Network Simulator using Cisco Packet Tracer

---

# 📖 1. Objective

The purpose of this experiment is to design and simulate a network using Cisco Packet Tracer in order to:

* Analyze packet delay
* Measure packet loss
* Evaluate end-to-end throughput
* Implement routing algorithms:

  * Static Routing
  * RIP
  * OSPF
  * EIGRP

The experiment compares routing performance under different traffic conditions.

---

# 🧠 2. Learning Outcomes

* Understand packet delay, packet loss, and throughput
* Design multi-router enterprise network topology
* Implement routing protocols
* Analyze network performance under varying loads
* Compare routing algorithms
* Improve network efficiency

---

# 🏗️ 3. Network Topology Design

## 🔹 Devices Used

* 4 PCs
* 2 Switches
* 2 Routers
* Copper Straight-Through cables
* Serial WAN link (optional for advanced routing)

---

## 🔹 Logical Topology

```text id="topo_net"
PC0 ---- Switch0 ---- Router0 ---- Router1 ---- Switch1 ---- PC2
PC1 ---- Switch0                     Switch1 ---- PC3
```

---

# 🌐 4. IP Addressing Scheme

## LAN 1:

* Network: 192.168.1.0/24
* Gateway: 192.168.1.1

## LAN 2:

* Network: 192.168.2.0/24
* Gateway: 192.168.2.1

---

| Device | IP Address  | Subnet Mask   | Default Gateway |
| ------ | ----------- | ------------- | --------------- |
| PC0    | 192.168.1.2 | 255.255.255.0 | 192.168.1.1     |
| PC1    | 192.168.1.3 | 255.255.255.0 | 192.168.1.1     |
| PC2    | 192.168.2.2 | 255.255.255.0 | 192.168.2.1     |
| PC3    | 192.168.2.3 | 255.255.255.0 | 192.168.2.1     |

---

# 🔌 5. Cabling Structure

* PC ↔ Switch → Copper Straight-Through
* Switch ↔ Router → Copper Straight-Through
* Router ↔ Router → Serial DCE or Copper crossover (depending setup)

---

# ⚙️ 6. Router Configuration

## Router0

* Interface Fa0/0 → 192.168.1.1
* WAN/Link Interface → Routed to Router1

## Router1

* Interface Fa0/1 → 192.168.2.1
* WAN/Link Interface → Routed to Router0

---

# 🔁 7. Routing Algorithm Implementation

---

## 🟢 Static Routing

* Manual route configuration
* Reliable for small networks
* Low scalability

### Commands:

```bash id="static_r"
ip route 192.168.2.0 255.255.255.0 [next-hop]
```

---

## 🔵 RIP

* Distance vector routing
* Hop-count based
* Easy to configure
* Slower convergence

---

## 🟣 OSPF

* Link-state routing
* Faster convergence
* Better scalability
* Lower packet delay

---

## 🟠 EIGRP

* Advanced Cisco protocol
* Fastest convergence
* Efficient bandwidth use

---

# 📊 8. Traffic Simulation

## Tools Used:

* Add Simple PDU (ICMP)
* Continuous ping
* FTP traffic
* Simulation Mode
* Event List analysis

---

# 🔍 9. Performance Metrics Measured

### Packet Delay

* Time taken for packet delivery
* Measured using Event List timestamps

### Packet Loss

* Number of dropped packets
* Observed during congestion/error simulations

### Throughput

* Successful packet delivery rate over time

---

# 📈 10. Comparative Routing Performance

| Routing Protocol | Delay    | Packet Loss | Throughput | Complexity |
| ---------------- | -------- | ----------- | ---------- | ---------- |
| Static Routing   | Low      | Low         | Moderate   | Low        |
| RIP              | Medium   | Medium      | Moderate   | Low        |
| OSPF             | Low      | Low         | High       | Medium     |
| EIGRP            | Very Low | Very Low    | Very High  | Medium     |

---

# 🔬 11. Observations

### Static Routing:

* Stable
* Manual
* Good for simple networks

### RIP:

* Functional
* Slower under larger traffic

### OSPF:

* Faster adaptation
* Better performance

### EIGRP:

* Best overall efficiency
* Lowest delay

---

# ⚠️ 12. Challenges Faced

* Routing table verification
* Serial interface activation
* Congestion simulation
* Packet capture interpretation

---

# 🚀 13. Improvements

* Add larger topologies
* Simulate failures
* Introduce QoS
* Include VLANs
* Test under heavier traffic

---

# 🧾 14. Conclusion

The experiment successfully demonstrated how routing algorithms affect:

* Delay
* Packet loss
* Throughput

### Key Result:

* **EIGRP and OSPF** performed best
* **RIP** was simpler but less efficient
* **Static Routing** was effective for small networks

---

# ▶️ 15. How to Run

1. Open `network_topology.pkt`
2. Verify IP configurations
3. Enable routing protocol
4. Switch to Simulation Mode
5. Generate traffic
6. Record metrics
7. Capture screenshots

---

# 📁 16. Files Included

* `network_topology.pkt`
* `README.md`
* `output.txt`
* `test_cases.txt`

---

