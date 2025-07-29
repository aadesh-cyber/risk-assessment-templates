# 📄 Policy Risk Assessment Template

This markdown template is designed for evaluating cybersecurity and data governance risks arising from **policy gaps** or outdated practices. It’s ideal for GRC analysts, auditors, compliance teams, or students learning to conduct policy-based risk assessments.

---

## 🎯 Purpose

To identify and assess risks caused by missing, weak, or non-compliant policies — and to suggest remediation strategies aligned with recognized frameworks like ISO 27001, NIST CSF, and PCI DSS.

---

## 📌 Policy Risk Table

| **Policy Area**       | **Identified Gap**                             | **Associated Risk**                        | **Standard Ref**  | **Recommended Mitigation**                                              | **Owner**        | **Target Date** |
| --------------------- | ---------------------------------------------- | ------------------------------------------ | ----------------- | ----------------------------------------------------------------------- | ---------------- | --------------- |
| Acceptable Use Policy | No formal AUP in place for end users           | Inappropriate use of systems, data leakage | ISO 27001 A.5.1.1 | Draft & enforce Acceptable Use Policy                                   | IT Compliance    | 2024-08-30      |
| Data Classification   | No data classification framework               | Sensitive data stored/shared insecurely    | NIST CSF ID.GV-3  | Implement a 3-tier classification policy (Public/Internal/Confidential) | Security Officer | 2024-09-15      |
| Remote Access Policy  | Remote login allowed without MFA               | Unauthorized access to internal systems    | PCI DSS 8.3.1     | Enforce multi-factor authentication (MFA) for all remote access         | Network Admin    | 2024-09-01      |
| Retention Policy      | No record retention or data destruction policy | Legal non-compliance, excess data exposure | GDPR Art. 5(1)(e) | Define retention schedules, integrate auto-deletion scripts             | Data Governance  | 2024-10-01      |
| Vendor Risk Policy    | No third-party security assessment procedure   | Supply chain compromise                    | ISO 27001 A.15.1  | Initiate vendor security questionnaire & onboarding checklist           | Risk Manager     | 2024-08-20      |

---

## 📘 Definitions

* **Policy Area**: General domain where policy is needed (e.g., Access Control, Encryption)
* **Gap**: Missing, outdated, or weak area in current documentation or enforcement
* **Associated Risk**: Threat or consequence resulting from the gap
* **Standard Ref**: Relevant control number from ISO 27001, NIST CSF, PCI DSS, GDPR, etc.
* **Recommended Mitigation**: High-level fix or improvement
* **Owner**: Person/team responsible for implementing control
* **Target Date**: Deadline to resolve or review the risk

---

## 🧩 Tips for Use

* Conduct interviews with IT, HR, legal, and operations to uncover undocumented policies.
* Cross-reference with your regulatory compliance map.
* Prioritize High Risk + High Impact gaps for mitigation.
* Use this file in combination with your Risk Register and Audit Plans.
---

## 🔗 License

Open for educational and non-commercial use. Attribution appreciated.

> Created with 💼 by [Aadesh Kanade](https://github.com/aadeshkanade)
