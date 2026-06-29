# Project Meridian — PMO AI Agent Architecture

A **sanitized, end-to-end architecture artifact** for a production AI agent that
replaces inaccurate BI-copilot output with a governed, grounded query agent. This repo
is a *design portfolio piece* — architecture, threat model, and cost model — not client
code. All identifying details removed.

> For an AI Solutions Architect, the design document is the deliverable. This shows how
> I scope, secure, cost, and phase a production agent.

## Problem

A PMO's out-of-the-box BI copilot produced confidently-wrong answers over a semantic
model with underlying data-quality issues. Shipping it as-is would erode trust. The
architecture below fixes the data layer first, then grounds an agent on top.

## 10-phase architecture

1. **Discovery** — stakeholder workshop, current-state pain, success criteria
2. **AI-readiness assessment** — semantic-model data-quality audit (the key gate)
3. **Northstar definition** — measurable target outcome
4. **Layer-by-layer system design** — retrieval, agent, grounding, presentation
5. **Component spec** — failure modes + cost drivers per component
6. **Agent workflow** — system prompt, tool definitions, decomposition logic
7. **Zero-trust security** — Row-Level Security identity propagation, least-privilege
   service principals, defense-in-depth, data-sovereignty controls
8. **EU AI Act classification** — risk tier + obligations mapping
9. **Bottom-up cost model** — token + infra costs with ROI analysis
10. **Six-sprint delivery roadmap** — Phase 1 scope and sequencing

## The judgment call (the part interviewers care about)

The semantic model had data-quality defects. Rather than ship an agent that would be
*confidently wrong*, the recommendation was to **delay delivery to remediate the data
layer first**. A grounded agent on bad data is worse than no agent — it launders errors
into authoritative-sounding answers. Fixing the foundation was the responsible call.

## What's in this repo

```
ARCHITECTURE.md       full 12-section design document
diagrams/             system, security, and data-flow diagrams
threat-model.md       zero-trust threat model
cost-model.md         bottom-up cost + ROI
eu-ai-act.md          risk classification + obligations
```

## Governance highlights

- Row-Level Security identity propagation through the agent
- Least-privilege service principals
- EU AI Act risk classification with mapped obligations
- Auditability of every agent action

---

*All client-identifying details removed. This is a reference architecture for
demonstration and portfolio purposes.*
