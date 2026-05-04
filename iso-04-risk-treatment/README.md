# ISO-04: Risk Treatment Plan

---

**Project Title:** Information Security Risk Treatment Plan for ClearBridge Health Management System
**System Reference:** ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD
**Framework / Standard:** ISO 27005:2022 | ISO 27001:2022 Clause 6.1.3
**Author:** Ina Grace Kamara, ISSO, ClearBridge Technologies
**Date:** May 2024
**Status:** Complete (Top 5 risks treated)

---

## Purpose

ISO 27001:2022 Clause 6.1.3 requires the organization to select and document risk treatment options for information security risks. ISO 27005:2022 identifies four treatment options: Modify (implement controls to reduce likelihood or impact), Retain (accept the risk within the defined threshold), Avoid (eliminate the activity that creates the risk), and Share (transfer the risk to a third party such as an insurer).

This Risk Treatment Plan documents the treatment approach for the five highest-residual risks identified in the ClearBridge HMS Risk Register (ISO-03). For each risk, the plan specifies the treatment option selected, the controls to be implemented or strengthened, the owner, cost estimate, implementation timeline, and success criteria.

---

## Treatment Decision Matrix

| Risk ID | Risk Title | Residual Score | Treatment Option | Justification |
|---|---|---|---|---|
| RISK-001 | Unauthorized access to PHI via compromised credentials | 10 (Moderate) | Modify | Residual risk exceeds acceptance threshold; additional technical controls feasible |
| RISK-002 | Ransomware encryption of production data | 8 (Low-Mod) | Accept with monitoring | Strong controls in place; cost of further reduction disproportionate to residual risk |
| RISK-003 | Exploitation of unpatched vulnerability in EC2 AMI | 8 (Low-Mod) | Modify + Accept | Automated patching improvements feasible; residual risk acceptable after improvement |
| RISK-004 | Integrity failure in Treasury disbursement API | 5 (Low) | Accept | Controls are strong; residual risk within threshold |
| RISK-005 | Unauthorized data exfiltration by malicious insider | 8 (Low-Mod) | Modify + Accept | UEBA enhancement feasible; risk not fully accepted without improvement |

---

## Risk Treatment Detail

### RISK-001: Unauthorized Access to PHI via Compromised Credentials

**Current Residual Score:** 10 (Moderate) | **Target Residual Score:** 6 (Low)

**Treatment Option:** Modify

**Current Controls:** MFA via HHS IdP; RBAC; quarterly access reviews; SIEM alerts on failed logins.

**Additional Controls to Implement:**

| Control | Description | ISO 27001 Reference | Owner | Target Date |
|---|---|---|---|---|
| Implement UEBA (User and Entity Behavior Analytics) | Configure SIEM Splunk to baseline normal user behavior and alert on anomalies: logins from new geographies, off-hours access, bulk data queries | ISO Annex A 8.16 (Monitoring Activities) | Kevin D. Ashworth, Cloud Ops | August 30, 2024 |
| Implement privileged access workstations (PAWs) | Require all admin access to occur from a dedicated, hardened device; no web browsing or email on PAWs | ISO Annex A 8.2 (Privileged Access Rights) | Kevin D. Ashworth, Cloud Ops | September 30, 2024 |
| Reduce MFA session duration for privileged accounts | Reduce re-authentication interval from 8 hours to 1 hour for admin accounts | ISO Annex A 8.5 (Secure Authentication) | Kevin D. Ashworth, Cloud Ops | August 15, 2024 |
| Implement just-in-time (JIT) privileged access | Replace standing privileged access with JIT access via AWS Systems Manager; access expires after defined window | ISO Annex A 5.18 (Access Rights) | Kevin D. Ashworth, Cloud Ops | October 31, 2024 |

**Resource Estimate:** 80 hours engineering time; existing Splunk license covers UEBA functionality.

**Success Criteria:** Post-implementation residual risk score of 6 or below; UEBA alerts tested and tuned within 30 days of deployment; JIT access operational by October 31, 2024.

**Risk Owner:** Ina Grace Kamara, ISSO

---

### RISK-002: Ransomware Encryption of Production Data

**Current Residual Score:** 8 (Low-Moderate) | **Treatment Option:** Accept with monitoring

**Justification:** The existing controls are strong. AWS GuardDuty with threat intelligence provides real-time detection. S3 Object Lock provides immutable backups with 30-day retention. EC2 image backups are taken daily and tested quarterly. The cost of further risk reduction (adding endpoint isolation automation, for example) is disproportionate to the residual risk given the cloud-native architecture.

**Monitoring Commitment:** Monthly review of GuardDuty findings; quarterly restore tests of RDS and S3 backups; annual review of this risk acceptance decision.

**Risk Owner:** Kevin D. Ashworth, Cloud Ops

---

### RISK-003: Exploitation of Unpatched Vulnerability in EC2 AMI

**Current Residual Score:** 8 (Low-Moderate) | **Target Residual Score:** 4 (Low)

**Treatment Option:** Modify + Accept

**Additional Controls to Implement:**

| Control | Description | ISO 27001 Reference | Owner | Target Date |
|---|---|---|---|---|
| Implement automated OS patching for non-production instances | Extend AWS Systems Manager Patch Manager to cover dev and staging environments on the same SLA as production | ISO Annex A 8.8 (Technical Vulnerability Management) | Kevin D. Ashworth, Cloud Ops | August 15, 2024 |
| Enable Amazon Inspector for continuous vulnerability scoring | Replace monthly scheduled scans with continuous Amazon Inspector scanning tied to new AMI deployments | ISO Annex A 8.8 | Kevin D. Ashworth, Cloud Ops | September 30, 2024 |

**Resource Estimate:** 20 hours engineering time; Amazon Inspector Standard tier at approximately $180/month.

**Success Criteria:** Zero High/Critical unpatched vulnerabilities older than 30 days on any in-scope instance, including non-production; Inspector reporting integrated into monthly ConMon.

**Risk Owner:** Kevin D. Ashworth, Cloud Ops

---

### RISK-004: Integrity Failure in Treasury Disbursement API

**Current Residual Score:** 5 (Low) | **Treatment Option:** Accept

**Justification:** The combination of HMAC-SHA256 transaction signing, mutual TLS authentication, daily reconciliation between HMS and Treasury records, and immutable CloudTrail logging of all API calls reduces the probability of an undetected integrity failure to near zero. The cost of additional controls would exceed the expected loss from the risk.

**Risk Owner:** Ina Grace Kamara, ISSO

---

### RISK-005: Unauthorized Data Exfiltration by Malicious Insider

**Current Residual Score:** 8 (Low-Moderate) | **Target Residual Score:** 6 (Low)

**Treatment Option:** Modify + Accept

**Additional Controls to Implement:**

| Control | Description | ISO 27001 Reference | Owner | Target Date |
|---|---|---|---|---|
| Tune Macie DLP rules for PHI patterns | Update AWS Macie custom identifiers to detect ClearBridge-specific PHI patterns beyond standard PII; create alerts for large S3 downloads | ISO Annex A 8.12 (Data Leakage Prevention) | Kevin D. Ashworth, Cloud Ops | August 30, 2024 |
| Implement network traffic analysis for anomalous data transfers | Configure AWS VPC Flow Logs with Athena queries to detect unusual outbound data volumes from EC2 | ISO Annex A 8.16 (Monitoring Activities) | Kevin D. Ashworth, Cloud Ops | September 30, 2024 |
| Add data access auditing for bulk record queries | Log all queries returning more than 100 PHI records; alert ISSO immediately | ISO Annex A 8.15 (Logging) | Kevin D. Ashworth, Cloud Ops | September 30, 2024 |

**Resource Estimate:** 60 hours engineering time; no additional licensing cost (uses existing AWS services).

**Success Criteria:** Macie DLP alerts configured and tested; VPC Flow Log queries operational; bulk query alerting producing actionable results by October 31, 2024.

**Risk Owner:** Ina Grace Kamara, ISSO

---

## Treatment Plan Summary and Timeline

| Risk ID | Treatment | Key Action | Owner | Due Date | Status |
|---|---|---|---|---|---|
| RISK-001 | Modify | Implement UEBA, PAWs, JIT access | Kevin D. Ashworth | October 31, 2024 | In progress |
| RISK-002 | Accept | Monthly monitoring, quarterly restore tests | Kevin D. Ashworth | Ongoing | Active |
| RISK-003 | Modify | Extend automated patching; enable Inspector | Kevin D. Ashworth | September 30, 2024 | In progress |
| RISK-004 | Accept | Annual review | Ina Grace Kamara | April 2025 | Active |
| RISK-005 | Modify | Tune Macie; VPC Flow Logs; bulk query alerts | Kevin D. Ashworth | October 31, 2024 | In progress |

---

## Interview Defense Notes

- **What are the four ISO 27005 risk treatment options?** Modify (add controls to reduce the risk), Retain (accept the risk as-is), Avoid (stop the activity that creates the risk), and Share (transfer the risk to a third party like an insurer). Most practical treatment plans use a combination of Modify and Retain.
- **Why would you choose to accept a risk rather than always treating it?** Because the cost of treatment can exceed the expected loss from the risk. Risk acceptance is a legitimate business decision, not laziness. The key is that it must be documented and formally approved by the risk owner. You cannot silently accept a risk.
- **What is a risk owner and why does it matter?** A risk owner is the person accountable for monitoring and managing a specific risk. They must accept or approve the residual risk level. Without a named owner, no one is accountable when the risk materializes.
- **How do you verify that a risk treatment was effective?** You re-assess the risk after controls are implemented. If the residual score drops as expected, the treatment was effective. You also look for operational evidence: UEBA alerts are firing correctly, JIT access is being used, backup restores are succeeding.
- **What is the relationship between the Risk Treatment Plan and the POA&M?** They address similar problems but in different frameworks. The Risk Treatment Plan is the ISO 27005 document tracking risk-based control improvements. The POA&M is the FedRAMP document tracking findings from the 3PAO assessment. For ClearBridge, both exist simultaneously, and many items appear in both.

---

*Prepared by: Ina Grace Kamara, ISSO, ClearBridge Technologies*
*System: ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD*
*[GitHub Portfolio](https://github.com/kamaraina277)*
