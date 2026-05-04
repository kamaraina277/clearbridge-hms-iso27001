# ISO-02: Statement of Applicability (SoA)

---

**Project Title:** ISO 27001:2022 Statement of Applicability for ClearBridge Health Management System
**System Reference:** ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD
**Framework / Standard:** ISO 27001:2022 Annex A (all 93 controls across 4 themes)
**Author:** Ina Grace Kamara, ISSO, ClearBridge Technologies
**Date:** May 2024
**Status:** Complete

---

## Purpose

The Statement of Applicability (SoA) is a mandatory deliverable required by ISO 27001:2022 Clause 6.1.3. It documents each Annex A control, states whether it is applicable to the organization, documents the justification for inclusion or exclusion, and indicates the current implementation status.

The SoA is one of the most important documents in an ISO 27001 ISMS. It demonstrates that the organization has thoughtfully considered all 93 controls rather than blindly applying all of them or arbitrarily excluding them. Auditors scrutinize the SoA carefully.

ISO 27001:2022 reorganized the controls from 114 controls in 14 domains (2013 version) to 93 controls in 4 themes (Organizational, People, Physical, Technological). This SoA follows the 2022 structure.

---

## SoA Summary

| Theme | Controls in Theme | Applicable | Not Applicable |
|---|---|---|---|
| 5. Organizational Controls | 37 | 35 | 2 |
| 6. People Controls | 8 | 8 | 0 |
| 7. Physical Controls | 14 | 8 | 6 |
| 8. Technological Controls | 34 | 32 | 2 |
| **Total** | **93** | **83** | **10** |

---

## Theme 5: Organizational Controls (37 Controls)

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 5.1 | Policies for information security | Yes | Core ISMS requirement; ClearBridge InfoSec Policy approved Jan 2024 | Implemented |
| 5.2 | Information security roles and responsibilities | Yes | Roles assigned in SSP and ISMS scope document | Implemented |
| 5.3 | Segregation of duties | Yes | IAM roles separate developer, ops, and admin functions | Implemented |
| 5.4 | Management responsibilities | Yes | Brian Holloway as executive sponsor; documented | Implemented |
| 5.5 | Contact with authorities | Yes | HHS CISO and US-CERT contacts documented in IRP | Implemented |
| 5.6 | Contact with special interest groups | Yes | ISSO subscribes to CISA advisories and NIST updates | Implemented |
| 5.7 | Threat intelligence | Yes | CISA alerts reviewed weekly; integrated into risk register | Implemented |
| 5.8 | Information security in project management | Yes | Security requirements included in all HMS sprint planning | Implemented |
| 5.9 | Inventory of information and other associated assets | Yes | ServiceNow CMDB maintained; asset inventory reviewed monthly | Implemented |
| 5.10 | Acceptable use of information and other associated assets | Yes | Acceptable Use Policy (AUP) signed by all staff | Implemented |
| 5.11 | Return of assets | Yes | Equipment return process on employee offboarding | Implemented |
| 5.12 | Classification of information | Yes | Data classification policy: PHI/PII (Sensitive), operational (Internal), public | Implemented |
| 5.13 | Labelling of information | Yes | Data labeling applied in S3 bucket tagging and DLP rules | Implemented |
| 5.14 | Information transfer | Yes | Secure transfer policies; TLS required for all data in transit | Implemented |
| 5.15 | Access control | Yes | RBAC enforced via AWS IAM; quarterly access reviews | Implemented |
| 5.16 | Identity management | Yes | HHS IdP via SAML 2.0; hardware MFA for privileged users | Implemented |
| 5.17 | Authentication information | Yes | Password policy enforced; no shared credentials permitted | Implemented |
| 5.18 | Access rights | Yes | Access rights granted through formal provisioning process | Implemented |
| 5.19 | Information security in supplier relationships | Yes | AWS contract includes security requirements; vendor risk register | Implemented |
| 5.20 | Addressing information security within supplier agreements | Yes | AWS BAA executed; MSA includes security requirements | Implemented |
| 5.21 | Managing information security in the ICT supply chain | Yes | SCRM policy approved Aug 2024; open-source dependency scanning active | Partially Implemented |
| 5.22 | Monitoring, review and change management of supplier services | Yes | AWS service changes reviewed in CAB | Implemented |
| 5.23 | Information security for use of cloud services | Yes | AWS GovCloud selected specifically for federal compliance | Implemented |
| 5.24 | Information security incident management planning and preparation | Yes | Incident Response Plan v2.1 approved | Implemented |
| 5.25 | Assessment and decision on information security events | Yes | SIEM triage procedures documented | Implemented |
| 5.26 | Response to information security incidents | Yes | IRP includes containment, eradication, and recovery steps | Implemented |
| 5.27 | Learning from information security incidents | Yes | Post-incident reviews conducted; lessons learned documented | Implemented |
| 5.28 | Collection of evidence | Yes | Evidence collection procedures in IRP for potential litigation | Implemented |
| 5.29 | Information security during disruption | Yes | Business Continuity Plan and BCP tested annually | Implemented |
| 5.30 | ICT readiness for business continuity | Yes | RTO: 4 hours; RPO: 1 hour; documented in SSP CP section | Implemented |
| 5.31 | Legal, statutory, regulatory and contractual requirements | Yes | FISMA, FedRAMP, HIPAA compliance requirements mapped | Implemented |
| 5.32 | Intellectual property rights | Yes | Open-source license policy; no unauthorized software | Implemented |
| 5.33 | Protection of records | Yes | Record retention: audit logs 3 years; HR records 7 years | Implemented |
| 5.34 | Privacy and protection of PII | Yes | PIA completed; HHS Privacy Officer oversight | Implemented |
| 5.35 | Independent review of information security | Yes | Annual 3PAO assessment; internal audit conducted | Implemented |
| 5.36 | Compliance with policies, rules and standards | Yes | Annual compliance review; policy acknowledgment required | Implemented |
| 5.37 | Documented operating procedures | Yes | Runbooks and SOPs maintained in Confluence | Implemented |

---

## Theme 6: People Controls (8 Controls)

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 6.1 | Screening | Yes | Background checks for all staff with HMS access | Implemented |
| 6.2 | Terms and conditions of employment | Yes | Security responsibilities in employment agreements | Implemented |
| 6.3 | Information security awareness, education and training | Yes | Annual security awareness training; 100% completion tracked | Implemented |
| 6.4 | Disciplinary process | Yes | HR disciplinary policy covers security policy violations | Implemented |
| 6.5 | Responsibilities after termination or change of employment | Yes | Access revoked within 4 hours of departure notification | Implemented |
| 6.6 | Confidentiality or non-disclosure agreements | Yes | NDAs signed by all employees and contractors | Implemented |
| 6.7 | Remote working | Yes | Remote work security policy; VPN and MFA required | Implemented |
| 6.8 | Information security event reporting | Yes | SIEM alerts and incident reporting procedures in place | Implemented |

---

## Theme 7: Physical Controls (14 Controls)

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 7.1 | Physical security perimeters | Partially | AWS manages data center perimeters; ClearBridge office has badge access | Inherited/Implemented |
| 7.2 | Physical entry | Partially | AWS handles data center entry; ClearBridge office has visitor log | Inherited/Implemented |
| 7.3 | Securing offices, rooms and facilities | Yes | ClearBridge office: badge access for secure areas | Implemented |
| 7.4 | Physical security monitoring | Partially | AWS CCTV for data center; ClearBridge office has security cameras | Inherited/Implemented |
| 7.5 | Protecting against physical and environmental threats | No | Not applicable: ClearBridge runs no on-premises infrastructure; all in AWS GovCloud | N/A |
| 7.6 | Working in secure areas | Yes | Policies for secure area work established | Implemented |
| 7.7 | Clear desk and clear screen | Yes | Clean desk policy; screen lock after 5 minutes | Implemented |
| 7.8 | Equipment siting and protection | No | No on-premises servers; not applicable to cloud-only environment | N/A |
| 7.9 | Security of assets off-premises | Yes | Laptop security policy for remote work | Implemented |
| 7.10 | Storage media | No | No physical media in use for HMS; all data in AWS S3/RDS | N/A |
| 7.11 | Supporting utilities | No | AWS manages power/cooling for all computing; not applicable | N/A |
| 7.12 | Cabling security | No | No on-premises cabling for HMS infrastructure | N/A |
| 7.13 | Equipment maintenance | Partially | AWS handles hardware maintenance; ClearBridge manages laptops | Partial |
| 7.14 | Secure disposal or re-use of equipment | Yes | Laptop disposal policy; certified erasure required | Implemented |

---

## Theme 8: Technological Controls (34 Controls)

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 8.1 | User endpoint devices | Yes | Endpoint protection on all ClearBridge laptops; MDM enrolled | Implemented |
| 8.2 | Privileged access rights | Yes | Privileged access restricted to named individuals with MFA and session logging | Implemented |
| 8.3 | Information access restriction | Yes | RBAC enforced; data access limited by role and need-to-know | Implemented |
| 8.4 | Access to source code | Yes | GitHub access restricted; branch protection on main; PR reviews required | Implemented |
| 8.5 | Secure authentication | Yes | MFA enforced for all users; PIV or Okta Verify | Implemented |
| 8.6 | Capacity management | Yes | AWS auto-scaling configured; CloudWatch capacity alarms | Implemented |
| 8.7 | Protection against malware | Yes | AWS GuardDuty; endpoint EDR on ClearBridge laptops | Implemented |
| 8.8 | Management of technical vulnerabilities | Yes | Monthly Nessus scans; patch SLAs enforced | Implemented |
| 8.9 | Configuration management | Yes | CIS Benchmarks; ServiceNow CMDB; AWS Config rules | Implemented |
| 8.10 | Information deletion | Yes | Data retention and deletion policy; S3 lifecycle rules | Implemented |
| 8.11 | Data masking | Yes | PII/PHI masked in non-production environments; no real data in dev/test | Implemented |
| 8.12 | Data leakage prevention | Yes | AWS Macie monitors S3 for sensitive data exposure | Implemented |
| 8.13 | Information backup | Yes | RDS automated daily backups; S3 versioning; restore tested quarterly | Implemented |
| 8.14 | Redundancy of information processing facilities | Yes | Multi-AZ RDS; ALB with health checks; auto-scaling | Implemented |
| 8.15 | Logging | Yes | CloudTrail; CloudWatch; SIEM integration | Implemented |
| 8.16 | Monitoring activities | Yes | SIEM alerts; weekly log review by ISSO | Implemented |
| 8.17 | Clock synchronization | Yes | AWS NTP used across all EC2 instances | Implemented |
| 8.18 | Use of privileged utility programs | Yes | No privileged utilities installed outside of approved toolset | Implemented |
| 8.19 | Installation of software on operational systems | Yes | Change management process required for all software installs | Implemented |
| 8.20 | Networks security | Yes | VPC with subnets; NACLs; security groups; WAF on ALB | Implemented |
| 8.21 | Security of network services | Yes | All network services encrypted; no unencrypted protocols permitted | Implemented |
| 8.22 | Segregation of networks | Yes | Production, staging, and development in separate VPCs | Implemented |
| 8.23 | Web filtering | Yes | Outbound web access from EC2 filtered via NAT Gateway restrictions | Implemented |
| 8.24 | Use of cryptography | Yes | TLS 1.2+; AES-256 at rest; KMS key rotation; HMAC signing for API | Implemented |
| 8.25 | Secure development lifecycle | Yes | SAST integrated in CI/CD pipeline; PR security reviews | Implemented |
| 8.26 | Application security requirements | Yes | Security requirements documented for all new features | Implemented |
| 8.27 | Secure system architecture and engineering principles | Yes | NIST SP 800-160 Vol.1 engineering principles applied | Implemented |
| 8.28 | Secure coding | Yes | OWASP Top 10 training required; secure code review checklist | Implemented |
| 8.29 | Security testing in development and acceptance | Yes | DAST and SAST in CI/CD; pen test annually | Implemented |
| 8.30 | Outsourced development | No | No software development outsourced outside ClearBridge | N/A |
| 8.31 | Separation of development, test and production environments | Yes | Separate AWS accounts for dev, staging, and production | Implemented |
| 8.32 | Change management | Yes | CAB approves all changes; change freeze periods enforced | Implemented |
| 8.33 | Test information | Yes | Production data not used in testing; anonymized test data sets used | Implemented |
| 8.34 | Protection of information systems during audit testing | Yes | Audit activities coordinated with ISSO; no disruptive testing in prod | Implemented |

---

## Interview Defense Notes

- **What is a Statement of Applicability and why is it required?** The SoA is a required ISO 27001 document that lists all 93 Annex A controls, states whether each one is applicable, and justifies the inclusion or exclusion. It is required because ISO 27001 does not require every control in every context. The SoA is the organization's formal declaration of what controls it needs and why.
- **Can you exclude controls from the SoA?** Yes, but you must justify every exclusion. You cannot exclude a control just because it is difficult to implement. Exclusions are appropriate when a control is genuinely not relevant to the context. For ClearBridge, physical infrastructure controls like 7.8 and 7.10 are excluded because all infrastructure is in AWS GovCloud with no on-premises components.
- **What is the difference between the 2013 and 2022 versions of ISO 27001 Annex A?** ISO 27001:2013 had 114 controls organized in 14 domains. ISO 27001:2022 reorganized to 93 controls in 4 themes: Organizational, People, Physical, and Technological. Several controls were merged and 11 new controls were added, including controls for threat intelligence, cloud services, and data masking.
- **How does the SoA connect to the risk treatment plan?** The risk treatment plan (ISO-04) selects controls to reduce identified risks. Those controls must appear in the SoA as applicable. If you select a control in your risk treatment plan but mark it as not applicable in the SoA, you have a contradiction that an auditor will flag.
- **What does Partially Implemented mean?** It means the control is applicable and partially in place, but work remains. It is an honest status rather than falsely claiming full implementation. A mature ISMS tracks the gap and has a timeline to full implementation.

---

*Prepared by: Ina Grace Kamara, ISSO, ClearBridge Technologies*
*System: ClearBridge Health Management System (HMS) | HHS-CB-HMS-2024-MOD*
*[GitHub Portfolio](https://github.com/kamaraina277)*
