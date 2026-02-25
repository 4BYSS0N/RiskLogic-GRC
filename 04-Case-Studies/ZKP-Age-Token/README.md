# 🛡️ Privacy-by-Design Architecture: Zero-Knowledge Age Verification
**Category:** Data Privacy Engineering & Regulatory Compliance (GRC)

## 📌 Executive Summary
Traditional Identity and Access Management (IAM) systems often require users to upload sensitive **Personally Identifiable Information (PII)**—such as Aadhaar, driver's licenses, or passports—to verify age. This creates massive "data honeypots," increasing the **Impact of Unauthorized Disclosure** and violating modern data protection frameworks.

This project is a **Proof-of-Concept (PoC)** demonstrating how to achieve technical compliance with **India's DPDP Act (2023)** and the **EU GDPR** using Zero-Knowledge Proofs (zk-SNARKs). It allows a system to cryptographically verify a user is 18+ without ever collecting, transmitting, or storing their actual birth date.

---

## ⚖️ Compliance & Governance Mapping
This architecture is mapped against the following global regulatory requirements:

* **Data Minimization (GDPR Art. 5c / DPDP Act Sec. 8):** The server never receives the user's birth year. By implementing **Data Purging** at the client-side, we ensure that if the "Data Fiduciary" (server) is breached, there is zero PII for threat actors to exfiltrate.
* **Privacy by Design (PbD):** Security is mathematically embedded into the architecture at the foundational level, ensuring "Default Privacy" as per international GRC standards.
* **Stateless Authorization:** Utilizes JSON Web Tokens (JWT) to manage session state securely, reducing the risk of database-level session leakage.

---

## 🏗️ Architectural Data Flow
1.  **Local Computation (Client-Side):** The user inputs their birth year. A WebAssembly (WASM) circuit runs entirely locally in the browser to calculate: `CurrentYear - BirthYear >= 18`.
2.  **Proof Generation:** A zk-SNARK proof is generated locally. The raw PII (birth year) is instantly **purged** from memory.
3.  **Transmission (Data in Transit):** Only the mathematical proof (a randomized cryptographic string) is sent over the network.
4.  **Verification (Server-Side):** The Node.js server mathematically verifies the proof against a trusted public key.
5.  **Token Issuance:** Upon successful verification, the server issues a JWT granting restricted access.

---

## 🕵️‍♂️ Threat Modeling & Risk Remediation
During the design phase, the following risks were identified and actively mitigated:

### 1. Risk: State Leakage / Session Hijacking
* **Vulnerability:** If a user modified their input after generating a valid token, the UI could potentially retain a valid state, allowing unauthorized access via a stale session.
* **Remediation (Technical Control):** Implemented **Active Session Destruction**. An event listener monitors the input field to instantly revoke the JWT and clear local storage the moment tampering or modification is detected.

### 2. Risk: The Oracle Problem (Residual Risk)
* **Vulnerability:** A minor could input a false birth year (e.g., 1990) to bypass the system. The ZKP proves the "math" is correct, but cannot verify the "truth" of the initial input.
* **Future Roadmap:** In a production environment, manual input would be replaced by **Verifiable Credentials (VCs)** issued by a trusted entity (e.g., DigiLocker/UIDAI). The ZK circuit would then verify the government's digital signature rather than raw user input.

---

## 🛠️ Technology Stack
* **Cryptography:** Circom, SnarkJS (Groth16 Protocol)
* **Backend:** Node.js, Express.js
* **Access Management:** JSON Web Tokens (JWT)
* **Frontend:** HTML5, JavaScript (Vanilla)

---

## 🛡️ Audit Procedure
To verify the GRC controls of this PoC:
1.  **Network Inspect:** Confirm via browser DevTools that no birth year data is included in the POST request.
2.  **State Integrity:** Attempt to change the age input after verification; confirm the session is immediately terminated.

---
**Created as a case study for GRC, Privacy Engineering, and Secure Systems Architecture.**
