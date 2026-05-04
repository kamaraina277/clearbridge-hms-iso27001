# ISO-01: ISMS Scope, Context, and Leadership Document

---

**Project Title:** Information Security Management System (ISMS) Scope, Context, and Leadership Document
**System Reference:** ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD
**Framework / Standard:** ISO 27001:2022, Clauses 4, 5, and 6
**Author:** Ina Grace Kamara, ISSO, ClearBridge Technologies
**Date:** May 2024
**Status:** Complete

---

## Purpose

ISO 27001:2022 Clause 4 requires the organization to understand its internal and external context before establishing an ISMS. Clause 5 requires leadership commitment and the assignment of roles and responsibilities. Clause 6 requires the organization to address risks and opportunities and establish information security objectives.

This document captures all three clauses for ClearBridge Technologies as they apply to the ClearBridge Health Management System (HMS). This is the foundational document of the ClearBridge ISMS. Everything else in the ISMS is built on the decisions and boundaries documented here.

---

## Section 1: Organizational Context (ISO 27001:2022, Clause 4)

### 4.1 Understanding the Organization and Its Context

ClearBridge Technologies is a cloud service provider (CSP) that develops and operates health benefits management software for federal agencies. The ClearBridge HMS is its primary federal product, serving approximately 45,000 beneficiaries across 12 HHS regional offices.

**Internal factors affecting the ISMS:**

- ClearBridge is a mid-size technology company with approximately 280 employees, of which 45 are in engineering and operations roles that interact with HMS.
- The company operates under a FedRAMP Moderate authorization and is subject to HHS agency security requirements.
- The engineering culture prioritizes continuous deployment, which creates a need for strong change management controls to maintain ATO compliance.
- The company has experienced growth of 35% in the past 18 months, increasing the risk of role sprawl and access control gaps.

**External factors affecting the ISMS:**

- ClearBridge operates under the Federal Information Security Modernization Act (FISMA), the FedRAMP Authorization Act (2022), and HIPAA Privacy and Security Rules.
- The threat landscape for federal health data systems is active: HHS and CISA have issued advisories on targeting of federal health IT systems by ransomware operators and nation-state actors.
- AWS GovCloud provides the infrastructure foundation. AWS security posture changes (including new services and deprecated features) can affect the ClearBridge security architecture.
- The regulatory environment continues to evolve: NIST SP 800-53 Rev 5 introduced significant changes to privacy and supply chain controls that affect ClearBridge's ISMS scope.

### 4.2 Understanding the Needs and Expectations of Interested Parties

| Interested Party | Relationship to ClearBridge HMS | Key Information Security Requirements |
|---|---|---|
| HHS (Sponsoring Agency) | System authorizer and data owner | FedRAMP Moderate compliance, monthly ConMon reporting, FISMA compliance |
| Federal Beneficiaries | System users (indirect) | Confidentiality of PHI and PII; availability of benefit services |
| CMS (Centers for Medicare and Medicaid Services) | Data sharing partner via ISA | Secure handling of Medicare eligibility data; ISA compliance |
| Treasury BFS | Payment processing partner via MOU | Integrity of disbursement instructions; secure API connection |
| HHS OIG (Office of Inspector General) | Oversight body | Audit readiness; accurate records and logs |
| ClearBridge Employees | Internal stakeholders | Clear security policies; security awareness training |
| AWS GovCloud | Infrastructure provider | Compliance with FedRAMP High P-ATO; customer responsibility matrix |
| SecureAssess Partners, LLC (3PAO) | Independent assessor | Access to SSP, scan results, and system personnel for assessments |
| HHS Privacy Officer (Angela N. Weiss) | Privacy oversight | Compliance with Privacy Act, HIPAA, and PIA requirements |

### 4.3 Determining the Scope of the ISMS

The scope of the ClearBridge ISMS covers all information assets, processes, and personnel involved in the development, operation, and security monitoring of the ClearBridge Health Management System (HMS) within the AWS GovCloud (US-East) authorization boundary.

**In scope:**
- All ClearBridge-managed AWS GovCloud resources (EC2, RDS, S3, CloudTrail, CloudWatch, ALB, KMS, Systems Manager)
- All ClearBridge employees and contractors with access to HMS systems or data
- All ClearBridge processes related to security operations, change management, incident response, vulnerability management, and access management for HMS
- All physical locations where ClearBridge employees with HMS access work (ClearBridge headquarters, remote work arrangements)

**Out of scope:**
- AWS infrastructure layer (covered by AWS FedRAMP High P-ATO)
- HHS internal systems (covered by HHS agency ATO)
- ClearBridge non-HMS product lines

### 4.4 Information Security Management System

ClearBridge maintains a documented ISMS that covers the processes and controls required to protect the confidentiality, integrity, and availability of information processed by the ClearBridge HMS. The ISMS is documented, implemented, maintained, and continually improved in accordance with the requirements of ISO 27001:2022.

---

## Section 2: Leadership (ISO 27001:2022, Clause 5)

### 5.1 Leadership and Commitment

Top management at ClearBridge Technologies (represented by Brian A. Holloway, VP Engineering and CSP Representative) demonstrates commitment to the ISMS by:

- Approving the ISMS scope, information security policy, and security objectives
- Ensuring that information security requirements are integrated into business processes
- Ensuring that resources required for the ISMS are available
- Communicating the importance of information security compliance to all staff
- Directing that the results of annual management reviews are acted upon

### 5.2 Information Security Policy

The ClearBridge Information Security Policy is the top-level policy governing all ISMS activities. Key statements:

- ClearBridge Technologies will protect the confidentiality, integrity, and availability of all federal health data entrusted to it by HHS.
- All employees and contractors with access to HMS data must comply with the ISMS policies and complete annual security awareness training.
- Information security risks will be assessed annually and whenever significant changes occur. Risks that exceed the accepted risk threshold must be treated with documented controls.
- ClearBridge will maintain FedRAMP Moderate authorization for the HMS and will comply with all continuous monitoring requirements.
- The ISSO is responsible for day-to-day security operations and is empowered to escalate issues to senior management and the AO.
- Policy compliance is mandatory. Violations may result in disciplinary action up to and including termination and civil or criminal liability.

Policy Owner: Brian A. Holloway, VP Engineering, ClearBridge Technologies
Policy Approved: January 15, 2024
Policy Review Frequency: Annually

### 5.3 Organizational Roles, Responsibilities, and Authorities

| Role | Name | ISMS Responsibilities |
|---|---|---|
| Top Management / CSP Rep | Brian A. Holloway | ISMS executive sponsor; approves policy and resources |
| ISSO | Ina Grace Kamara | Day-to-day ISMS implementation, risk management, ConMon, AO liaison |
| Cloud Ops Lead | Kevin D. Ashworth | Technical implementation of controls; vulnerability remediation |
| Privacy Officer (HHS) | Angela N. Weiss | Privacy controls; PIA review and approval |
| System Owner (HHS) | Dr. Carolyn M. Fletcher | Business requirements; ATO decisions |
| Authorizing Official (HHS) | Robert T. Hargrove | ATO authorization; risk acceptance |

---

## Section 3: Planning (ISO 27001:2022, Clause 6)

### 6.1 Actions to Address Risks and Opportunities

The ClearBridge ISMS uses a formal risk assessment and treatment process (documented in ISO-03 and ISO-04) to identify, evaluate, and treat information security risks. Risk assessments are conducted annually and triggered by significant changes. The risk assessment methodology is documented in alignment with ISO 27005:2022.

Risk criteria:
- Likelihood scale: 1 (Very Low) to 5 (Very High)
- Impact scale: 1 (Negligible) to 5 (Catastrophic)
- Risk score = Likelihood x Impact (range: 1-25)
- Risk acceptance threshold: Risk scores below 9 are accepted. Scores 9-15 are treated or accepted with documentation. Scores above 15 require mandatory treatment.

### 6.2 Information Security Objectives

| Objective | Measure | Target | Frequency |
|---|---|---|---|
| Maintain FedRAMP Moderate ATO | ATO status | Active ATO at all times | Continuous |
| Close all High-risk POA&M items within 30 days | POA&M tracking | Zero overdue High items | Monthly |
| Complete monthly vulnerability scans | Scan completion rate | 100% on schedule | Monthly |
| Achieve 100% security awareness training completion | Training completion rate | 100% annually | Annual |
| Patch Critical vulnerabilities within 15 days | Mean time to remediate (Critical) | 15 days or less | Monthly |
| Respond to all Moderate+ incidents within 1 hour | Incident response time | 100% within SLA | As needed |

---

## Interview Defense Notes

- **What is the purpose of an ISMS scope document?** It defines what is inside the ISMS, what the organization is trying to protect, and why. Without a clear scope, you cannot determine which controls apply and which risks need to be assessed. ISO 27001 will not certify a vague or undefined scope.
- **What is an interested party in ISO 27001?** An interested party is any person or organization that has a stake in the security of your information. For ClearBridge, that includes HHS, beneficiaries, CMS, Treasury, and regulators. You need to understand what each interested party requires so your ISMS addresses their expectations.
- **What is the relationship between Clause 6 and the risk register?** Clause 6 requires you to identify risks and establish objectives. The risk register (ISO-03) and risk treatment plan (ISO-04) are the detailed deliverables that fulfill Clause 6. The scope document sets the framework; the risk documents do the work.
- **How does ISO 27001 relate to FedRAMP for ClearBridge?** FedRAMP requires a specific set of controls and processes aligned with NIST SP 800-53. ISO 27001 provides a management framework for implementing and improving those controls. Running both in parallel means the risk register, incident response plan, and ConMon activities serve both frameworks simultaneously.
- **What does top management commitment mean in an ISO 27001 ISMS?** It means the executives approve the policy, allocate resources, and hold the ISSO accountable. If top management does not commit, the ISMS becomes a compliance checkbox exercise rather than a real security program. Auditors look for documented evidence of top management involvement.

---

*Prepared by: Ina Grace Kamara, ISSO, ClearBridge Technologies*
*System: ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD*
*[GitHub Portfolio](https://github.com/kamaraina277)*
