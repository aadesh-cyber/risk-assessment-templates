# 🔍 Threat-Risk Mapping Template

**Author**: Aadesh Kanade
**Purpose**: To help GRC professionals and security teams connect organizational **assets**, **threat actors**, **vulnerabilities**, and **controls** in a structured, MITRE-aligned format.

---

## 🎯 Objective

This document supports:

* Threat modeling
* Risk identification workshops
* Security assessments aligned to frameworks (ISO 27005, NIST 800-30, MITRE ATT\&CK)

---

## 📌 Threat-Risk Map Table

| **Asset**          | **Threat Actor**      | **Threat Scenario**                     | **Vulnerability**                | **Potential Impact**              | **Mitigation / Controls**                      |
| ------------------ | --------------------- | --------------------------------------- | -------------------------------- | --------------------------------- | ---------------------------------------------- |
| Web Application    | External Hacker       | Exploits input field for SQL injection  | Lack of input sanitization       | Data theft, unauthorized access   | Input validation, WAF, secure coding practices |
| Workstation        | Insider (Malicious)   | USB exfiltration of sensitive data      | No DLP or USB blocking           | IP theft, compliance violation    | Endpoint protection, DLP, user training        |
| Cloud Storage (S3) | External Threat Actor | Public misconfiguration exposure        | Misconfigured access permissions | Data leakage, reputational damage | IAM hardening, S3 bucket policy review         |
| Email System       | Phishing Attacker     | Credential harvesting via phishing link | No SPF/DMARC or user awareness   | Account compromise                | Email filters, security awareness, MFA         |
| HR Database        | Nation-State APT      | Credential reuse & lateral movement     | Weak password policy             | Long-term undetected access       | MFA, strong password policy, EDR alerts        |

---

## 📘 Field Descriptions

* **Asset**: IT or business system at risk (e.g., database, email, server)
* **Threat Actor**: Who may exploit the asset (external, insider, APT)
* **Threat Scenario**: How the attack might occur
* **Vulnerability**: Weakness in system/process that can be exploited
* **Impact**: Likely business or operational consequence
* **Controls**: Mitigation strategies aligned to best practices

---

## 🎯 MITRE ATT\&CK Mapping (Optional Add-on)

| **Technique**                     | **ID**    | **Applicable Asset** |
| --------------------------------- | --------- | -------------------- |
| Spear Phishing Link               | T1566.002 | Email System         |
| Exploit Public-Facing Application | T1190     | Web Application      |
| Valid Accounts                    | T1078     | HR Database          |
| Command and Scripting Interpreter | T1059     | Workstation          |
| Cloud Storage Object Discovery    | T1619     | Cloud Storage (S3)   |

---

## 🧩 Usage Notes

* Use during tabletop exercises or as part of ISO 27005 risk process
* Can be exported to Excel, visualized in Lucidchart/Miro
* Regularly update based on vulnerability scans and threat intel

---

> 📌 *This document is part of the `risk-assessment-templates` portfolio by [Aadesh Kanade](https://github.com/aadeshkanade). Educational use encouraged.*
