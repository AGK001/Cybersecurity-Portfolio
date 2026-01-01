# 🛡️ Project: Linux File Permissions & Access Control

**System:** Ubuntu Linux  
**Focus:** Authorization & Principle of Least Privilege

## 📝 Executive Summary
In this project, I managed and audited file system security for a research team by reviewing and modifying directory and file permissions. Using the Linux Command Line Interface (CLI), I identified unauthorized access levels and implemented strict authorization controls. My work ensured that sensitive research data; including hidden system files, was only accessible to authorized users, effectively reducing the organization's internal attack surface.

---

## 🏗️ System Environment
The audit focused on the `/home/researcher2/projects` directory, which contains sensitive research files and subdirectories.
* **Primary Tool:** Bash (Linux Terminal).
* **Key Commands:** `ls -la`, `chmod`.
* **Objective:** Remove "World" and "Group" write/execute permissions from sensitive assets.

---

## 🔍 Permission Audit & Deconstruction
I used the `ls -la` command to analyze the 10-character permission strings for all files, including hidden files (e.g., `drwx--x--- .project_x.txt`).

| Character Position | Represents | Meaning |
| :--- | :--- | :--- |
| **1st** | File Type | `d` for Directory, `-` for Regular File. |
| **2nd - 4th** | **User (Owner)** | Read (`r`), Write (`w`), Execute (`x`). |
| **5th - 7th** | **Group** | Read (`r`), Write (`w`), Execute (`x`). |
| **8th - 10th** | **Other (World)** | Read (`r`), Write (`w`), Execute (`x`). |

---

## 🛡️ Remediation & Command History
I identified several security gaps where "Other" users had excessive access. Below are the specific remediation steps taken:

### 1. Hardening File Permissions
* **The Problem:** `project_k.txt` allowed global write access (`-rw-rw-rw-`), and the hidden file `.project_x.txt` had unauthorized group write permissions.
* **The Action:**
    * `chmod o-w project_k.txt` (Removed world write access).
    * `chmod u=r,g=r .project_x.txt` (Reset to read-only for user and group).

### 2. Securing Subdirectories
* **The Problem:** The `drafts` directory allowed group execute permissions, which violated the research team's security policy.
* **The Action:**
    * `chmod g-x drafts` (Removed group execution rights).

---

## 💡 Key Skills Demonstrated
* **System Administration:** Proficient in navigating and managing Linux file systems via CLI.
* **Access Control:** Expertise in translating organizational security policies into technical `chmod` configurations.
* **Attention to Detail:** Ability to identify and secure hidden files (dotfiles) that are often overlooked in manual audits.
* **Security Advocacy:** Implemented the **Principle of Least Privilege** to ensure users only have the minimum access necessary for their roles.

---

## 📂 Project Assets
For a full technical breakdown of the commands used and the permission strings analyzed, see the documents below:
* 📄 [File Permissions in Linux Analysis (Google Doc)](https://docs.google.com/document/d/1NcFcykvSIokbqlqWfUBq11smrja7BpU1TRavqlbpsF4/edit?usp=sharing)
* 📄 [Initial vs. Final Permission Logs (Google Doc)](https://docs.google.com/document/d/1GteoAzqdWrIwZrWvLTLrG4W4dHZK0f4HiH_YGICD7iY/edit?usp=sharing)
