# 🧾 Simple Risk Register

This document provides a basic cybersecurity risk register in markdown format ideal for student labs, GRC analyst practice, or policy documentation.

It includes practical examples, a scoring matrix, and key definitions to help you perform qualitative risk assessments aligned with ISO 27001, NIST CSF, and other frameworks.

---

## 🧭 Step-by-Step Risk Assessment Flow

1. **Identify critical assets** (data, systems, apps)
2. **Map threats & vulnerabilities** related to those assets
3. **Score likelihood and impact** (1–5 scale)
4. **Calculate risk score** (Likelihood × Impact)
5. **Apply controls** to reduce the risk
6. **Evaluate residual risk** after controls

---

## 🔍 Asset Identification Guide

A few asset categories to consider:

* **Web applications** (e.g. login portals, admin panels)
* **Databases** (user data, financial records)
* **Servers** (API backend, file servers)
* **User credentials** (employees, customers)
* **Endpoints** (workstations, mobile devices)

---

## 🔗 Threat & Vulnerability Mapping

* **Threats**: SQL injection, malware, phishing, insider abuse, data theft
* **Vulnerabilities**: Unpatched software, misconfigured access, poor password hygiene, lack of logging

Use threat intelligence (e.g. MITRE ATT\&CK, OWASP Top 10) to build your list.

---

## 📌 Risk Table

| **Asset**        | **Threat**       | **Vulnerability**     | **Likelihood (1-5)** | **Impact (1-5)** | **Risk Score (L×I)** | **Controls**                       | **Residual Risk** |
| ---------------- | ---------------- | --------------------- | -------------------- | ---------------- | -------------------- | ---------------------------------- | ----------------- |
| Web Application  | SQL Injection    | Unpatched Input Field | 4                    | 5                | 20                   | Input validation, WAF rules        | Medium            |
| Database Server  | Data Breach      | Unencrypted Storage   | 3                    | 5                | 15                   | Encryption at rest, access control | Low               |
| User Credentials | Credential Theft | Weak Password Policy  | 5                    | 4                | 20                   | Enforce MFA, password complexity   | Medium            |

---

## 🧮 Risk Scoring Matrix

| **Likelihood ↓ / Impact →** | 1 (Low) | 2  | 3  | 4  | 5 (High) |
| --------------------------- | ------- | -- | -- | -- | -------- |
| **1 (Rare)**                | 1       | 2  | 3  | 4  | 5        |
| **2 (Unlikely)**            | 2       | 4  | 6  | 8  | 10       |
| **3 (Possible)**            | 3       | 6  | 9  | 12 | 15       |
| **4 (Likely)**              | 4       | 8  | 12 | 16 | 20       |
| **5 (Very Likely)**         | 5       | 10 | 15 | 20 | 25       |

* **Low Risk**: 1–6
* **Medium Risk**: 7–14
* **High Risk**: 15–25

---

## 💡 Control Recommendations by Risk Type

| **Risk Category** | **Suggested Controls**                                    |
| ----------------- | --------------------------------------------------------- |
| Web App Risk      | Input validation, WAF, secure coding guidelines           |
| Data Protection   | Encryption, role-based access control, backups            |
| Identity Theft    | MFA, password policy, SSO monitoring                      |
| Insider Risk      | Least privilege, user activity logging, background checks |

---

## 📘 Definitions

* **Asset**: The IT resource or system under assessment.
* **Threat**: A potential event or attacker causing harm (e.g. hacker, malware).
* **Vulnerability**: A weakness that could be exploited (e.g. poor patching).
* **Likelihood**: Probability of the threat exploiting the vulnerability (1 = Rare, 5 = Very Likely).
* **Impact**: Potential severity of the impact if exploited (1 = Negligible, 5 = Critical).
* **Risk Score**: Product of Likelihood × Impact. Helps prioritize response.
* **Controls**: Measures taken to reduce risk (technical or administrative).
* **Residual Risk**: The risk level that remains after applying controls.

---

## 🎯 Interpreting Residual Risk

After applying controls, reassess the likelihood and impact. If the **residual risk** is still Medium or High:

* Consider **additional layered defenses**
* Flag the risk for **management approval or exception**
* Document risk acceptance and mitigation plan

---

## 🔗 License

Open for educational and non-commercial use. Attribution appreciated.

> Created with ❤️ by [Aadesh Kanade](https://github.com/aadeshkanade)
