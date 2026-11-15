# CompTIA Security+ Practical Home Labs
Welcome to my hands-on cybersecurity portfolio. This repository documents the practical implementations and environments I engineered to simulate enterprise Tier 1 SOC, OCC, and NOC environments.

---

## 🧪 Project 1: Enterprise SIEM Log Aggregation & Triage (Wazuh Cloud)
### Objective
To architect a cloud-hosted SIEM environment to securely ingest local endpoint telemetry, analyze system events, and triage live security alerts.

### Environment & Tools
*   **SIEM Platform:** Wazuh Cloud (Enterprise Open-Source SIEM)
*   **Target Endpoint:** Personal Host Machine (Windows)
*   **Log Forwarder:** Lightweight Wazuh Monitoring Agent

### Implementation Steps
1. Deployed an enterprise-ready tenant via the Wazuh Cloud dashboard.
2. Installed and initialized the lightweight monitoring agent locally via administrative terminal commands.
3. Successfully established a secure cryptographic log pipeline forwarding endpoint event logs to the cloud.
4. Simulated a brute-force authentication attack by intentionally generating multiple failed system login events.

### Project Artifacts
*(Paste SIEM Dashboard Alert Screenshot Here)*

---

## 🧪 Project 2: Network Protocol Diagnostics & Deep Packet Analysis (Wireshark)
### Objective
To capture, filter, and perform deep-packet analysis on live network traffic streams to isolate connectivity bottlenecks, audit cleartext credential exposures, and detect reconnaissance patterns.

### Environment & Tools
*   **Packet Analyzer:** Wireshark
*   **Protocols Investigated:** TCP, HTTP, ICMP

### Implementation Steps
1. Initialized a live capture packet stream tracking local network interface metrics.
2. Isolated a standard **TCP 3-Way Handshake** by utilizing custom sequence display filters (`tcp.flags.syn == 1`).
3. Captured an unencrypted **HTTP POST** login transmission to reveal data exposures and cleartext credential vulnerability risks.
4. Audited **ICMP traffic** timestamps to baseline regular network echoes against intense scanning signatures.

### Project Artifacts
*(Paste TCP Handshake Screenshot Here)*
*(Paste HTTP Cleartext Password Screenshot Here)*
<img width="760" height="685" alt="image" src="https://github.com/user-attachments/assets/8c19ce85-c335-45bc-b376-20a67eb19812" />

*(Paste ICMP Ping Screenshot Here)*
