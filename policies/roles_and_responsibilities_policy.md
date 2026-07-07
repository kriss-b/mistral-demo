# Roles and Responsibilities Policy

## 1. Purpose
This policy defines the roles and responsibilities for information security within the Company to ensure accountability and compliance with **ISO 27001:2022 (Controls A.5.2 — Information security roles and responsibilities, and A.5.3 — Segregation of duties)**.

## 2. Scope
This policy applies to all employees, contractors, and third parties involved in the implementation, maintenance, and oversight of the Information Security Management System (ISMS).

## 3. Roles and Responsibilities

Mistral AI is a frontier AI lab. Its role structure reflects a research-intensive organisation that trains and operates foundation models as its core business. Named individuals are recorded separately; this policy defines the roles and their accountabilities. Where a single person holds more than one role, segregation of duties is preserved through independent review and approval (see A.5.3).

### 3.1 Executive Leadership
#### **CEO (Chief Executive Officer)**
- Provide overall leadership and resources for the ISMS and AIMS.
- Approve information security and AI policies and strategic decisions.
- Ensure alignment between business objectives, responsible AI, and information security.

#### **COO (Chief Operating Officer)**
- Oversee the implementation of security policies and procedures.
- Ensure operational processes, including supplier management, align with information security requirements.
- Coordinate with the CISO and ISMS Owner to address security risks.

---

### 3.2 Information Security Leadership
#### **CISO (Chief Information Security Officer)**
- Lead the development, implementation, and maintenance of the ISMS.
- Report on the performance of the ISMS to executive leadership.
- Ensure compliance with ISO 27001:2022 and other relevant standards.
- Oversee incident response and risk management activities, including protection of model weights and training infrastructure against exfiltration.
- Define security requirements for AI systems, including adversarial-testing standards (see the **[Secure AI Development Policy](../iso42001/policies/secure_ai_development_policy.md)**).

#### **ISMS Owner**
- Act as the primary point of contact for the ISMS.
- Coordinate internal audits and management reviews.
- Monitor the effectiveness of the ISMS and drive continuous improvement.
- Ensure policies and procedures are up-to-date and aligned with ISO 27001:2022.

#### **DPO (Data Protection Officer)**
- Ensure compliance with data protection regulations (GDPR) in the Company's roles as both controller and processor.
- Oversee data protection impact assessments (DPIAs), including for customer prompts, API data, and training data containing personal data.
- Act as the point of contact for data subjects and the supervisory authority (CNIL).
- Monitor compliance with the **[Data Protection Policy](data_protection_policy.md)**.

---

### 3.3 Technical and Research Leadership
#### **CTO (Chief Technology Officer)**
- Oversee the implementation of technical security controls across the platform, production serving stack, and owned compute infrastructure (Mistral Compute).
- Ensure secure development and MLOps practices are followed.
- Collaborate with the CISO to address technical risks.
- Approve changes to IT and compute infrastructure and systems.

#### **Chief Science Officer / Head of Research**
- Own the security and governance of model training pipelines, datasets, and model weights.
- Ensure training-data governance, provenance, and quality requirements are met (see the **[Secure AI Development Policy](../iso42001/policies/secure_ai_development_policy.md)**).
- Approve, with the CTO and CISO, the release or open-weight publication of models.

#### **Head of AI Safety / Responsible AI Lead**
- Own the responsible-AI and AI-safety dimension of the AIMS, including model evaluation, red-teaming, and impact assessments.
- Ensure prompt/output safety controls and misuse mitigations are defined and effective.
- Coordinate AI incident response with the CISO for AI-specific incidents (e.g., harmful output, prompt injection, model misuse).

---

### 3.4 Human Resources
#### **Chief People Officer (CPO)**
- Ensure employees complete information security and AI-safety training.
- Oversee background checks and onboarding/offboarding processes.
- Collaborate with the CISO to address human resource security risks, including for staff with access to model weights.

---

### 3.5 Policy Owners
Each information security policy has a designated **owner** responsible for its maintenance, implementation, and review. The owner is identified in the Changelog at the end of each policy document.

---

## 4. Compliance
Non-compliance with this policy may result in disciplinary action, up to and including termination of employment or contracts.

## 5. Review and Updates
This policy will be reviewed annually or after significant changes to organizational structure or roles.


---

## Changelog

| Version | Date | Owner | Approver | Changes |
|---------|------|-------|----------|---------|
| 1.0 | TBD | ISMS Owner | ISMS Owner | Initial version |
| 1.1 | 2026-07-07 | ISMS Owner | ISMS Owner | Adapted roles to Mistral AI's research-lab structure: added Chief Science Officer/Head of Research and Head of AI Safety, expanded CISO/DPO/CTO responsibilities, removed CMO |
