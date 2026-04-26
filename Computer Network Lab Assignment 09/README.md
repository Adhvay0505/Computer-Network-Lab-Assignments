# 🌐 Experiment 9: Transport Layer Protocol Simulation (UDP, TCP, SCTP)

---

# 📖 1. Objective

The purpose of this experiment is to design and simulate **transport layer communication** using:

* **UDP (User Datagram Protocol)**
* **TCP (Transmission Control Protocol)**
* **SCTP (Stream Control Transmission Protocol)**

The experiment demonstrates process-to-process communication and compares each protocol based on:

* Connection establishment
* Data transmission reliability
* Congestion control
* Efficiency

---

# 🧠 2. Learning Outcomes

* Understand transport layer protocol behaviour
* Implement and simulate UDP, TCP, and SCTP
* Compare protocol performance
* Observe packet transmission in Simulation Mode
* Analyze protocol efficiency under varying conditions

---

# 🏗️ 3. Network Topology Design

## 🔹 Devices Used

* 6 PCs / Servers total:

  * PC0 ↔ PC1 → UDP
  * PC2 ↔ PC3 → TCP
  * PC4 ↔ PC5 → SCTP
* 3 Switches
* Optional Router for inter-network communication

---

## 🔹 Logical Structure

```text
UDP Pair:
PC0 ---- Switch0 ---- PC1

TCP Pair:
PC2 ---- Switch1 ---- PC3

SCTP Pair:
PC4 ---- Switch2 ---- PC5
```

---

# 🌐 4. IP Addressing Scheme

| Device | IP Address  | Subnet Mask   |
| ------ | ----------- | ------------- |
| PC0    | 192.168.1.1 | 255.255.255.0 |
| PC1    | 192.168.1.2 | 255.255.255.0 |
| PC2    | 192.168.2.1 | 255.255.255.0 |
| PC3    | 192.168.2.2 | 255.255.255.0 |
| PC4    | 192.168.3.1 | 255.255.255.0 |
| PC5    | 192.168.3.2 | 255.255.255.0 |

---

# 🔌 5. Cabling Structure

* PC ↔ Switch → Copper Straight-Through cable
* Switch ↔ Router (if used) → Copper Straight-Through cable

---

# ⚙️ 6. Protocol Simulations

---

## 🟢 UDP Simulation (`udp_simulation.pkt`)

### Configuration:

* PC0 sends packets to PC1
* Used Command Prompt / Simulation Mode
* No connection establishment
* No acknowledgment
* No retransmission

### Observation:

* Fast transmission
* Lower overhead
* Packet loss possible
* Suitable for streaming or VoIP

---

## 🔵 TCP Simulation (`tcp_simulation.pkt`)

### Configuration:

* PC2 communicates with PC3
* Three-way handshake:

  * SYN
  * SYN-ACK
  * ACK
* Reliable data transfer
* Retransmissions on failure
* Congestion control enabled

### Observation:

* Higher reliability
* Slower than UDP
* Better for web traffic, email, file transfer

---

## 🟣 SCTP Simulation (`sctp_simulation.pkt`)

### Configuration:

* PC4 communicates with PC5
* Multi-stream communication
* Four-way handshake
* Better resilience
* Simulated conceptually due Packet Tracer limitations

### Observation:

* More reliable than TCP in some scenarios
* Supports multi-homing
* Advanced session control

---

# 📊 7. Comparative Analysis

| Feature            | UDP     | TCP             | SCTP            |
| ------------------ | ------- | --------------- | --------------- |
| Connection Setup   | None    | 3-Way Handshake | 4-Way Handshake |
| Reliability        | Low     | High            | Very High       |
| Speed              | Fastest | Moderate        | Moderate        |
| Congestion Control | No      | Yes             | Yes             |
| Error Recovery     | No      | Yes             | Yes             |
| Overhead           | Low     | Medium          | High            |

---

# 🔍 8. Key Findings

### UDP:

* Fastest
* Minimal delay
* Best for real-time applications
* No guaranteed delivery

### TCP:

* Reliable
* Ordered delivery
* Suitable for critical data transfer

### SCTP:

* Advanced transport protocol
* Multi-streaming support
* Better fault tolerance
* Less commonly used in Packet Tracer

---

# 🧪 9. Simulation Steps

## Common Procedure:

1. Build topology
2. Assign IP addresses
3. Verify connectivity using ping
4. Switch to Simulation Mode
5. Generate protocol traffic
6. Observe packet flow
7. Record results

---

# 📸 10. Required Screenshots

* Network topology
* UDP packet flow
* TCP handshake
* SCTP communication
* Successful transmissions

---

# ⚠️ 11. Limitations

* Cisco Packet Tracer has limited SCTP implementation
* SCTP often demonstrated conceptually
* Advanced congestion metrics may require manual analysis

---

# 🚀 12. Improvements

* Simulate larger enterprise networks
* Add routers for WAN scenarios
* Include packet loss testing
* Measure latency under load

---

# 🧾 13. Conclusion

This experiment successfully demonstrated key transport layer protocols and highlighted the strengths and weaknesses of UDP, TCP, and SCTP.

* UDP provides speed
* TCP ensures reliability
* SCTP offers advanced communication features

Each protocol is suited to different networking requirements.

---

# 📁 14. Files Included

* `udp_simulation.pkt`
* `tcp_simulation.pkt`
* `sctp_simulation.pkt`
* `README.md`
* `output.txt`
* `test_cases.txt`

---

# ▶️ 15. How to Run

1. Open corresponding `.pkt` file
2. Verify IP configurations
3. Use Command Prompt / Simulation Mode
4. Observe protocol traffic
5. Capture screenshots
6. Document observations

---

