# DPDP Act 2023 Gap Analysis Report: ShopLogic India

**Date:** 2026-02-27  
**Auditor:** Sarthak Suman (GRC Analyst)  
**Scope:** Customer Data Lifecycle  

---

## 1. Gap Analysis Table

| DPDP Clause | Legal Requirement | Current Status | Observation / Gap | Recommended Action |
| :--- | :--- | :--- | :--- | :--- |
| **Section 6** | **Notice:** Notice must be provided in English or any of the 22 languages specified in the 8th Schedule. | Partial | Privacy notice is only available in English; violates multilingual requirements. | Implement a language toggle for the Privacy Notice in 22 regional languages. |
| **Section 6** | **Consent:** Consent must be free, specific, informed, unconditional, and unambiguous. | Non-Compliant | ShopLogic uses "Pre-ticked boxes" for marketing consent. | Redesign UI to use "Opt-in" instead of "Opt-out" mechanisms. |
| **Section 9** | **Children's Data:** Verifiable parental consent required for processing data of users under 18. | Non-Compliant | No verifiable age-gate or parental consent flow exists. | Integrate ZKP-based Age Verification or a govt-ID-linked parental consent flow. |
| **Section 10** | **SDF Obligations:** Appoint a Data Protection Officer (DPO) and an Independent Data Auditor. | Non-Compliant | High volume of data suggests SDF status, but no DPO has been appointed. | Formally appoint an India-based DPO and schedule an independent audit. |
| **Section 12** | **Right to Erasure:** Data must be deleted once the purpose is fulfilled or consent is withdrawn. | Partial | Data is retained indefinitely for "analytics." | Implement a Data Retention Policy and automated deletion scripts. |

---

## 2. Executive Summary of Gaps
The audit identified three **Critical** gaps (Notice, Children's Data, and SDF Status) that pose a high risk of financial penalty. The organization is currently processing data of minors without verifiable consent, which is a direct violation of Section 9. Failure to appoint a Data Protection Officer (DPO) further complicates the organization's ability to demonstrate accountability to the Data Protection Board of India.



---

## 3. Remediation Roadmap (Next 6 Months)

### Phase 1: Foundational Compliance (Months 1-2)
* Update Privacy Notice to support 22 regional languages.
* Overhaul Consent Architecture to ensure "Opt-in" mechanisms are the default across all digital touchpoints.

### Phase 2: Technical Integration (Months 3-4)
* Deploy a **Consent Manager** portal to allow Data Principals to manage or withdraw consent in real-time.
* Integrate age-verification controls for minor data principals.
* Formally establish the DPO office and internal reporting lines for personal data breaches.

### Phase 3: Automation and Audit (Months 5-6)
* Implement automated "Right to Erasure" (Right to be Forgotten) workflows to handle data deletion requests at scale.
* Conduct a pre-audit dry run to ensure all remediation efforts meet the SDF requirements under Section 10.



---

*Note: This report is a simulation based on the Digital Personal Data Protection Act, 2023.*

---
**Developed by Sarthak Suman (RiskVectorX)** *GRC Analyst Portfolio*
