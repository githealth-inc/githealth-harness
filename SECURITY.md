# Security and clinical safety

**MVP restriction:** synthetic data only. Never commit real patient data, access tokens, credentials or secrets. This project is not authorized for production clinical use.

- Fail closed when ontology, policy or authority checks cannot complete.
- No direct model-to-clinical-action pathway. Consequential care actions require separately verified authority and appropriate human approval.
- Keep policy and protocol versions in every decision record.
- Protect evidence references, logs and approval identities with least-privilege access.
- Avoid claiming tamper-proof or cryptographically sealed logs until implemented and tested.
- Dependency scanning, secret scanning, code review and protected branches should be configured before accepting outside contributions.

To report a vulnerability, contact the repository owner privately; do not post sensitive details in public issues.
