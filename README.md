# GitHealth Harness™
## The Healthcare Trust and Execution Layer for AI Agents

**AI can propose. Experts authorize. GitHealth proves what happened.**

GitHealth is a proposed model-agnostic infrastructure layer for governed healthcare AI: formal healthcare ontologies, policy enforcement, expert authority, agent execution, provenance, outcome measurement and AI economics. **Status: MVP development, not a production clinical system.**

General-purpose harnesses make agents extensible. GitHealth is designed to make their healthcare actions governable, traceable and measurable. Compatible agent runtimes (potentially including DeepSeek Harness) sit below GitHealth's versioned healthcare-specific contracts; no particular runtime is required.

## Architecture
```text
Data + expertise + protocols + workflows
  → Model / agent proposes
  → Formal healthcare ontology validates semantics
  → Policy engine evaluates constraints
  → Authority check and human approval where required
  → Authorized execution
  → Provenance + evidence references
  → Outcome evaluation + AI economics
```

The model reasons. The ontology defines permitted semantic structure. Policy defines what is allowed. Authority determines who can act. GitHealth records what happened. **Ontology validation and cryptographic integrity do not establish clinical truth or correctness.**

## Product surfaces
- **Studio — Build:** agents, protocols, ontology, policy, evaluations.
- **Live — Run:** governed execution, approval queue, monitoring.
- **Prove — Prove:** evidence lineage, outcome evaluation and costs.
- **WoundOS:** first clinical demonstrator, using synthetic wound-care data.
- **AION:** proposed authority and interoperability capabilities within the Harness, not a separate competing runtime.

## First demonstrator
One synthetic wound-care episode: intake → ontology validation → protocol recommendation → policy check → expert approval → simulated action → provenance → outcome → cost. No real PHI and no autonomous treatment authorization.

[Architecture](docs/architecture/OVERVIEW.md) · [MVP roadmap](docs/roadmap/MVP.md) · [Security](SECURITY.md)

**Development status:** specifications and prototype work only. No claim of clinical validation, HIPAA compliance, or production readiness.
