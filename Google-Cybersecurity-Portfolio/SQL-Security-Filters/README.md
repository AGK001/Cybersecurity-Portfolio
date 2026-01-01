# 🛡️ Project: SQL Security Auditing & Data Filtering

**Language:** SQL (MariaDB)                     
**Focus:** Incident Investigation & User Access Auditing

## 📝 Executive Summary
As a cybersecurity analyst, I utilized SQL to audit an organization's database containing employee information and system login records. My objective was to investigate potential security threats - such as unauthorized after-hours access and geographical anomalies, and to identify specific employee groups for critical security updates. By applying advanced filtering logic, I streamlined the process of identifying vulnerabilities and ensuring organizational compliance.

---

## 🏗️ Database Environment
The investigation involved querying two primary tables within the organizational database:
* **`log_in_attempts`:** Tracks Every login event, including timestamps, geographical location (country), IP addresses, and success/failure status.
* **`employees`:** Contains organizational data, including department names, office locations, and device IDs.

---

## 🔍 Security Analysis Matrix
I executed the following queries to extract actionable security intelligence:

| Investigation Scenario | SQL Filtering Logic | Security Purpose |
| :--- | :--- | :--- |
| **After-Hours Failed Logins** | `WHERE login_time > '18:00:00' AND success = FALSE` | Identifying potential brute-force or unauthorized access attempts outside business hours. |
| **Suspicious Date Audit** | `WHERE login_date = '2022-05-09' OR login_date = '2022-05-08'` | Correlating login patterns with a known security event period for forensic analysis. |
| **Geographical Anomalies** | `WHERE NOT country LIKE 'MEX%'` | Detecting logins originating from unauthorized or unexpected international locations. |
| **Sensitive Dept. Audit** | `WHERE department = 'Sales' OR department = 'Finance'` | Auditing access for personnel in high-value departments prone to social engineering. |
| **Patch Management** | `WHERE NOT department = 'Information Technology'` | Identifying machines needing updates while excluding the already-patched IT department. |

---

## 🛡️ Security Insights & Remediation
By translating raw log data into filtered results, I implemented a data-driven security approach:
* **Threat Hunting:** Isolated specific IP addresses and usernames associated with failed after-hours logins for further investigation by the SOC team.
* **Attack Surface Reduction:** Identified "Impossible Travel" scenarios by filtering out authorized countries, pointing toward potential credential compromise.
* **Operational Efficiency:** Accelerated the deployment of security patches by providing the IT department with a clean list of targeted employees, preventing redundant work.

---

## 💡 Key Skills Demonstrated
* **Database Auditing:** Proficiency in querying relational databases to monitor user activity.
* **SQL Filtering:** Advanced use of `WHERE` clauses combined with `AND`, `OR`, `NOT`, and `LIKE` operators.
* **Log Analysis:** Ability to interpret system logs to identify suspicious behavior and security gaps.
* **Asset Management:** Using data to identify and categorize hardware/software assets for organizational updates.

---

## 📂 Project Assets
For full transparency, the original planning and reporting documents can be viewed via the links below:
* 📄 [SQL Filtering Project Report (Google Doc)](https://docs.google.com/document/d/1dvuXpMai1ui_MiYdP_sqtiUF6gSnvak8xqXnnNID5wQ/edit?usp=sharing)
* 📄 [Database Schema & Table Formats (Google Doc)](https://docs.google.com/document/d/1JmjCTP7NXGAgClBoDEv7wP8jxMB9tA8QUSbMSM4Q7q8/edit?usp=sharing)
