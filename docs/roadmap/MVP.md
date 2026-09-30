# Five-week MVP roadmap

**Objective:** one working, end-to-end, synthetic wound-care workflow; not a production EHR integration or autonomous clinical system.

- **Week 1 — Foundation:** architecture lock, ontology subset, agent manifest, local development environment, synthetic data.
- **Week 2 — Governed execution:** deterministic policy, authority checks, deny-by-default, human approval and execution state machine.
- **Week 3 — Provenance:** event schema, ingestion, model/protocol versions, evidence references, query and timeline.
- **Week 4 — Economics and Prove:** model/tool cost metering, goal-to-cost report, evaluation and outcome association.
- **Week 5 — WoundOS demonstrator:** synthetic case, proposed wound assessment, protocol eligibility, expert review, simulated execution, provenance and cost report.

## Acceptance criteria
1. Invalid ontology data is rejected with an explicit reason.
2. Unauthorized treatment actions cannot execute.
3. Human approval is recorded with approver identity and scope.
4. Every proposed and executed action has correlated provenance events.
5. An independent reviewer can reconstruct which data, model, protocol and authority informed an action.
6. Cost and outcome are linked to a task, with estimates distinguished from actual usage.
7. The demo uses only synthetic patient information.

## Deferred
Production EHR/HL7 FHIR integrations, real PHI, ZK circuits, blockchain settlement, x402, formal clinical validation and deployment certifications are separate workstreams.
