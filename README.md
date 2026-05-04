# ClearBridge HMS: ISO 27001:2022 and ISO 27005 Compliance Portfolio
### Information Security Management System (ISMS) for a Federal Health Benefits Platform

![Framework](https://img.shields.io/badge/Framework-ISO%2027001%3A2022-blue)
![Standard](https://img.shields.io/badge/Standard-ISO%2027005%3A2022-darkblue)
![System](https://img.shields.io/badge/System-ClearBridge%20HMS-green)
![Status](https://img.shields.io/badge/Status-Portfolio%20Complete-brightgreen)
![Cert](https://img.shields.io/badge/Cert-CompTIA%20Security%2B%20(In%20Progress)-orange)

---

## About This Repository

This repository contains a simulated ISO 27001:2022 Information Security Management System (ISMS) compliance program for the ClearBridge Health Management System (HMS), a fictional cloud-hosted federal health benefits platform. The work demonstrates practical application of ISO 27001 clauses, Annex A controls, and ISO 27005 risk management methodology in a federal healthcare context.

All documents follow the structure and terminology of ISO 27001:2022 and ISO 27005:2022 and are grounded in the specific system details of ClearBridge HMS. This portfolio also includes a crosswalk between the FedRAMP/NIST RMF framework and ISO 27001:2022, demonstrating how federal GRC knowledge maps to international standards.

---

## System Overview

| Field | Detail |
|---|---|
| System Name | ClearBridge Health Management System (HMS) |
| System ID | HHS-CB-HMS-2024-MOD |
| System Owner | Dr. Carolyn M. Fletcher, HHS Deputy Director, Benefits Technology |
| ISSO | Ina Grace Kamara, ClearBridge Technologies |
| Cloud Platform | AWS GovCloud (US-East) |
| FedRAMP Baseline | Moderate (parallel authorization) |
| Users | ~45,000 federal beneficiaries, 300 agency staff, 12 regional offices |
| Data Types | PHI, PII, federal benefit eligibility records, audit logs |

---

## Repository Structure

```
clearbridge-hms-iso27001/
|
|-- iso-01-isms-scope/
|   |-- README.md   (ISMS Scope, Context, and Interested Parties -- ISO Clauses 4-6)
|
|-- iso-02-soa/
|   |-- README.md   (Statement of Applicability -- all 93 Annex A controls)
|
|-- iso-03-risk-register/
|   |-- README.md   (Information Security Risk Register -- 12 risks, ISO 27005)
|
|-- iso-04-risk-treatment/
|   |-- README.md   (Risk Treatment Plan -- top 5 risks, ISO 27005)
|
|-- iso-05-audit-management-review/
|   |-- README.md   (Internal Audit Checklist and Management Review Template -- ISO Clauses 9-10)
|
|-- iso-06-crosswalk/
|   |-- README.md   (FedRAMP/NIST RMF vs. ISO 27001:2022 Framework Crosswalk)
|
|-- README.md       (This file)
```

---

## Project Deliverables

| Project | Document | ISO Reference | Status |
|---|---|---|---|
| ISO-01 | ISMS Scope and Context Document | ISO 27001:2022 Clauses 4, 5, 6 | Complete |
| ISO-02 | Statement of Applicability (SoA) | ISO 27001:2022 Annex A (all 93 controls) | Complete |
| ISO-03 | Information Security Risk Register | ISO 27005:2022 | Complete |
| ISO-04 | Risk Treatment Plan | ISO 27005:2022 | Complete |
| ISO-05 | Internal Audit Checklist and Management Review | ISO 27001:2022 Clauses 9, 10 | Complete |
| ISO-06 | FedRAMP/NIST RMF vs. ISO 27001:2022 Crosswalk | NIST SP 800-53, ISO 27001:2022 | Complete |

---

## Framework Coverage

| ISO 27001:2022 Clause | Topic | Covered |
|---|---|---|
| Clause 4 | Context of the Organization | ISO-01 |
| Clause 5 | Leadership | ISO-01 |
| Clause 6 | Planning (risk, objectives) | ISO-01, ISO-03, ISO-04 |
| Clause 7 | Support | ISO-01 |
| Clause 8 | Operation | ISO-02, ISO-03, ISO-04 |
| Clause 9 | Performance Evaluation | ISO-05 |
| Clause 10 | Improvement | ISO-05 |
| Annex A (all 93 controls) | Security Controls | ISO-02 |
| ISO 27005:2022 | Risk Management | ISO-03, ISO-04 |

---

## Key Personnel

| Role | Name | Organization |
|---|---|---|
| ISSO | Ina Grace Kamara | ClearBridge Technologies |
| Authorizing Official (AO) | Robert T. Hargrove | HHS CISO |
| System Owner | Dr. Carolyn M. Fletcher | HHS, Benefits Technology |
| Privacy Officer | Angela N. Weiss | HHS Office of the General Counsel |
| Cloud Ops Lead | Kevin D. Ashworth | ClearBridge Technologies |

---

## Related Repositories

| Repository | Description |
|---|---|
| [clearbridge-hms-fedramp-rmf](https://github.com/kamaraina277/clearbridge-hms-fedramp-rmf) | FedRAMP Moderate ATO journey for ClearBridge HMS (NIST RMF Steps 0-6) |
| [clearbridge-hms-security-plus](https://github.com/kamaraina277/clearbridge-hms-security-plus) | CompTIA Security+ SY0-701 domain projects mapped to ClearBridge HMS |

---

## Portfolio Overview

| Repository | Framework | Projects | Status |
|---|---|---|---|
| clearbridge-hms-fedramp-rmf | FedRAMP Moderate / NIST RMF | 7 | Complete |
| clearbridge-hms-iso27001 | ISO 27001:2022 / ISO 27005 | 6 | Complete |
| clearbridge-hms-security-plus | CompTIA Security+ SY0-701 | 6 | Complete |

---

## About the Author

**Ina Grace Kamara**
Junior GRC Analyst, Quarantyne Technologies | Cybersecurity Analyst | GRC and Compliance
CompTIA Security+ SY0-701 (In Progress) | NIST RMF Foundational Training
Maryland

[GitHub Portfolio](https://github.com/kamaraina277)
