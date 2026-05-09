# DIKWP SemanticEnergy OS

Open-source AI semantic value, cost, carbon, and purpose-governance monitor.

DIKWP SemanticEnergy OS helps teams answer a hard question:

> Did this AI workload produce enough evidence-backed semantic value to justify its token, cost, energy, privacy, and governance burden?

It is not a hardware power meter. It is a white-box governance prototype that combines:

- DIKWP registration: Data, Information, Knowledge, Wisdom, Purpose, Reliability.
- AI FinOps: cost, token, model, retry, and tool-call tracking.
- Green AI governance: estimated joules and carbon, with stronger proof when telemetry is supplied.
- Semantic value scoring: purpose coupling, evidence support, redundancy, unsupported-claim risk, privacy risk.
- Portfolio policy: semantic budget, event-level recommendations, and governance thresholds.

## Why this matters

Generative AI and agentic workflows can burn money, tokens, time, and energy while producing unsupported or low-value outputs. Traditional FinOps can see the bill. Traditional observability can see latency. DIKWP SemanticEnergy OS tries to see the missing middle: whether the output was semantically worth the cost.

## Install

```bash
pip install -e .
```

Optional dashboard:

```bash
pip install -e .[app]
streamlit run src/dikwp_semanticenergy/app.py
```

## Run demo

```bash
dikwp-semanticenergy analyze examples/sample_ai_workflow_log.json \
  --policy configs/default_policy.json \
  --out outputs/demo
```

Generated outputs:

- `semantic_energy_report.json`
- `event_scores.csv`
- `recommendations.md`
- `semantic_budget_policy.json`

## Static boundary audit

```bash
dikwp-semanticenergy static-audit src --out outputs/demo/static_boundary_audit_report.json
```

## Key metrics

- **Purpose Coupling**: whether the output is aligned with P-layer goal, value, constraints, time horizon, and feedback.
- **Evidence Support**: whether claims have sources or evidence custody.
- **Redundancy Score**: whether prompts and outputs are bloated or repetitive.
- **Unsupported Claim Risk**: unsupported certainty, guarantees, best/only claims, or claim-like statements without evidence.
- **Semantic Energy Score**: semantic value adjusted by estimated energy burden.
- **Waste Index**: 1 - weighted semantic-energy score.

## Boundary

This project is designed for governance and optimization. It does not claim exact joule measurement unless hardware telemetry is supplied. It does not remove privacy, safety, evidence, or human-review controls in the name of cost reduction.

## Attribution

This project preserves attribution to the DIKWP model associated with Yucong Duan. Confirm formal authorship, trademark, and licensing arrangements before official release under a specific account or organization.
