# 🇬🇧 UK Cyber Business Impact Level (CBIL) Report

This template provides a structured Cyber Business Impact Level (CBIL) assessment aligned with **UK NCSC guidelines**, the **NIS Regulations 2018**, **UK GDPR**, and **ISO 22301 / ISO 27005**. It is designed for GRC professionals, security analysts, and compliance teams operating within UK-regulated environments.

---

## 📋 Assessment Details

| Field                    | Details                              |
| ------------------------ | ------------------------------------ |
| **Organisation Name**    | [Enter Organisation Name]            |
| **Assessment Lead**      | [Name / Role]                        |
| **Review Date**          | [DD/MM/YYYY]                         |
| **Next Review Date**     | [DD/MM/YYYY]                         |
| **Classification**       | OFFICIAL / OFFICIAL-SENSITIVE        |
| **Regulatory Scope**     | UK GDPR / NIS / FCA / PCI DSS / Other |
| **Framework Alignment**  | NCSC CAF / ISO 27005 / ISO 22301     |

---

## 🏢 Organisation Overview

| Field                       | Details                            |
| --------------------------- | ---------------------------------- |
| **Sector**                  | [Finance / Health / CNI / Other]   |
| **Organisation Size**       | [SME / Mid-size / Enterprise]      |
| **Critical Functions**      | [List key business functions]      |
| **Data Processed**          | [PII / Financial / Health / Other] |
| **Regulatory Body**         | [FCA / ICO / CQC / Ofcom / Other]  |

---

## 📊 CBIL Classification Scale

The Cyber Business Impact Level (CBIL) is a 1–5 ordinal scale used to categorise the severity of a cyber incident's business impact.

| **CBIL Level** | **Label**    | **Description**                                                                   |
| -------------- | ------------ | --------------------------------------------------------------------------------- |
| **1**          | Negligible   | Minimal disruption. No regulatory breach. Fully recoverable within hours.         |
| **2**          | Low          | Minor service degradation. Limited data exposure. Recoverable within 1–2 days.   |
| **3**          | Moderate     | Significant disruption. Possible regulatory notification required. 2–7 days RTO. |
| **4**          | High         | Major operational failure. Likely regulatory breach. Financial/reputational harm. |
| **5**          | Critical     | Organisation-wide impact. Loss of critical infrastructure. Existential risk.      |

---

## 🎯 Critical Function Impact Assessment

For each critical business function, assess the impact of a cyber disruption across four dimensions.

| **Business Function**   | **Financial Impact** | **Reputational Impact** | **Operational Impact** | **Legal / Regulatory Impact** | **Assigned CBIL** |
| ----------------------- | -------------------- | ----------------------- | ---------------------- | ----------------------------- | ----------------- |
| Customer Data Processing | High                | High                   | Medium                 | High (UK GDPR Art. 33)        | 4                 |
| Payment Systems          | Critical            | High                   | High                   | High (PCI DSS)                | 5                 |
| Internal IT Services     | Low                 | Low                    | Medium                 | Low                           | 2                 |
| Remote Access / VPN      | Medium              | Medium                 | High                   | Medium                        | 3                 |
| [Add Function]           |                     |                        |                        |                               |                   |

---

## 🔑 Key Assets & Dependency Mapping

| **Asset**               | **Type**             | **Owner**          | **CBIL Dependency** | **Single Point of Failure?** |
| ----------------------- | -------------------- | ------------------ | ------------------- | ---------------------------- |
| Customer Database        | Data                | IT / Data Team     | 4                   | Yes                          |
| Payment Gateway          | System              | Finance / IT       | 5                   | Yes                          |
| Active Directory / IdP   | Identity            | IT Security        | 4                   | Yes                          |
| Cloud Storage (S3/Azure) | Infrastructure      | Cloud Team         | 3                   | No                           |
| [Add Asset]              |                     |                    |                     |                              |

---

## ⏱️ Recovery Objectives

| **Business Function**    | **RTO (Recovery Time Objective)** | **RPO (Recovery Point Objective)** | **Current Capability** | **Gap?** |
| ------------------------ | --------------------------------- | ---------------------------------- | ---------------------- | -------- |
| Customer Data Processing | 4 hours                           | 1 hour                             | 8 hours                | Yes      |
| Payment Systems          | 1 hour                            | 15 minutes                         | 2 hours                | Yes      |
| Internal IT Services     | 24 hours                          | 4 hours                            | 24 hours               | No       |
| Remote Access / VPN      | 2 hours                           | N/A                                | 2 hours                | No       |
| [Add Function]           |                                   |                                    |                        |          |

---

## ⚠️ Cyber Threat Scenarios

| **Scenario**              | **Threat Actor**          | **Attack Vector**       | **Likely CBIL** | **Probability** | **Priority** |
| ------------------------- | ------------------------- | ----------------------- | --------------- | --------------- | ------------ |
| Ransomware Attack          | Cybercriminal Group       | Phishing / RDP          | 5               | High            | Critical     |
| Data Exfiltration          | Nation-State / Insider    | Credential Abuse        | 4               | Medium          | High         |
| DDoS on Web Services       | Hacktivist / Criminal     | Volumetric Attack       | 3               | Medium          | Medium       |
| Supply Chain Compromise    | APT / Cybercriminal       | Third-party Software    | 4               | Low             | High         |
| Insider Data Theft         | Malicious Insider         | Privileged Access Abuse | 4               | Low             | High         |
| [Add Scenario]             |                           |                         |                 |                 |              |

---

## 🛡️ Control Effectiveness Assessment

| **Control Domain**           | **Control in Place?** | **Effectiveness** | **Gap / Weakness**                        | **Recommended Action**                    |
| ---------------------------- | --------------------- | ----------------- | ----------------------------------------- | ----------------------------------------- |
| Identity & Access Management | Yes                   | Moderate          | MFA not enforced on all accounts          | Enforce MFA org-wide (NCSC guidance)      |
| Patch & Vulnerability Mgmt   | Partial               | Low               | Critical patches >30 days outstanding     | Automate patching; adopt vulnerability SLA|
| Backup & Recovery            | Yes                   | Moderate          | Backups not tested quarterly              | Schedule quarterly DR tests               |
| Incident Response Plan       | Yes                   | Moderate          | Plan not exercised in 12+ months          | Conduct tabletop exercise bi-annually     |
| Network Segmentation         | Partial               | Low               | Flat network; no east-west filtering      | Implement micro-segmentation / VLANs      |
| Third-party Risk Management  | No                    | None              | No supplier security assessments          | Introduce vendor due diligence process    |
| Data Loss Prevention (DLP)   | No                    | None              | No DLP tooling deployed                   | Evaluate DLP solution; enforce policies   |
| Security Awareness Training  | Yes                   | High              | Annual training only                      | Move to quarterly phishing simulations    |

---

## 📏 UK Regulatory Notification Thresholds

| **Regulation**             | **Notification Trigger**                                     | **Deadline**       | **Notify**       |
| -------------------------- | ------------------------------------------------------------ | ------------------ | ---------------- |
| **UK GDPR (Art. 33)**      | Personal data breach likely to result in rights/freedoms risk | 72 hours           | ICO              |
| **NIS Regulations 2018**   | Incident with significant impact on service continuity       | Without undue delay| Competent Authority (NCSC/Ofcom etc.) |
| **FCA (SYSC 15A)**         | Operational or security incident of material impact          | ASAP / as required | FCA              |
| **PCI DSS v4.0**           | Suspected or confirmed cardholder data compromise            | Immediately        | Card Brands / Acquirer |
| **NHS DSP Toolkit**        | Serious incident involving patient data                      | 72 hours           | ICO / DSPT       |

---

## 📈 Overall Organisational CBIL Rating

| **Assessment Dimension**    | **Score (1–5)** | **Notes**                                    |
| --------------------------- | --------------- | -------------------------------------------- |
| Financial Impact             | [1–5]          | Estimated loss if critical function disrupted|
| Reputational Impact          | [1–5]          | Media, customer, and stakeholder exposure    |
| Operational Impact           | [1–5]          | Duration and breadth of service disruption   |
| Legal / Regulatory Impact    | [1–5]          | Regulatory breach, fines, enforcement risk   |
| **Composite CBIL Score**     | **[1–5]**      | Average or highest-dimension score           |

**Composite Scoring Method**: Use the highest individual dimension score OR average across all four.

---

## 🗺️ Risk Treatment Plan

| **Risk / Gap**                  | **CBIL Level** | **Treatment Option**    | **Owner**      | **Target Date** | **Status**   |
| ------------------------------- | -------------- | ----------------------- | -------------- | --------------- | ------------ |
| MFA not enforced org-wide       | 4              | Mitigate                | IT Security    | [DD/MM/YYYY]    | In Progress  |
| No DR test conducted in 12m     | 4              | Mitigate                | CISO / IT Ops  | [DD/MM/YYYY]    | Planned      |
| No third-party risk assessments | 3              | Mitigate                | Procurement    | [DD/MM/YYYY]    | Not Started  |
| DLP tooling absent              | 3              | Mitigate / Transfer     | IT Security    | [DD/MM/YYYY]    | Not Started  |
| Legacy systems without patches  | 5              | Mitigate / Accept       | IT / Board     | [DD/MM/YYYY]    | Escalated    |
| [Add Risk]                      |                |                         |                |                 |              |

---

## ✅ Executive Summary

| Field                            | Details                                                          |
| -------------------------------- | ---------------------------------------------------------------- |
| **Overall CBIL Rating**          | [1–5] – [Label: Negligible / Low / Moderate / High / Critical]   |
| **Highest Risk Function**        | [e.g. Payment Systems – CBIL 5]                                  |
| **Key Findings**                 | [Summary of top 3–5 findings]                                    |
| **Immediate Actions Required**   | [List critical remediation items]                                |
| **Regulatory Notification Needed?** | Yes / No / Under Review                                       |
| **Board Escalation Required?**   | Yes / No                                                         |
| **Assessment Status**            | Draft / Under Review / Final                                     |

---

## 📘 Glossary

| **Term**    | **Definition**                                                                              |
| ----------- | ------------------------------------------------------------------------------------------- |
| **CBIL**    | Cyber Business Impact Level — a 1–5 scale classifying business impact severity from a cyber event. |
| **RTO**     | Recovery Time Objective — maximum acceptable downtime for a business function.              |
| **RPO**     | Recovery Point Objective — maximum acceptable data loss measured in time.                   |
| **NCSC**    | National Cyber Security Centre — UK government body providing cyber security guidance.      |
| **NIS**     | Network and Information Systems Regulations 2018 — UK law mandating security for essential services. |
| **UK GDPR** | UK General Data Protection Regulation — UK data protection law post-Brexit.                 |
| **FCA**     | Financial Conduct Authority — UK financial services regulator.                              |
| **CAF**     | Cyber Assessment Framework — NCSC framework for assessing cyber resilience of critical infrastructure. |
| **ICO**     | Information Commissioner's Office — UK data protection supervisory authority.               |
| **APT**     | Advanced Persistent Threat — sophisticated, long-term cyber attacker (often nation-state).  |

---

## 🔗 Reference Frameworks

- [NCSC Cyber Assessment Framework (CAF)](https://www.ncsc.gov.uk/collection/cyber-assessment-framework)
- [NCSC 10 Steps to Cyber Security](https://www.ncsc.gov.uk/collection/10-steps)
- [UK GDPR – ICO Guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/)
- [NIS Regulations 2018](https://www.legislation.gov.uk/uksi/2018/506/contents)
- [ISO/IEC 27005:2022 – Information Security Risk Management](https://www.iso.org/standard/80585.html)
- [ISO 22301:2019 – Business Continuity Management](https://www.iso.org/standard/75106.html)

---

## 📄 Document Control

| **Version** | **Date**       | **Author**       | **Changes**         |
| ----------- | -------------- | ---------------- | ------------------- |
| 1.0         | [DD/MM/YYYY]   | [Name]           | Initial draft       |
| 1.1         | [DD/MM/YYYY]   | [Name]           | [Change description]|

---

> Template maintained by [Aadesh Kanade](https://github.com/aadesh-cyber) – Cybersecurity Graduate | GRC & Risk Management Enthusiast  
> Open for educational and non-commercial use. Attribution appreciated.
