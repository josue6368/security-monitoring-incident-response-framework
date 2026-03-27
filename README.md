# SIEM-based threat detection and incident response framework for a streaming platform environment

## Overview

This project demonstrates the design and implementation of a security monitoring and incident response framework for a large-scale streaming platform environment. The goal of this project was to improve visibility into system activity, detect malicious behavior, and establish structured response procedures aligned with industry standards.

This project was completed as part of a cybersecurity capstone at Western Governors University and simulates real-world attack scenarios commonly targeting cloud-based streaming platforms.


## Problem Statement

Modern streaming platforms rely on distributed cloud infrastructure, APIs, and authentication systems, making them prime targets for cyber threats such as:

  - Credential stuffing and account takeover
  - API abuse and automation attacks
  - Lateral movement within internal networks

Many organizations lack centralized logging and incident response processes, resulting in delayed detection and increased risk of compromise.

## Solution

To address these challenges, I designed a SIEM-based security monitoring and incident response framework that includes:

  - Centralized log aggregation (authentication logs, API logs, network traffic)
  - Detection rules for identifying malicious activity
  - MITRE ATT&CK mapping for adversary behavior
  - Incident response playbooks aligned with NIST 800-61

## Technologies and Tools

  - SIEM concepts (log aggregation & correlation)
  - MITRE ATT&CK Framework
  - NIST 800-61 Incident Response
  - Wireshark (network analysis)
  - Nmap (reconnaissance simulation)


## Attack Scenarios Samples

1. Credential Stuffing / Account Takeover
   - Multiple failed login attempts from a single IP
   - Successful login from a new geographic location
2. API Abuse
   - Excessive API requests exceeding normal thresholds
   - Automated behavior patterns
3. Lateral Movement
   - Suspicious internal SMB connections
   - Privilege escalation attempts

## Sample SIEM Log Output

| Timestamp           | Event Type           | User   | Source IP    | Description                                  |
| ------------------- | -------------------- | ------ | ------------ | -------------------------------------------- |
| 2026-03-25 10:15:22 | Failed Login         | jsmith | 192.168.1.10 | Failed login attempt detected                |
| 2026-03-25 10:15:30 | Failed Login         | jsmith | 192.168.1.10 | Repeated failed login attempts               |
| 2026-03-25 11:02:10 | Successful Login     | jsmith | 203.45.88.12 | Login from new/unrecognized location         |
| 2026-03-25 11:05:44 | API Anomaly          | N/A    | 203.45.88.12 | API rate exceeded threshold                  |
| 2026-03-25 11:10:33 | Lateral Movement     | jsmith | 10.0.0.15    | Suspicious SMB connection to internal system |
| 2026-03-25 11:12:47 | Privilege Escalation | jsmith | 10.0.0.15    | Attempt to elevate privileges detected       |

## Incident Response Playbook (Summary)

Identification  
  - Detect abnormal login activity and API anomalies
  - Analyze SIEM alerts and logs

Containment  
  - Disable compromised accounts
  - Block malicious IP addresses

Eradication  
  - Reset credentials
  - Remove unauthorized sessions

Recovery  
  - Restore account access securely
  - Monitor for recurring threats

Lessons Learned  
  - Update detection rules
  - Recommend MFA and stronger control


## Key Takeaways

  - Centralized logging significantly improves detection capabilities
  - MITRE ATT&CK provides structured visibility into attacker behavior
  - SIEM correlation enables faster and more accurate threat identification
  - Incident response playbooks improve consistency and reduce response time

## Future Improvements

  - Integration with real SIEM platforms (Splunk, Elastic)
  - Automated alerting and response workflows
  - Implementation of multi-factor authentication (MFA)
  - Cloud-native security controls and monitoring



### Author
josue6368  
Cybersecurity Analyst | IT Professional
 

