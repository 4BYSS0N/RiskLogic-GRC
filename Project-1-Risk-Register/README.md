# Project 1: Enterprise Risk Register (NIST SP 800-30)

## 🏢 Overview & Business Context
This project demonstrates the application of **NIST Special Publication 800-30 Revision 1** to a fictional mid-sized e-commerce company, **ShopLogic India** (Retail/Fintech). 

The primary objective was to transition the organization from a reactive security posture to a proactive, risk-based approach, focusing on three critical areas:
* **Customer Data Management**
* **Payment Processing**
* **Cloud Infrastructure**

---

## 🛠️ Methodology
Risk was calculated qualitatively using a $3 \times 3$ matrix focused on two primary variables:

1.  **Likelihood:** The probability of a threat source successfully exploiting a known vulnerability.
2.  **Impact:** The magnitude of harm (Financial, Reputational, and Regulatory).

### Risk Calculation Formula
$$Inherent Risk = Likelihood \times Impact$$

### Qualitative Risk Matrix
| Likelihood / Impact | Low (1) | Medium (2) | High (3) |
| :--- | :---: | :---: | :---: |
| **High (3)** | 3 (M) | 6 (H) | 9 (C) |
| **Medium (2)** | 2 (L) | 4 (M) | 6 (H) |
| **Low (1)** | 1 (L) | 2 (L) | 3 (M) |

---

## 📊 Enterprise Risk Register (Extract)
*This extract highlights the top-priority risks identified during the assessment.*

| Risk ID | Asset | Vulnerability | Inherent Score | Mitigation Control (Proposed) | Residual Score |
| :--- | :--- | :--- | :---: | :--- | :---: |
| **RR-001** | Customer PII DB | Lack of MFA | 9 (C) | Implement FIDO2 MFA & JIT Access | 2 (L) |
| **RR-002** | Payment Gateway | Unpatched API | 6 (H) | Monthly Patch Cycle & WAF Deployment | 3 (M) |
| **RR-003** | Cloud S3 Buckets | Public Access | 6 (H) | Automated Config Drift Monitoring | 2 (L) |
| **RR-004** | Staff Laptops | No Encryption | 4 (M) | Full Disk Encryption (FDE) via MDM | 1 (L) |
| **RR-005** | Prod Server | No Backups | 6 (H) | 3-2-1 Backup Strategy (Immutable) | 2 (L) |

---

## 🔍 Critical Findings & Remediation Impact
The assessment identified that **Customer PII Storage** carried the highest inherent risk (Score: 9) due to the absence of Multi-Factor Authentication (MFA) and granular access controls. 

By proposing the implementation of **phishing-resistant MFA** and **Just-In-Time (JIT) access**, the calculated Residual Risk was successfully reduced from **9 (Critical)** to **2 (Low)**.

---

## ⚖️ Regulatory Alignment: India DPDP Act 2023
A significant driver for this assessment was ensuring compliance with the **Digital Personal Data Protection (DPDP) Act 2023**:

* **Section 8 (Breach Prevention):** RR-001 and RR-003 address the legal requirement for "reasonable security safeguards" to prevent personal data breaches.
* **Section 9 (Children's Data):** Mitigation plans include age-verification controls to ensure heightened protection for minor data principals.

---

## 🚀 Live Interactive Visualization
[**View Interactive Risk Dashboard**](https://RiskVectorX.github.io/RiskLogic-GRC/)  


---

## 📂 Key Artifacts in this Folder
* `Risk_Register_ShopLogic.xlsx`: A comprehensive assessment sheet featuring threat sources, vulnerabilities, and an automated "Heat Map" scoring system.
* `Enterprise_Risk_Infographic.html`: An interactive SPA dashboard developed to communicate risk data effectively to executive stakeholders.
* `README.md`: This documentation.

---
**Developed by Sarthak Suman** *GRC Analyst Portfolio*
