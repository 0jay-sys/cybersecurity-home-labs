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


<img width="1358" height="640" alt="image" src="https://github.com/user-attachments/assets/8463bd54-e424-4175-a95a-f66a978a844f" />

> **Analyst Takeaway:** Filtered over 23,000 internal telemetry events using SPL (`index=_internal error OR failed`) to isolate system errors and failed authentication patterns. Identifying spikes in this baseline timeline helps Tier 1 analysts quickly spot brute-force attempts or service failures during a shift.

















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

> **Analyst Takeaway:** Isolated the standard TCP three-way handshake (`SYN` -> `SYN, ACK` -> `ACK`) using the `tcp.flags.syn == 1` display filter. Verifying clean handshake completion is a core NOC/SOC step for confirming legitimate connections and diagnosing network drops.

**2. Unencrypted HTTP POST Stream Analysis**



<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/8c19ce85-c335-45bc-b376-20a67eb19812" />

> **Analyst Takeaway:** Reconstructed an unencrypted HTTP `POST` transmission via Wireshark's TCP Stream viewer, exposing plaintext form data over the wire. This demonstrates the security risk of legacy unencrypted protocols and why enforcing HTTPS/TLS is critical.


**3. ICMP Echo Request/Reply Traffic Baseline (`icmp`)**


<img width="1000" height="685" alt="image" src="https://github.com/user-attachments/assets/0addadb4-f63d-478c-9fd4-75f02184f075" />

> **Analyst Takeaway:** Captured and filtered ICMP Echo Request and Echo Reply packets (`icmp`) to verify round-trip connectivity and response times. Establishing a normal ICMP baseline allows analysts to distinguish standard network troubleshooting from high-volume ping sweeps or reconnaissance scans.


