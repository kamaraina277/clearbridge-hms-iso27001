# ISO-03: Information Security Risk Register

---

**Project Title:** Information Security Risk Register for ClearBridge Health Management System
**System Reference:** ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD
**Framework / Standard:** ISO 27005:2022 | ISO 27001:2022 Clause 6.1.2
**Author:** Ina Grace Kamara, ISSO, ClearBridge Technologies
**Date:** May 2024
**Status:** Complete (12 risks documented)

---

## Purpose

ISO 27001:2022 Clause 6.1.2 requires the organization to define and apply an information security risk assessment process. ISO 27005:2022 provides the methodology for identifying, analyzing, evaluating, and treating information security risks.

This risk register documents 12 information security risks identified for ClearBridge HMS through a structured risk assessment conducted in April 2024. The assessment used structured interviews with key personnel, review of the threat landscape, and analysis of historical incidents and vulnerability scan results.

---

## Risk Assessment Methodology

**Risk Identification Sources:** Threat landscape review (CISA advisories, HHS sector alerts), vulnerability scan analysis, incident history, asset inventory review, and structured interviews with ISSO, Cloud Ops Lead, and System Owner.

**Risk Scoring Methodology:**
- Likelihood: 1 (Very Low) to 5 (Very High)
- Impact: 1 (Negligible) to 5 (Catastrophic)
- Inherent Risk Score = Likelihood x Impact (range: 1-25)
- Residual Risk Score = Likelihood (after controls) x Impact (after controls)

**Risk Acceptance Thresholds:**
- Scores 1-8: Accept (Low)
- Scores 9-15: Treat or Accept with documentation (Moderate)
- Scores 16-25: Must treat (High / Critical)

**Risk Assessment Date:** April 15-19, 2024
**Next Assessment Due:** April 2025
**Assessment Lead:** Ina Grace Kamara, ISSO

---

## Risk Register

| Risk ID | Risk Title | Threat Source | Affected Asset | Likelihood | Impact | Inherent Score | Risk Level | Current Controls | Residual Likelihood | Residual Impact | Residual Score | Residual Level | Treatment |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RISK-001 | Unauthorized access to PHI via compromised credentials | External attacker; insider threat | User authentication system; RDS (PHI data) | 3 | 5 | 15 | Moderate-High | MFA via HHS IdP; RBAC; quarterly access reviews; SIEM alerts | 2 | 5 | 10 | Moderate | Treat |
| RISK-002 | Ransomware encryption of production data | External attacker (phishing vector) | EC2 instances; RDS database; S3 buckets | 3 | 5 | 15 | Moderate-High | Endpoint EDR; GuardDuty; immutable backups; S3 object lock | 2 | 4 | 8 | Low | Accept with monitoring |
| RISK-003 | Exploitation of unpatched vulnerability in EC2 AMI | External attacker; automated scanning | EC2 application servers | 3 | 4 | 12 | Moderate | Monthly Nessus scans; 30-day patch SLA for High; auto-patching for critical | 2 | 4 | 8 | Low | Accept with monitoring |
| RISK-004 | Integrity failure in Treasury disbursement API | Internal error; API injection attack | Treasury API integration; payment records | 2 | 5 | 10 | Moderate | HMAC-SHA256 signing; TLS mutual auth; transaction reconciliation; immutable logs | 1 | 5 | 5 | Low | Accept |
| RISK-005 | Unauthorized data exfiltration by malicious insider | Malicious insider | PHI/PII in S3 and RDS; beneficiary records | 2 | 5 | 10 | Moderate | Least privilege IAM; CloudTrail logging; DLP (AWS Macie); UEBA in SIEM | 2 | 4 | 8 | Low | Accept with monitoring |
| RISK-006 | Data exposure via misconfigured S3 bucket | Accidental misconfiguration; developer error | S3 buckets containing PHI and audit logs | 3 | 4 | 12 | Moderate | S3 Block Public Access enforced organization-wide; AWS Config rules; Macie scanning | 1 | 4 | 4 | Low | Accept |
| RISK-007 | Denial of Service attack rendering HMS unavailable | External DDoS; resource exhaustion | ALB; EC2 application tier | 3 | 3 | 9 | Moderate | AWS Shield Standard; ALB rate limiting; auto-scaling; CloudWatch alarms | 2 | 3 | 6 | Low | Accept |
| RISK-008 | Supply chain compromise via malicious dependency | Third-party/open-source risk | Application codebase; CI/CD pipeline | 2 | 4 | 8 | Low-Moderate | Dependency scanning (Dependabot); approved package registry; SCRM policy | 2 | 3 | 6 | Low | Accept with monitoring |
| RISK-009 | Loss of audit log integrity | Insider threat; misconfiguration | CloudTrail logs; SIEM data | 2 | 4 | 8 | Low-Moderate | CloudTrail log file validation; S3 object lock on log archive; SIEM immutable storage | 1 | 4 | 4 | Low | Accept |
| RISK-010 | Unauthorized access via unrevoked access rights | Process failure; HR communication gap | All HMS systems | 3 | 4 | 12 | Moderate | Offboarding process: access revoked within 4 hours; quarterly reviews; automated deprovisioning | 2 | 3 | 6 | Low | Accept with monitoring |
| RISK-011 | CMS Medicare data exposure during SFTP transfer | Network interception; misconfiguration | CMS data feed; SFTP connection | 2 | 4 | 8 | Low-Moderate | Dedicated circuit for SFTP; TLS for all transfers; ISA executed | 1 | 4 | 4 | Low | Accept |
| RISK-012 | Non-compliance with FedRAMP ConMon requirements leading to ATO suspension | Process failure; resource constraints | ATO status; system operation | 2 | 5 | 10 | Moderate | ISSO owns ConMon calendar; monthly report checklist; senior management oversight | 1 | 5 | 5 | Low | Accept |

---

## Risk Summary

| Risk Level | Count (Inherent) | Count (Residual) |
|---|---|---|
| High/Critical (16-25) | 0 | 0 |
| Moderate-High (13-15) | 2 | 0 |
| Moderate (9-12) | 6 | 2 |
| Low (1-8) | 4 | 10 |
| **Total** | **12** | **12** |

All residual risks are within the accepted risk tolerance. The two Moderate residual risks (RISK-001 and RISK-002) are addressed in the Risk Treatment Plan (ISO-04) with additional controls and are subject to ongoing monitoring.

---

## Risk Owner Assignments

| Risk ID | Risk Owner | Review Frequency |
|---|---|---|
| RISK-001 | Ina Grace Kamara, ISSO | Quarterly |
| RISK-002 | Kevin D. Ashworth, Cloud Ops | Quarterly |
| RISK-003 | Kevin D. Ashworth, Cloud Ops | Monthly (tied to scan cycle) |
| RISK-004 | Ina Grace Kamara, ISSO | Semi-annual |
| RISK-005 | Ina Grace Kamara, ISSO | Quarterly |
| RISK-006 | Kevin D. Ashworth, Cloud Ops | Monthly (tied to AWS Config) |
| RISK-007 | Kevin D. Ashworth, Cloud Ops | Semi-annual |
| RISK-008 | Kevin D. Ashworth, Cloud Ops | Quarterly |
| RISK-009 | Ina Grace Kamara, ISSO | Monthly |
| RISK-010 | Ina Grace Kamara, ISSO | Quarterly |
| RISK-011 | Ina Grace Kamara, ISSO | Semi-annual |
| RISK-012 | Ina Grace Kamara, ISSO | Monthly |

---

## Interview Defense Notes

- **What is the difference between a risk assessment and a risk register?** The risk assessment is the process: identifying threats, evaluating likelihood and impact, calculating scores. The risk register is the output: a documented record of all identified risks with scores, owners, controls, and treatment decisions. The register is updated as risks are reassessed or new risks emerge.
- **What is the difference between inherent risk and residual risk?** Inherent risk is the risk before controls are applied. Residual risk is what remains after existing controls reduce the likelihood or impact. The goal is to bring residual risk below the acceptance threshold. If residual risk is still too high, you need additional controls.
- **Why was RISK-004 (Treasury disbursement integrity) rated Moderate rather than High despite the 5-impact?** The likelihood was rated 2 (Low) because the technical controls are strong: HMAC signing, mutual TLS, and transaction reconciliation. The combination of a strong cryptographic integrity check and daily reconciliation significantly reduces the probability of an undetected integrity failure. Inherent risk was 10; residual was 5.
- **How does ISO 27005 relate to ISO 27001?** ISO 27001 tells you that you must do risk assessment (Clause 6.1.2). ISO 27005 tells you how to do it. ISO 27005:2022 provides the methodology, terminology, and process guidance. You can use ISO 27005 as your risk assessment methodology referenced in your ISMS.
- **What would you do if a new risk emerged between annual assessments?** Significant changes (new system components, new threat intelligence, incidents) should trigger an ad-hoc risk assessment for the affected area. The risk register is not a once-a-year document. It should be a living artifact that the ISSO updates whenever the risk landscape changes.

---

*Prepared by: Ina Grace Kamara, ISSO, ClearBridge Technologies*
*System: ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD*
*[GitHub Portfolio](https://github.com/kamaraina277)*
