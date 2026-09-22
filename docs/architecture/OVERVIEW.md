# GitHealth architecture v0.1

## Position
Healthcare trust and execution layer above model-agnostic agent runtimes. DeepSeek Harness and other runtimes may be adapters, not hard dependencies.

## Boundaries
1. **Model/agent:** probabilistic proposals; never direct clinical authority.
2. **Ontology:** versioned types and relations for Patient, Encounter, Wound, Evidence, Protocol, Recommendation, Clinician, Authorization, CareEvent, Outcome and EconomicEvent. Validate proposed structured outputs; validation is not medical verification.
3. **Policy:** versioned, deterministic allow/deny/needs-review decisions with explicit reason codes. Fail closed on missing context.
4. **Authority:** verify identity, organizational role, scope, delegated permissions, patient-specific constraints and human approvals where applicable.
5. **Execution:** explicit state machine: proposed → validated → policy_checked → pending_approval → authorized → executed | denied | failed. Log each transition.
6. **Provenance:** append-only logical event history with stable IDs, source references, versions, decision traces and timestamps. Integrity guarantees require separate implementation and tests.
7. **Economics:** model usage, tool costs, execution time, human review time and outcomes. Estimates labeled as estimates.

## Adapter interface
`propose(context, agent_manifest) -> StructuredProposal`; GitHealth validates and authorizes before an executor may invoke consequential tools. Runtime adapters must not bypass policy or approval checks.

## Security
Synthetic data only during MVP. No real PHI in source control, fixtures or logs. Separate operational identifiers from patient identifiers. Secrets supplied via environment or secret manager. Audit log access restricted and monitored.

## MVP proof
Demonstrate a denied unauthorized treatment action and an approved simulated documentation action, each with a reconstructable evidence and authority trail.
