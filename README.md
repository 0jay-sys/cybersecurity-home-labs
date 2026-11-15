# CompTIA Security+ Practical Home Labs
Welcome to my hands-on cybersecurity portfolio. This repository documents the practical implementations and environments I engineered to simulate enterprise Tier 1 SOC, OCC, and NOC environments.

## 🧪 Project 1: Enterprise SIEM Log Aggregation & Triage (Splunk Cloud)
### Objective
To operate a cloud-hosted enterprise SIEM environment to ingest system telemetry, execute Search Processing Language (SPL) queries, and triage security and operational anomalies.

### Environment & Tools
*   **SIEM Platform:** Splunk Cloud Platform
*   **Query Language:** Splunk Search Processing Language (SPL)
*   **Log Sources:** Internal System Telemetry & Authentication Logs

### Implementation Steps
1. Provisioned and administered an enterprise tenant on **Splunk Cloud Platform**.
2. Executed targeted **SPL queries** (`index=_internal error OR failed`) to filter high-volume telemetry streams and isolate system errors and failed authentication events.
3. Analyzed event timeline distributions and raw JSON log payloads to establish baseline anomaly triage workflows.

### Project Artifacts
**1. Splunk Cloud Event Ingestion & SPL Log Triage**


<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/399278c0-e4af-4a9a-bb96-ff914c52860c" />










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
**1. TCP 3-Way Handshake Isolation (`tcp.flags.syn == 1`)**


<img width="1000" height="685" alt="image" src="https://github.com/user-attachments/assets/094afd97-9eb7-4757-9007-d6fc1ff6c120" />

**2. Unencrypted HTTP POST Stream Analysis**



<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/8c19ce85-c335-45bc-b376-20a67eb19812" />

**3. ICMP Echo Request/Reply Traffic Baseline (`icmp`)**


<img width="1000" height="685" alt="image" src="https://github.com/user-attachments/assets/0addadb4-f63d-478c-9fd4-75f02184f075" />

