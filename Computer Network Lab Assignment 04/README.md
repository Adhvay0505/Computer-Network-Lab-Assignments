# README.md

## Experiment 4: Error Detection and Correction using Block Coding and CRC

## 1. Objective

This experiment demonstrates error detection and correction mechanisms in data communication using:

* **Block Coding (Parity Bits)**
* **Cyclic Redundancy Check (CRC)**

A simple communication system was designed in Cisco Packet Tracer to simulate how transmitted data can be checked for corruption, how errors are detected, and how correction mechanisms improve transmission reliability.

---

## 2. Learning Outcomes

* Understand block coding and CRC concepts
* Implement basic error detection and correction in a network simulation
* Simulate data transfer between sender and receiver
* Analyze performance of parity checking and CRC
* Visualize transmission errors in Simulation Mode

---

## 3. Network Topology Design

### Devices Used:

* PC0 (Sender)
* PC1 (Receiver)
* 1 × Switch

### Cabling:

* PC0 → Switch: Copper Straight-Through
* PC1 → Switch: Copper Straight-Through

### IP Configuration:

| Device | IP Address  | Subnet Mask   |
| ------ | ----------- | ------------- |
| PC0    | 192.168.1.1 | 255.255.255.0 |
| PC1    | 192.168.1.2 | 255.255.255.0 |

---

## 4. Simulation Methodology

### Step 1: Basic Communication

* Configured static IP addresses on both PCs
* Verified connectivity using:

```bash
ping 192.168.1.2
```

---

### Step 2: Block Coding Implementation

* Added workspace notes explaining:

  * Data divided into blocks
  * Parity bits appended to each block
  * Single-bit errors can be detected
  * In some cases, corrected

### Simulation:

* Used Add Simple PDU to generate ICMP traffic
* Deleted packets manually in Simulation Mode to simulate bit errors
* Observed retransmission and failure behavior

---

### Step 3: CRC Implementation

* Added workspace notes explaining:

  * Sender generates CRC remainder
  * Receiver recalculates CRC
  * If mismatch occurs → error detected
  * Corrupted frame discarded

### Simulation:

* Introduced packet corruption manually
* Observed detection efficiency
* CRC proved more reliable than parity

---

## 5. Performance Comparison

| Mechanism    | Error Detection | Error Correction | Efficiency | Observation        |
| ------------ | --------------- | ---------------- | ---------- | ------------------ |
| Block Coding | Moderate        | Single-bit       | Medium     | Simple, basic      |
| CRC          | Very High       | Detection only   | High       | Stronger detection |

---

## 6. Key Observations

### Block Coding:

* Detects simple errors
* Can correct limited errors
* Lower overhead
* Less effective for burst errors

### CRC:

* Excellent for error detection
* Detects burst and multiple-bit errors
* Widely used in practical networking
* Requires retransmission for correction

---

## 7. Advantages and Limitations

### Block Coding:

**Advantages**

* Simple
* Easy to implement
* Low complexity

**Limitations**

* Limited correction capability
* Weak against multiple errors

---

### CRC:

**Advantages**

* Strong detection
* Industry standard
* Reliable

**Limitations**

* No direct correction
* Slight computational overhead

---

## 8. How to Run the Simulation

1. Open `error_detection_correction.pkt`
2. Verify PC IP addresses
3. Switch to Simulation Mode
4. Use Add Simple PDU to send packets
5. Delete packets manually to simulate errors
6. Observe:

   * Block Coding notes
   * CRC notes
   * Event List
   * Packet drops/retransmissions

---

## 9. Files Included

* `error_detection_correction.pkt`
* `README.md`
* `output.txt`
* `test_cases.txt`

---

## 10. Assumptions and Design Decisions

* Packet Tracer cannot natively perform CRC mathematics
* Simulation relies on:

  * ICMP traffic
  * Manual packet deletion
  * Conceptual notes
* Simple LAN topology used to isolate protocol behavior

---

## 11. Conclusion

This experiment successfully demonstrated:

* Error detection using block coding
* Advanced error detection using CRC
* Packet corruption simulation
* Reliability improvement in communication systems

### Final Result:

* **CRC** provides stronger detection
* **Block Coding** offers simpler correction
* Both are essential concepts in reliable networking

