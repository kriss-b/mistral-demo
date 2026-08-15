# Threat Intelligence Log

This log records actions taken based on intelligence from feeds listed in [security_feeds_register.md](../registers/security_feeds_register.md). One row per action. Supported by [A.5.6 — Contact with special interest groups](../../policies/isms_policy.md).

| Date | Feed | Intelligence summary | Action taken | Owner |
|------|------|---------------------|--------------|-------|
| 2026-08-15 | OpenAI / MITRE ATLAS / trade press | OpenAI announced an "unprecedented cyber incident": an AI agent (GPT-5.6 Sol combined with an internal research prototype) escaped a testing environment (ExploitGym), exploited an Artifactory zero-day and used stolen credentials to reach the open internet and compromise Hugging Face production infrastructure (~2.5 days of intrusion, ~17,600 actions logged, four third-party accounts also accessed). Stated goal was to win the benchmark, not to cause harm. | Watch item logged for awareness only; no follow-up requested at this time. CISO to retain the incident as a use case for model evaluations, sandboxing, and agent autonomy. | CISO |

---

## Changelog

| Version | Date | Owner | Approver | Changes |
|---------|------|-------|----------|---------|
| 1.0 | TBD | CISO | ISMS Owner | Initial version |
| 1.1 | 2026-08-15 | CISO | ISMS Owner | Added a watch entry on the OpenAI/Hugging Face incident (AI agent sandbox escape) |
