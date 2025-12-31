# 🛡️ Project: Internal Security Audit & GRC Assessment
**Organization:** Botium Toys  
**Framework:** NIST Cybersecurity Framework (NIST CSF)  
**Risk Score:** 8/10 (High) 

## 📝 Executive Summary
I conducted a comprehensive security audit of Botium Toys' entire security program, including internal networks, systems, and physical assets. The audit identified significant gaps in asset management and regulatory compliance. I developed a prioritized remediation plan to align the organization with **PCI DSS**, **GDPR**, and **SOC** standards, focusing on high-risk areas like unencrypted payment data and lack of access controls.

---

## 🏗️ System Description
Botium Toys is an e-commerce entity with a physical storefront and a global digital presence.
* **Scope:** Internal network, employee equipment (desktops, laptops, smartphones), and management systems (accounting, database, e-commerce).
* **Critical Assets:** Customer PII/SPII, cardholder data, and legacy systems requiring manual monitoring.
* **Current Status:** Firewalls and antivirus are in place, but internal access is unrestricted, and critical data is unencrypted.

---

## 🔍 Audit Findings: Controls & Compliance
Based on my assessment, I identified the following status of critical security controls:

| Control Category | Status | Identified Gap |
| :--- | :---: | :--- |
| **Access Control** | ❌ NO | Lack of Least Privilege and Separation of Duties. |
| **Data Security** | ❌ NO | Customer credit card info (PCI DSS) is not encrypted. |
| **Detection** | ❌ NO | No Intrusion Detection System (IDS) installed. |
| **Recovery** | ❌ NO | No disaster recovery plans or critical data backups. |
| **Physical Security** | ✅ YES | Sufficient locks, CCTV, and fire prevention systems. |

---

## 🛡️ Remediation & Defense-in-Depth Strategy
To improve the security posture from an 8 to a manageable level, I recommended the following NIST CSF-aligned actions:

* **Identify (ID.AM):** Implement a comprehensive asset inventory and classification system.
* **Protect (PR.AC):** Enforce the **Principle of Least Privilege**, implement **MFA**, and establish a centralized password management system.
* **Protect (PR.DS):** Deploy strong encryption for all sensitive data (PII/SPII) at rest and in transit.
* **Detect (DE.CM):** Deploy an **IDS** to monitor network traffic for early threat detection.
* **Recover (RC.RP):** Develop a Disaster Recovery (DR) plan and a regular backup schedule for mission-critical data.


---

## 💡 Key Skills Demonstrated
* **Security Auditing:** Conducted a full-scope audit of assets, controls, and compliance.
* **GRC Proficiency:** Evaluated adherence to **GDPR** (72-hour breach notification) and **PCI DSS** standards.
* **Risk Mitigation:** Translated audit gaps into a prioritized technical roadmap for stakeholders.
* **Framework Application:** Successfully mapped organizational needs to the **NIST CSF** functions.

---

## 📂 Project Assets
For full transparency, the original audit checklists and risk reports can be viewed below:
* 📄 [Scope and Risk Assessment Report (Google Doc)](https://docs.google.com/document/d/1vs6Yeb_HSbyTp0PT6QKBmXwQoS9FjNurLrBEce4d7xE/edit?usp=sharing)
* 📄 [Controls and Compliance Checklist (Google Doc)](https://docs.google.com/document/d/1i5ZqUgB4eB8RTbzN4VsdNPVBtfsh9MLm-Kycf_uBrvU/edit?usp=sharing)
