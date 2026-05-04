# ISO-05: Internal Audit Checklist and Management Review Template

---

**Project Title:** Internal Audit Checklist and Management Review Template for ClearBridge HMS ISMS
**System Reference:** ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD
**Framework / Standard:** ISO 27001:2022 Clauses 9.2 (Internal Audit) and 9.3 (Management Review)
**Author:** Ina Grace Kamara, ISSO, ClearBridge Technologies
**Date:** May 2024
**Status:** Complete

---

## Purpose

ISO 27001:2022 Clause 9 covers Performance Evaluation. Two of its most important requirements are the internal audit (Clause 9.2) and the management review (Clause 9.3). These are the mechanisms through which the organization checks that its ISMS is working as intended and that leadership is actively engaged.

An internal audit is not the same as a 3PAO assessment. The internal audit is conducted by the organization itself (or an independent internal auditor) to verify ISMS effectiveness against its own policies and ISO 27001 requirements. A management review is a formal meeting where top management reviews the ISMS outputs, risks, and objectives and makes decisions about improvements.

This document provides an internal audit checklist for the ClearBridge HMS ISMS and a completed management review template for the Q2 2024 review.

---

## PART A: INTERNAL AUDIT CHECKLIST

### Audit Overview

| Field | Detail |
|---|---|
| Audit Scope | ClearBridge HMS ISMS, all clauses of ISO 27001:2022 |
| Audit Period | Q2 2024 (April-June) |
| Lead Auditor | Ina Grace Kamara, ISSO (Internal Auditor) |
| Supporting Auditor | Walter J. Drummond, HHS SAISO (Independent Reviewer) |
| Audit Dates | June 3-7, 2024 |
| Audit Report Date | June 14, 2024 |

Note: For a fully conformant ISO 27001 certification audit, the internal auditor should be independent from the area being audited. This internal audit was conducted by the ISSO with independent review by the HHS SAISO to maintain reasonable objectivity in the absence of a separate internal audit function.

---

### Clause 4: Context of the Organization

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 4.1 | Is the internal and external context documented and current? | ISMS Scope document (ISO-01), last updated April 2024 | Current and complete | Conformant |
| 4.2 | Are interested parties and their requirements documented? | ISO-01 interested parties table | 9 interested parties documented with requirements | Conformant |
| 4.3 | Is the ISMS scope clearly defined with justified inclusions and exclusions? | ISO-01 scope section | Scope covers AWS GovCloud boundary and ClearBridge employees | Conformant |
| 4.4 | Is the ISMS established, implemented, and maintained? | SSP, risk register, policies | ISMS artifacts current and reviewed within 12 months | Conformant |

### Clause 5: Leadership

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 5.1 | Is there evidence of top management commitment? | Signed InfoSec Policy (Jan 2024); CAB meeting minutes | Policy signed by VP Engineering; management participates in CAB | Conformant |
| 5.2 | Is the information security policy documented and communicated? | InfoSec Policy v1.2; staff acknowledgment records | Policy distributed; 97% of staff have acknowledged | Minor Finding (3 new hires have not yet acknowledged) |
| 5.3 | Are ISMS roles and responsibilities assigned? | ISMS roles table in ISO-01; SSP roles | Roles assigned with names for all key positions | Conformant |

### Clause 6: Planning

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 6.1 | Is a risk assessment process defined and applied? | Risk register (ISO-03); methodology documentation | 12 risks assessed; methodology documented | Conformant |
| 6.2 | Are information security objectives defined, measurable, and tracked? | ISO-01 objectives table; monthly ConMon reports | 6 measurable objectives with targets; 5 of 6 on track | Conformant |
| 6.1.3 | Is a Statement of Applicability produced and current? | SoA (ISO-02) | All 93 controls addressed; 10 exclusions with documented justifications | Conformant |

### Clause 7: Support

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 7.2 | Is documented evidence of staff competence maintained? | Training records; certification records | Annual security training 97% complete; ISSO maintains certifications | Minor Finding (3 users overdue for training -- addressed in POA-013) |
| 7.3 | Are staff aware of the information security policy and their responsibilities? | Policy acknowledgment records; training completion records | 97% acknowledgment rate | Minor Finding (same 3 users as above) |
| 7.4 | Are there processes for relevant internal and external communication? | Incident reporting procedures; ConMon reporting calendar | Communication procedures documented and followed | Conformant |
| 7.5 | Is documented information controlled and maintained? | Document control log; version history in Confluence | Version control applied; document reviews documented | Conformant |

### Clause 8: Operation

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 8.1 | Are operational plans and controls in place? | SSP; runbooks; ConMon plan | Documented and operational | Conformant |
| 8.2 | Are risk assessments conducted at planned intervals or when changes occur? | Risk register dated April 2024; change log | Annual assessment completed; no significant changes without risk review | Conformant |
| 8.3 | Are risk treatment plans being implemented? | Risk treatment plan (ISO-04); POA&M | Treatment actions underway; timelines tracked | Conformant |

### Clause 9: Performance Evaluation

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 9.1 | Are monitoring and measurement processes defined? | ConMon plan; monthly reports | Monthly monitoring activities documented and executed | Conformant |
| 9.2 | Was an internal audit conducted? | This checklist | Current audit underway | N/A |
| 9.3 | Was a management review conducted? | Management review minutes (see Part B) | Q1 2024 review completed April 5, 2024 | Conformant |

### Clause 10: Improvement

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 10.1 | Are nonconformities documented and corrective actions tracked? | Audit finding tracker; POA&M | 3 minor findings from prior quarter; 2 closed, 1 in progress | Conformant |
| 10.2 | Is the ISMS continually improved based on audit results and reviews? | Risk treatment plan updates; policy revisions | Risk treatment plan updated post-assessment; policy minor update in May | Conformant |

### Audit Summary

| Finding Type | Count |
|---|---|
| Conformant | 22 |
| Minor Finding | 2 |
| Major Nonconformity | 0 |
| Observation | 0 |

**Minor Findings:**
- MF-001: 3 staff members have not acknowledged the information security policy (Clause 5.2). Corrective Action: ISSO to send reminders; confirm acknowledgment within 30 days.
- MF-002: 3 staff members are overdue for annual security awareness training (Clause 7.2/7.3). Corrective Action: This is tracked in POA-013; completion confirmed August 10, 2024.

---

## PART B: MANAGEMENT REVIEW TEMPLATE (Q2 2024)

**Management Review Meeting: ClearBridge HMS ISMS**
**Date:** July 8, 2024
**Location:** ClearBridge Technologies HQ, Conference Room B (virtual participation for HHS attendees)

### Attendees

| Name | Role | Organization |
|---|---|---|
| Brian A. Holloway | VP Engineering / CSP Representative | ClearBridge Technologies |
| Ina Grace Kamara | ISSO | ClearBridge Technologies |
| Kevin D. Ashworth | Cloud Ops Lead | ClearBridge Technologies |
| Dr. Carolyn M. Fletcher | System Owner | HHS, Benefits Technology |
| Walter J. Drummond | SAISO | HHS CISO Office |

### Review Agenda and Minutes

**1. Status of Actions from Previous Management Review (Q1 2024)**

Three action items from the Q1 2024 review were reviewed:
- Action 1: Complete FedRAMP RAR remediation actions. Status: Completed. All High-priority RAR findings closed by April 30, 2024.
- Action 2: Expand vulnerability scanning to cover all API endpoints. Status: Completed (POA-004 closed).
- Action 3: Execute ISA with CMS. Status: Completed June 30, 2024.

**2. Changes in External and Internal Context**

No significant changes to the threat landscape or regulatory environment were identified since Q1 2024. AWS announced the availability of two new GovCloud services that may be evaluated for use in HMS (AWS MemoryDB and Amazon Bedrock Government). Security review required before adoption.

**3. Information Security Performance Feedback**

Review of Q1/Q2 security objectives performance:
- ATO maintained: Yes. ATO granted July 22, 2024.
- High-risk POA&M items closed within 30 days: Yes. POA-001 and POA-002 closed July 31, 2024.
- Monthly scans on schedule: Yes. 100% completion rate.
- Security awareness training: 97% as of review date (3 users in progress).
- Critical patch SLA: 100% compliance. No Critical vulnerabilities past 15 days.
- Incident response SLA: No Moderate+ incidents in period; 1 Low event handled appropriately.

**4. Risk Assessment Results**

ISSO presented the updated risk register (ISO-03). No new risks above the acceptance threshold were identified. RISK-001 and RISK-005 treatment plans are underway and on schedule. No residual risk exceeds 10.

**5. Opportunities for Improvement**

Two improvement opportunities identified:
- Opportunity 1: Automate policy acknowledgment tracking through the LMS rather than manual tracking.
- Opportunity 2: Implement Amazon Inspector for continuous vulnerability scoring (included in RISK-003 treatment plan).

**6. Management Decisions and Resource Allocations**

Brian A. Holloway approved:
- Allocation of 60 additional engineering hours for RISK-001 treatment (UEBA, JIT access) in Q3 2024.
- Procurement of Amazon Inspector Standard tier ($180/month).
- Automation of policy acknowledgment tracking in LMS by Q4 2024.

**7. Next Review Date**

Next management review scheduled: October 7, 2024.

---

## Interview Defense Notes

- **What is the purpose of an internal audit in ISO 27001?** The internal audit verifies that the ISMS is implemented as intended and conforms to the organization's own requirements and to ISO 27001. It is not a third-party certification audit. It is an internal health check that identifies nonconformities before they become bigger problems.
- **What is the difference between a minor finding and a major nonconformity?** A minor finding means a requirement is partially met or has an isolated gap. A major nonconformity means a requirement is systematically not met or absent, which would prevent certification. For ClearBridge, failing to acknowledge a policy for 3 new hires is minor. Having no information security policy at all would be a major nonconformity.
- **Why is management review a required part of ISO 27001?** Because an ISMS requires leadership engagement to work. If management never reviews security performance, they cannot allocate resources, make decisions, or set direction. ISO 27001 mandates the review as a accountability mechanism.
- **What are the required inputs to a management review?** ISO 27001 Clause 9.3 specifies the inputs: status of prior review actions, changes in context, ISMS performance feedback (objectives, audit results, nonconformities, incidents), risk treatment status, and opportunities for improvement.
- **Can the ISSO serve as the internal auditor?** In a mature organization, the internal audit function is separate from the security operations function. In a smaller organization, the ISSO may conduct the audit with an independent reviewer for objectivity. The key is documented independence: you cannot audit your own controls without any external review.

---

*Prepared by: Ina Grace Kamara, ISSO, ClearBridge Technologies*
*System: ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD*
*[GitHub Portfolio](https://github.com/kamaraina277)*
