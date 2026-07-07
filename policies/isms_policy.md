# Information Security Management System (ISMS) Policy

## 1. Purpose
This document defines the overarching policy governing the Information Security Management System (ISMS) of **Mistral AI**. It serves as the master policy for information security, providing the framework within which all other information security policies, procedures, and controls operate.

This policy is aligned with **ISO 27001:2022 (Clauses 4, 5, 6, 8, 9 and 10)** and supports the Company's commitment to protecting the confidentiality, integrity, and availability of information assets — most critically its model weights, training data, and the customer prompts and personal data processed through its products.

---

## 2. Introduction & Objectives

Mistral AI is committed to establishing, implementing, maintaining, and continually improving its ISMS in accordance with ISO 27001:2022. As a frontier AI lab, the Company also operates an AI Management System (AIMS) aligned with **ISO 42001:2023**; the ISMS and AIMS share a single risk register and interface closely (see the **[AIMS Policy](../iso42001/policies/aims_policy.md)**).

The following are the information security objectives for the current annual period. They are reviewed and updated at each management review (see Section 10).

- Maintain zero critical or high security incidents, with particular focus on preventing unauthorised access to or exfiltration of model weights and training data.
- Maintain ISO 27001:2022 certification with no critical non-conformities, and progress ISO 42001:2023 (AIMS) certification readiness.
- Achieve 100% completion of security and AI-safety awareness training across all employees by year-end.
- Zero orphaned or unauthorised accounts found during quarterly access reviews of production and model-storage systems.
- Maintain 99.9% availability of La Plateforme (developer API) and Le Chat.
- Ensure all services and data processing remain hosted exclusively within the European Union.

---

## 3. Context of the Organisation

Mistral AI is a frontier artificial intelligence lab headquartered in Paris, France. The Company researches, trains, and deploys open-weight and commercial large language models (the Mistral and Mixtral families and their successors) and delivers them through products including **Le Chat** (its consumer and enterprise assistant, available on web, iOS, and Android) and **La Plateforme** (its developer API). The Company operates in the artificial intelligence and foundation-model sector.

The Company develops, trains, and deploys AI systems as its core business. It processes customer prompts, API request data, and personal data, acting as both **data controller** (e.g., for its own users and Le Chat consumers) and **data processor** (e.g., for enterprise and API customers). All services and data processing are hosted **exclusively within the European Union**, supporting the Company's European digital-sovereignty positioning.

The Company operates its own GPU compute and data-centre capacity (Mistral Compute) alongside third-party cloud and hardware partners. Its most valuable assets are its model weights, training pipelines and datasets, research intellectual property, and the confidentiality of customer data.

The ISMS has been designed to reflect the Company's scale, high growth rate, research-intensive culture, and risk profile as a high-value target for sophisticated adversaries, balancing security requirements with the pace of AI research and product development.

---

## 4. Internal & External Issues

The following issues are considered in defining the scope and objectives of the ISMS.

### 4.1 Internal Issues

| Issue | Impact on ISMS |
|-------|----------------|
| Model weights and training pipelines are the Company's crown-jewel assets | Requires strong access control, segregation, monitoring, and exfiltration prevention around model storage and training infrastructure |
| Rapid headcount growth and scaling | Onboarding, access provisioning, and awareness training must scale without weakening controls |
| Fast research and product iteration pace | Security must be embedded into research and MLOps workflows without blocking innovation (DevSecOps / MLSecOps) |
| Hybrid estate: own compute (Mistral Compute) plus third-party clouds | Shared-responsibility boundaries must be defined and managed across owned and rented infrastructure |
| Large-scale processing of customer prompts and personal data | Strong data classification, minimisation, retention, and privacy controls required |
| Distributed and hybrid workforce | Increased endpoint, identity, and remote-access control requirements |
| High reliance on GPU compute supply and data-centre partners | Concentration and availability risk in the compute supply chain |

### 4.2 External Issues

| Issue | Impact on ISMS |
|-------|----------------|
| GDPR (as both controller and processor) | Strict requirements on lawful basis, data-subject rights, processor obligations, and breach notification |
| EU AI Act (as a provider of general-purpose AI / foundation models) | Obligations on GPAI model documentation, transparency, systemic-risk assessment, and incident reporting |
| Intense, well-funded competition and high public visibility | Elevated threat of targeted attacks, IP theft, and espionage against the Company |
| Threat landscape targeting frontier AI labs (incl. nation-state actors seeking model weights) | Advanced, persistent adversaries require defence-in-depth and continuous monitoring |
| Enterprise customer contractual and assurance requirements | Customers require evidence of ISO 27001 / SOC 2 and responsible-AI governance |
| European digital-sovereignty expectations | Commitment to EU-only hosting and data residency is a market and regulatory expectation |
| Third-party and supply-chain risks (compute, data centres, cloud distribution) | Vendors, hardware and data-centre partners shall meet security and continuity standards |
| Model misuse and dual-use concerns | Public and regulatory scrutiny of how released models could be misused |
| Climate change (ISO/IEC 27001:2022/AMD 1:2024) | The organization shall determine whether climate change is a relevant issue affecting its context. Given the energy intensity and physical footprint of AI data centres, climate-related risks (e.g. extreme weather or energy disruption affecting data centres and supply chains) shall be assessed and treated within the risk management process. |

---

## 5. Interested Parties

The following interested parties have been identified as having requirements relevant to information security.

| Interested Party | Key Requirements |
|-----------------|-----------------|
| Enterprise and API customers | Confidentiality and integrity of their data and prompts; EU data residency; evidence of security and AI-governance compliance |
| Developers using La Plateforme | Secure, reliable API; clear data-handling terms; protection of API credentials |
| Le Chat users and data subjects | Protection of personal data; transparency about AI processing; data-subject rights under GDPR |
| Employees and contractors | Clear security policies; safe and secure working environment |
| Regulators (e.g., CNIL, EU AI Office, national competent authorities) | Compliance with GDPR and the EU AI Act |
| Law enforcement authorities | Cooperation in the event of a security incident or criminal investigation |
| Special interest groups (e.g., CERTs, ISACs, AI-safety and security communities) | Threat intelligence sharing; awareness of emerging vulnerabilities and AI-specific threats |
| Compute, hardware, and data-centre partners | Clear contractual security obligations; coordinated incident notification |
| Cloud distribution partners (model hosting/marketplaces) | Defined shared-responsibility boundaries; timely incident notification |
| Investors and board | Adequate risk management; protection of IP; business continuity assurance |
| Open-source and research community | Responsible release practices; integrity of published model artefacts |
| Certification body | Compliance with ISO 27001:2022 (and ISO 42001:2023) requirements |

### 5.1 Contact with Authorities
The ISMS Owner and CISO are responsible for maintaining appropriate contacts with relevant authorities, including the data protection supervisory authority (CNIL), the EU AI Office and national competent authorities under the EU AI Act, law enforcement, and national cybersecurity agencies (e.g., ANSSI, CERT-FR). These contacts shall be activated in the event of a significant security incident, personal-data breach, or serious AI incident, or when required by applicable law. Contact details are maintained by the Legal & Compliance function and reviewed annually.

### 5.2 Contact with Special Interest Groups
The CISO is responsible for maintaining membership of, or engagement with, relevant security special interest groups, such as national CERTs, sector-specific ISACs, AI-safety forums, and professional security communities. This ensures the Company remains informed of emerging threats, vulnerabilities, and both conventional and AI-specific security best practices. Threat intelligence gathered through these channels feeds into the risk assessment process.

---

## 6. Dependencies & Interfaces

The ISMS does not operate in isolation. It interfaces with the following internal functions and external systems:

- **Legal & Compliance / DPO**: GDPR and EU AI Act monitoring, contract review, DPIAs, NDA management.
- **Human Resources**: Onboarding, offboarding, training, and disciplinary processes.
- **Research & Engineering**: Model training, MLOps, implementation of technical controls, secure development, and patch management.
- **Platform & Infrastructure (Mistral Compute)**: Security of owned data-centre and GPU infrastructure and the production serving stack.
- **Finance & Procurement**: Vendor assessment and contractual security requirements.
- **Executive Leadership**: Resource allocation, risk acceptance, and strategic alignment.
- **Cloud, hardware, and data-centre partners**: Shared-responsibility model, security configurations, and incident coordination.
- **AIMS (ISO 42001)**: The ISMS operates alongside the AIMS; AI-specific risks feed into the shared risk register and interested-party analysis.

---

## 7. Scope of the ISMS

### 7.1 In Scope

**Systems**
- Foundation-model training pipelines, datasets, and model weight/artefact storage.
- La Plateforme (developer API) and its serving infrastructure.
- Le Chat (web, iOS, Android) and supporting services.
- Mistral Compute — owned GPU and data-centre infrastructure used for training and inference.
- Third-party cloud regions and hosting used for serving and internal workloads (EU only).
- Internal tools (CI/CD, MLOps, monitoring, code repositories, collaboration and SaaS platforms).
- Customer prompts, API data, user accounts, and personal data.
- Corporate IT and office network infrastructure.

**People**
- All employees and contractors of the Company (research, engineering, product, platform/infrastructure, go-to-market, and corporate functions).
- Third-party vendors and partners with access to Company systems or data.

**Locations**
- Paris headquarters (primary place of business).
- Company and partner data centres within the European Union (e.g., France and Sweden).
- Remote workstations (employees working from home or other locations).
- Third-party cloud data centres (EU regions), under a shared-responsibility model.

### 7.2 Out of Scope
- Physical security of employee home offices.
- Personal devices not used for work.
- Third-party AI products used by customers that are not integrated into Company services.

### 7.3 Justification
The ISMS covers all digital assets and processes critical to the Company's models, products, and customer data, including its owned compute infrastructure and its use of third-party EU cloud. Remote working locations are included in scope for logical and endpoint security controls, but physical security of individual home offices is outside the Company's direct control and is therefore excluded.

---

## 8. Locations

The ISMS applies to the following locations:

| Location | Type | In Scope |
|----------|------|----------|
| Paris headquarters | Primary place of business | Full scope (physical and logical) |
| EU data centres (owned and partner, e.g. France, Sweden) | Training and production compute | Physical and logical controls; shared responsibility with data-centre partners |
| Remote working locations | Employee home offices and other remote sites | Logical and endpoint security controls only |
| Third-party cloud data centres (EU regions) | Hosted by cloud providers | Logical controls and shared responsibility |

---

## 9. Governance

| Role | Accountability | Name |
|------|---------------|------|
| **ISMS Owner** | Overall accountability for the ISMS | _TBD_ |
| **CISO** | Technical and operational implementation of information security | _TBD_ |
| **CTO** | Platform, infrastructure, and production security | _TBD_ |
| **DPO** | GDPR and personal-data protection | _TBD_ |
| **CEO** | Executive oversight; approves the ISMS Policy | _TBD_ |
| **All employees and contractors** | Comply with information security policies and report security events | — |

Full role definitions are documented in the **[Roles and Responsibilities Policy](roles_and_responsibilities_policy.md)**.

---

## 10. Executive Management Review

The executive team conducts a formal **management review of the ISMS** at least once per year. The review covers:

- Results of internal audits and security assessments.
- Status of actions from previous reviews.
- Feedback from interested parties, including customers and regulators.
- Risk assessment results and treatment plan status (including AI-specific risks shared with the AIMS).
- Performance against information security objectives.
- Changes in internal and external context that may affect the ISMS.
- Opportunities for continual improvement.
- Resource adequacy.

Outputs of the management review include decisions on ISMS improvements, resource allocations, and updates to policies or objectives. Review minutes are documented and retained.

---

## 11. Activities of the ISMS

The ISMS operates through the following recurring activities:

| Activity | Frequency | Owner |
|----------|-----------|-------|
| Risk assessment review | Annual (or after significant change) | ISMS Owner |
| Internal audit | Annual | ISMS Owner / CISO (see [audit_policy.md](audit_policy.md)) |
| Management review | Annual | CEO / ISMS Owner |
| Policy and documented information review | Annual (or after significant change) | Policy owners / ISMS Owner |
| Security and AI-safety awareness training | Annual (onboarding + refresh) | CPO |
| Supplier security review | Annual | COO |
| Backup and recovery testing | Quarterly | CTO |
| Incident response exercises | Annual | CISO |
| Vulnerability scanning and patching | Ongoing | CTO |
| Access rights review (incl. model-storage and production systems) | Quarterly | CTO |

---

## 12. Description of Activities

### 12.1 Risk Assessment
Risks to the confidentiality, integrity, and availability of information — including AI-specific risks — are identified, assessed, and treated in accordance with the **[Risk Assessment Policy](risk_assessment_policy.md)** and **[Risk Assessment Procedure](../risks/risk_assessment_procedure.md)**. Results are documented in the **[Risk Register](../risks/risks_register.md)**, which is shared with the AIMS.

### 12.2 Internal Audit
Internal audits verify that the ISMS is implemented and maintained effectively and in conformance with ISO 27001:2022. Findings are reported to executive management and tracked to resolution.

### 12.3 Policy and Documented Information Management
All ISMS policies and documented information (procedures, plans, templates, registers, and records) are reviewed at least annually. Policy owners are responsible for initiating reviews and obtaining approval from the ISMS Owner. Documented information shall be created, updated, controlled, and retained in a manner that ensures it remains accurate, accessible, and fit for purpose. Version history is maintained in the Changelog of each document.

### 12.4 Security Awareness Training
All employees complete information security and AI-safety awareness training upon onboarding and at least annually thereafter, as defined in the **[Employee Training Procedure](../procedures/employee_training_procedure.md)**.

### 12.5 Incident Management
Security incidents are managed in accordance with the **[Incident Management Policy](incident_management_policy.md)** and **[Incident Response Plan](../incidents/incident_response_plan.md)**.

### 12.6 Supplier Management
Third-party suppliers with access to Company systems or data — including compute, hardware, data-centre, and cloud distribution partners — are assessed for security risks in accordance with the **[Supplier Security Policy](supplier_security_policy.md)**.

### 12.7 Nonconformity and Corrective Actions
Nonconformities identified from any source (audits, incidents, management reviews, or employee feedback) shall be recorded, root-caused, and resolved by the responsible owner. Corrective actions are tracked to resolution by the ISMS Owner and reported at the next management review. Audit-related nonconformities follow the process defined in the **[Audit Policy](audit_policy.md)**.

### 12.8 Performance Monitoring and Measurement
The ISMS Owner monitors and measures information security performance on an ongoing basis. Key inputs include audit results, incident metrics, vulnerability scan outcomes, access rights review findings, and training completion rates. Results are consolidated and presented at the annual management review to evaluate whether information security objectives are being met and to identify areas for improvement.

### 12.9 Continual Improvement
Improvement opportunities are identified from all ISMS activities, including audits, incidents, risk assessments, management reviews, and performance monitoring. The ISMS Owner maintains a log of improvement opportunities, prioritises them based on risk and impact, and tracks their implementation. Progress is reviewed at each management review to ensure the ISMS remains effective, relevant, and aligned with the Company's objectives.

---

## 13. Risks of the ISMS

The following risks to the effective operation of the ISMS have been identified:

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Security controls unable to keep pace with rapid scaling and hiring | Medium | High | Scalable IAM and onboarding; annual resource review at management review |
| Key person dependency (ISMS Owner / CISO) | Medium | High | Document processes; cross-train team members |
| Security friction slows research and product delivery, driving workarounds | Medium | Medium | Embed security into MLOps/DevSecOps; risk-based, proportionate controls |
| Low security or AI-safety awareness among staff | Medium | Medium | Mandatory annual training programme |
| Scope creep or unmanaged changes across a fast-moving estate | Medium | High | Change management policy enforced |
| Failure to keep policies up to date with GDPR / EU AI Act developments | Medium | High | Annual review cycle with assigned owners and regulatory monitoring |

---

## 14. Opportunities of the ISMS

The following opportunities have been identified through the operation of the ISMS:

- **Customer trust and competitive differentiation**: ISO 27001 (and ISO 42001) certification enables Mistral AI to demonstrate security and responsible-AI maturity to enterprise customers and regulators, and to win business in regulated sectors.
- **European sovereignty positioning**: A demonstrably secure, EU-hosted ISMS reinforces the Company's digital-sovereignty value proposition.
- **Reduced incident impact**: Mature detection and response capabilities reduce the cost and reputational impact of security incidents, including model-weight and data-related events.
- **Regulatory readiness**: A strong ISMS simplifies compliance with GDPR and the EU AI Act.
- **Operational efficiency**: Documented processes and controls reduce ad-hoc decision-making and improve consistency across a fast-scaling organisation.
- **Supplier confidence**: A certified ISMS strengthens the Company's position in negotiations with compute, hardware, and cloud partners.

---

## 15. Compliance
Non-compliance with this policy may result in disciplinary action, up to and including termination of employment or contracts.

## 16. Review and Updates
This policy will be reviewed annually or following significant changes to the organisation, its context, or the threat landscape.

---

## Changelog

| Version | Date | Owner | Approver | Changes |
|---------|------|-------|----------|---------|
| 1.0 | TBD | ISMS Owner | ISMS Owner | Initial version |
| 1.1 | 2026-07-07 | ISMS Owner | ISMS Owner | Tailored context, scope, issues, interested parties, and objectives to Mistral AI |
