# Supplier Register

Current state of third-party suppliers. One row per supplier. Update rows in place when status changes. Suppliers are reviewed at least annually per the **[Supplier Security Policy](../../policies/supplier_security_policy.md)**.

These entries are an initial population of Mistral AI's key vendors across compute, infrastructure, and SaaS. None have yet undergone the Company's formal vendor security review (`Last reviewed` = ---); a first review date is planned for each. Certifications listed are typical for the vendor and must be verified during the review. Rows marked _(to confirm)_ in Notes are plausible but not yet verified against the actual vendor list.

| Supplier ID | Name | Department | Description | Certifications | Last reviewed | Next review | Status | Notes |
|-------------|------|------------|-------------|---------------|---------------|-------------|--------|-------|
| SUP-001 | NVIDIA | Platform & Infrastructure | GPU hardware and reference architectures for training and inference | ISO 27001 (verify) | --- | 2026-09-30 | Pending initial review | Compute/hardware; premier partner for GB-class GPUs |
| SUP-002 | Eclairion | Platform & Infrastructure | French data-centre partner hosting owned GPU capacity (Bruyères-le-Châtel) | ISO 27001 (verify) | --- | 2026-09-30 | Pending initial review | EU data centre; physical/environmental shared responsibility |
| SUP-003 | EcoDataCenter | Platform & Infrastructure | Swedish data-centre partner for AI infrastructure | ISO 27001 (verify) | --- | 2026-09-30 | Pending initial review | EU (Sweden) data centre |
| SUP-004 | Microsoft Azure | Platform & Infrastructure | Cloud distribution partner; hosts Mistral models on Azure AI (EU regions) | ISO 27001, SOC 2, ISO 42001 (verify) | --- | 2026-09-30 | Pending initial review | Cloud distribution; enforce EU-region data residency |
| SUP-005 | Google Cloud (Vertex AI) | Platform & Infrastructure | Cloud distribution partner for model serving (EU regions) | ISO 27001, SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | Cloud distribution; EU-only regions |
| SUP-006 | Amazon Web Services (Bedrock) | Platform & Infrastructure | Cloud distribution partner for model serving (EU regions) | ISO 27001, SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | Cloud distribution; EU-only regions |
| SUP-007 | Koyeb | Platform & Infrastructure | Serverless GPU cloud infrastructure | SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | Acquired by Mistral AI — confirm whether now internal vs. third-party |
| SUP-008 | Hugging Face | Research | Model artefact hosting and distribution for open-weight releases | SOC 2 Type II | 2025-01-15 | 2026-09-30 | Verified | SOC 2 Type II certified (Hub, Inference Endpoints, Serverless API). ISO 27001 not held. GDPR compliant. Report available under NDA from account team. Sources: [Security Docs](https://huggingface.co/docs/hub/en/security), [Compliance Guide](https://huggingface.co/blog/jeffboudier/soc2-iso27001-ai-compliance-guide) |
| SUP-009 | Black Forest Labs | Product | Third-party image-generation model (Flux) integrated into Le Chat | (verify) | --- | 2026-09-30 | Pending initial review | AI sub-processor; assess data handling & model governance |
| SUP-010 | GitHub | Engineering | Source code management and CI/CD | ISO 27001, SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | Source-code protection (A.8.4) |
| SUP-011 | Productivity & email suite (Google Workspace / Microsoft 365) | Corporate IT | Email, documents, and collaboration | ISO 27001, SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | _(to confirm which provider)_ |
| SUP-012 | Identity provider (SSO/IdP) | Corporate IT | Single sign-on and identity management | ISO 27001, SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | _(to confirm provider)_ |
| SUP-013 | Observability / monitoring platform | Platform & Infrastructure | Logging, metrics, and monitoring | SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | _(to confirm provider, e.g. Datadog/Grafana)_ |
| SUP-014 | Payments provider (e.g. Stripe) | Finance | Billing and payments for La Plateforme / Le Chat subscriptions | PCI-DSS, SOC 2 (verify) | --- | 2026-09-30 | Pending initial review | _(to confirm provider)_ |
| SUP-015 | Bitwarden | Corporate IT | Password / secrets management | ISO 27001, SOC 2 | --- | 2026-09-30 | Pending initial review | Listed as approved supplier in Supplier Security Policy |

---

## Changelog

| Version | Date | Owner | Approver | Changes |
|---------|------|-------|----------|---------|
| 1.0 | TBD | COO | CEO | Initial version |
| 1.1 | 2026-07-07 | COO | CEO | Populated initial supplier list (compute, infrastructure, cloud distribution, SaaS); all pending first vendor security review |
| 1.2 | 2025-01-15 | User | TBD | Verified Hugging Face (SUP-008) compliance: SOC 2 Type II certified, ISO 27001 not held, GDPR compliant |
