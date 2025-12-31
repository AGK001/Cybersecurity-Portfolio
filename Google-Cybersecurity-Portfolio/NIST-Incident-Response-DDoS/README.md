# 🛡️ Project: Incident Response using NIST CSF
**Incident Type:** Distributed Denial of Service (DDoS)
**Framework:** NIST Cybersecurity Framework (CSF)
**Duration of Attack:** 2 Hours

## 📝 Executive Summary
In this project, I analyzed and responded to a two-hour DDoS attack that compromised an organization's internal network. The attack utilized a flood of ICMP packets to render network services unresponsive. By applying the five core functions of the **NIST Cybersecurity Framework**, I identified the root cause - an unconfigured firewall, and implemented a defense-in-depth strategy to mitigate future risks.

---

## 🏗️ Incident Overview
* **The Problem:** A malicious actor exploited a firewall vulnerability to flood the network with ICMP pings.
* **The Impact:** Network services became unresponsive, halting internal operations for the duration of the attack.
* **The Goal:** Contain the incident, restore services, and harden the network against similar ICMP-based attacks.

---

## 🔍 NIST CSF Incident Analysis
Using the NIST CSF functions, I documented the following response lifecycle:

| Function | Action Taken |
| :--- | :--- |
| **Identify** | Detected security gaps: unconfigured firewall (no ICMP filtering), lack of source IP verification, and absence of an IDS/IPS. |
| **Protect** | Implemented rate-limiting for ICMP packets, enabled source IP verification, and installed an IDS/IPS to filter suspicious traffic. |
| **Detect** | Established real-time network monitoring and alert systems configured to flag specific ICMP attack signatures. |
| **Respond** | Blocked incoming ICMP packets to stop the attack, isolated non-critical services, and restored core network functionality. |
| **Recover** | Verified critical service functionality, tested system performance for stability, and documented the full restoration process. |

---

## 🛡️ Remediation & Post-Incident Improvements
To prevent a recurrence, I recommended and implemented the following technical controls:
1. **Firewall Hardening:** Configured strict rules to limit the rate of ICMP traffic.
2. **Network Visibility:** Deployed monitoring software to detect abnormal traffic patterns in real-time.
3. **Automated Defense:** Installed an **IDS/IPS system** specifically tuned to intercept and block malicious ICMP floods.
4. **Validation:** Established a schedule for regular security audits and staff training on incident response procedures.

---

## 💡 Key Skills Demonstrated
* **Incident Response:** Managed the full lifecycle of a network attack from detection to recovery.
* **Technical Troubleshooting:** Identified specific firewall misconfigurations and ICMP protocol vulnerabilities.
* **NIST CSF Application:** Translated theoretical framework functions into practical technical actions.
* **Network Security:** Implemented rate-limiting, IP verification, and IDS/IPS filtering.

---

## 📂 Project Assets
For a detailed breakdown of the technical response and framework application, see the documents below:
* 📄 [Incident Report Analysis (Google Doc)](https://docs.google.com/document/d/1dzHxg470CD4jNGJzNJ-0uhCf502shhNi387JraInNvI/edit?usp=sharing)
* 📄 [Applying the NIST CSF Reference (Google Doc)](https://docs.google.com/document/d/14crrxHUoX_RX6Klq7uNck2CsLQ5ABmq6EWafpZPEznA/edit?usp=sharing)
