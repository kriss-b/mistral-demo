# AI Systems Register

Inventory of AI systems in use or under development. One row per system. Update rows in place when status or classification changes.

Scope follows [isms_policy.md](../../policies/isms_policy.md) section 7.1. Governance of these systems is defined in [aims_policy.md](../../iso42001/policies/aims_policy.md); impact assessments follow [ai_system_impact_assessment_template.md](../../iso42001/procedures/ai_system_impact_assessment_template.md). Supports ISO 42001 A.5.3, A.5.4 and A.5.5 via the checks in [iso42001/checks](../../iso42001/checks).

**Risk Level** records the Company's own assessment. Where an EU AI Act classification is also relevant it is noted in the Notes column; the two are tracked separately because the regulatory category and the Company's internal risk rating do not always coincide.

| AI System ID | Name | Owner | Purpose | Deployment Context | Risk Level | Status | Last reviewed | Impact Assessment Link | Notes |
|--------------|------|-------|---------|--------------------|------------|--------|---------------|------------------------|-------|
| AI-001 | Foundation model training pipeline | Chief Science Officer / Head of Research | Pre-training and post-training of the Company's general-purpose models, including dataset ingestion, curation, and evaluation. | Internal only — training clusters on Mistral Compute and EU cloud regions. Not customer-facing. | High | Active | TBD | — (not yet performed) | Produces the model weights treated as the crown-jewel asset in RISK-001. Training data provenance and copyright exposure assessed here rather than per downstream product. |
| AI-002 | La Plateforme — model serving API | CTO | Developer-facing API providing inference, fine-tuning, and embeddings over the Company's models. | External — customers and partners, EU-hosted serving infrastructure. | High | Active | TBD | — (not yet performed) | GPAI obligations under the EU AI Act apply to the models served here. Customer prompts and API data in scope for GDPR; see [data_protection_policy.md](../../policies/data_protection_policy.md). |
| AI-003 | Le Chat — assistant | CTO | Consumer and business conversational assistant across web, iOS, and Android. | External — general public and business users. | High | Active | TBD | — (not yet performed) | Highest direct exposure to individuals and therefore the priority for the A.5.4 individual and group impact assessment. Transparency obligations apply (users must know they interact with an AI system). |
| AI-004 | Fine-tuning and customisation service | CTO | Customer-initiated adaptation of Company models on customer-supplied data. | External — customers, EU-hosted. | Medium | Active | TBD | — (not yet performed) | Customer data is processed under the shared-responsibility model; the resulting adapted weights are customer-controlled. Supplier and contractual boundaries per [supplier_security_policy.md](../../policies/supplier_security_policy.md). |
| AI-005 | Content moderation and safety classifiers | Head of AI Safety / Responsible AI Lead | Detection and filtering of prohibited content across Le Chat and La Plateforme. | Internal component of external services. | Medium | Active | TBD | — (not yet performed) | False negatives carry societal impact and false positives carry individual impact; relevant to both A.5.4 and A.5.5. |
| AI-006 | Internal AI developer and productivity tooling | CTO | Third-party and internal AI assistants used by staff for coding and internal workflows. | Internal only — employees and contractors. | Medium | Active | TBD | — (not yet performed) | Use governed by [acceptable_use_policy.md](../../policies/acceptable_use_policy.md). Third-party AI tooling is also tracked in [suppliers_register.md](suppliers_register.md). |

**Impact assessments are not yet performed for any registered system.** This is a known and deliberate gap: the register is being established first so that assessment coverage can be measured against it. The ISO 42001 A.5.3, A.5.4 and A.5.5 checks will fail until assessments are completed, and should be treated as the tracking mechanism for closing this gap rather than as unexpected failures. Assessment priority follows the Risk Level column, starting with AI-003.

---

## Changelog

| Version | Date | Owner | Approver | Changes |
|---------|------|-------|----------|---------|
| 1.0 | TBD | CTO | CEO | Initial version |
| 1.1 | 2026-08-22 | CTO | CEO | Populated the register with the six AI systems in ISMS scope; impact assessments recorded as outstanding |
