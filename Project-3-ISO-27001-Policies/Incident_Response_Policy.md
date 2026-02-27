# Incident Response Policy (IRP)

| Attribute | Details |
| :--- | :--- |
| **Reference** | ISO/IEC 27001:2022 Control A.5.24 |
| **Version** | 1.0 |
| **Status** | Approved |
| **Classification** | Internal |

---

## 1. Overview
The purpose of this policy is to establish a consistent and effective approach to managing information security incidents. By defining structured procedures, the organization aims to identify, respond to, and recover from security events while minimizing operational impact and protecting corporate and customer data.

## 2. Incident Classification
Incidents are categorized based on their severity and potential impact on the organization:

| Severity | Criteria |
| :--- | :--- |
| **Low** | Minor policy violations, single-user unsuccessful phishing attempts, or isolated system glitches with no data loss. |
| **Medium** | Malware detected on a single workstation or unauthorized access to non-sensitive internal documentation. |
| **High / Critical** | Confirmed data breach of PII, Ransomware infection, total system/service outage, or compromise of administrative credentials. |

---

## 3. The Incident Response Lifecycle
FinTech-Scale India adheres to the **SANS Framework** for structured incident handling:



1.  **Preparation:** Maintaining the Incident Response Team (IRT), keeping contact lists current, and ensuring monitoring tools are tuned for detection.
2.  **Identification:** Detecting, validating, and triaging the event to determine if it constitutes a security incident.
3.  **Containment:** Limiting the "blast radius" to prevent further damage (e.g., isolating an infected server from the network).
4.  **Eradication:** Identifying and removing the root cause of the threat (e.g., deleting malware, closing exploited ports).
5.  **Recovery:** Restoring systems to normal production operations and verifying the integrity of the environment.
6.  **Lessons Learned:** Conducting a mandatory Post-Incident Review (PIR) to document the event and implement controls to prevent recurrence.

---

## 4. Reporting Obligations
In strict alignment with the **Digital Personal Data Protection (DPDP) Act 2023**:
* **Regulatory Notification:** Any personal data breach must be reported to the Data Protection Board of India within the legally mandated timeframe.
* **Data Principal Notification:** Affected individuals (Data Principals) must be notified of the breach and the remedial steps taken by the organization.
* **Law Enforcement:** Criminal activities, such as ransomware or targeted cyberattacks, must be reported to the relevant authorities (e.g., CERT-In).

---

## 5. Enforcement
All personnel are responsible for the timely reporting of suspected security incidents. Failure to report a known or suspected incident, or attempts to conceal a security breach, may result in disciplinary action up to and including termination of employment or contract.

---
**Developed by Sarthak Suman (RiskVectorX)** *GRC Analyst Portfolio*
