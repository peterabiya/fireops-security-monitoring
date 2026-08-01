# FireOps — Security Monitoring Environment

A practical security monitoring project focused on centralized threat detection, endpoint monitoring, network visibility, and incident response within a simulated enterprise environment.

---

## Project Overview

FireOps was developed to simulate an enterprise security monitoring environment comprising Windows endpoints, Ubuntu monitoring servers, and cloud infrastructure. The project centralized security telemetry using Wazuh, OpenSearch, Suricata, AWS CloudTrail, and Tailscale to provide visibility across endpoint, network, and cloud activity.

The monitoring environment leveraged Wazuh as the centralized SIEM platform for log aggregation and threat detection, OpenSearch for log storage and analysis, Wazuh Dashboard for security visualization, and Suricata for network intrusion detection. Secure connectivity between distributed components was established using Tailscale.

To validate the monitoring capabilities, controlled attack simulations—including SSH brute-force attacks, privilege escalation, and network reconnaissance—were performed. Security events were investigated through the Wazuh Dashboard, while incident handling followed the NIST Incident Response Lifecycle with detection workflows aligned to the MITRE ATT&CK framework.

---

## Objectives

- Build a centralized security monitoring environment.
- Collect and analyze security logs from multiple sources.
- Implement endpoint, network, and cloud monitoring.
- Develop and validate security detection rules.
- Simulate common attack scenarios.
- Investigate generated security alerts.
- Apply structured incident response procedures.
- Improve security visibility across the environment.

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Wazuh | SIEM platform, endpoint monitoring, log collection, and threat detection |
| Wazuh Dashboard | Security monitoring, visualization, and alert investigation |
| OpenSearch | Log storage, indexing, and analysis |
| Suricata | Network Intrusion Detection System (NIDS) |
| AWS CloudTrail | Cloud activity monitoring |
| Tailscale | Secure encrypted mesh networking |
| Docker | Containerized deployment of the monitoring stack |
| Ubuntu | Monitoring infrastructure |
| Windows | Monitored endpoint |
| Hydra | SSH brute-force attack simulation |
| Nmap | Network reconnaissance simulation |

---

## What We Implemented

- Deployed a centralized Wazuh SIEM environment using Docker.
- Configured OpenSearch for log indexing, storage, and analysis.
- Integrated Wazuh Dashboard for security monitoring and visualization.
- Connected Windows and Ubuntu systems for centralized endpoint monitoring.
- Integrated Suricata to monitor network traffic and generate intrusion alerts.
- Connected AWS CloudTrail logs for cloud activity monitoring.
- Established secure communication between distributed systems using Tailscale.
- Created custom Wazuh detection rules for:
  - SSH brute-force attacks
  - After-hours login detection
  - Privileged (`sudo`) activity
- Centralized endpoint, network, and cloud telemetry within a single monitoring platform.
- Developed incident response procedures aligned with the NIST Incident Response Lifecycle.

---

## Security Testing

The monitoring environment was validated using controlled attack simulations conducted within an authorized project environment.

### SSH Brute-Force

Hydra was used to simulate repeated SSH authentication attempts against the monitored server. Wazuh successfully detected multiple failed login attempts and generated security alerts for investigation.

### Privilege Escalation

Privilege escalation scenarios were simulated through administrative command execution and `sudo` activity. Wazuh monitored privileged operations and generated alerts for suspicious administrative behavior.

### Network Reconnaissance

Nmap was used to perform TCP SYN port scanning and service enumeration. Suricata detected reconnaissance activity and forwarded network telemetry into Wazuh for centralized analysis.

---

## Incident Response

Security events generated during testing were investigated using a structured incident response process based on the **NIST Incident Response Lifecycle**:

- Preparation
- Identification
- Containment
- Eradication
- Recovery
- Lessons Learned

Detection and response activities were mapped to relevant **MITRE ATT&CK** techniques to support consistent investigation and response procedures.

---

## Key Outcomes

The project demonstrated the ability to:

- Centralize endpoint, network, and cloud security telemetry.
- Aggregate logs from multiple security data sources.
- Monitor endpoint authentication and administrative activity.
- Detect simulated SSH brute-force attacks.
- Detect privilege escalation attempts through `sudo` monitoring.
- Detect network reconnaissance using Suricata.
- Monitor cloud activity through AWS CloudTrail.
- Correlate security events within Wazuh Dashboard.
- Investigate alerts using structured incident response procedures.
- Improve overall visibility across a simulated enterprise environment.

---

## Project Screenshots

The screenshots below were extracted from the original project documentation and illustrate various stages of the deployment, monitoring, threat detection, dashboards, and attack simulations completed during the project.

| | |
|---|---|
| ![](screenshots/screenshot-01.png) | ![](screenshots/screenshot-02.png) |
| ![](screenshots/screenshot-03.png) | ![](screenshots/screenshot-04.png) |
| ![](screenshots/screenshot-05.png) | ![](screenshots/screenshot-06.png) |
| ![](screenshots/screenshot-07.png) | ![](screenshots/screenshot-08.png) |
| ![](screenshots/screenshot-09.png) | ![](screenshots/screenshot-10.png) |
| ![](screenshots/screenshot-11.png) | ![](screenshots/screenshot-12.png) |
| ![](screenshots/screenshot-13.png) | ![](screenshots/screenshot-14.png) |
| ![](screenshots/screenshot-15.png) | ![](screenshots/screenshot-16.png) |
| ![](screenshots/screenshot-17.png) | ![](screenshots/screenshot-18.png) |
| ![](screenshots/screenshot-19.png) | ![](screenshots/screenshot-20.png) |
| ![](screenshots/screenshot-21.png) | ![](screenshots/screenshot-22.png) |
| ![](screenshots/screenshot-23.png) | ![](screenshots/screenshot-24.png) |
| ![](screenshots/screenshot-25.png) | ![](screenshots/screenshot-26.png) |
| ![](screenshots/screenshot-27.png) | ![](screenshots/screenshot-28.png) |
| ![](screenshots/screenshot-29.png) | ![](screenshots/screenshot-30.png) |
| ![](screenshots/screenshot-31.png) | |

> **Note:** These screenshots are presented in the same order as they appear in the original project documentation.

---

## Project Documentation

The complete original project report is included in this repository:

- **[FireOps-Project-Documentation.pdf](FireOps-Project-Documentation.pdf)**

The documentation contains the project architecture, deployment process, configuration steps, threat simulations, detection rules, dashboards, and incident response procedures implemented during the project.

---

## Repository Structure

```text
fireops-security-monitoring/
│
├── README.md
├── screenshots/
|   |── Architecture-Diagram.png
│   ├── screenshot-01.png
│   ├── screenshot-02.png
│   ├── ...
│   └── screenshot-31.png
│
└── FireOps-Project-Documentation.pdf
```

---

## Disclaimer

This project was conducted within a controlled and authorized environment for educational and defensive security purposes.

All attack simulations documented in this repository—including SSH brute-force attacks, privilege escalation, and network reconnaissance—were performed solely to validate security monitoring, threat detection, and incident response capabilities. No unauthorized systems or networks were targeted.
