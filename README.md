# chatgpt_app_and_agentic_registry

A structured, versioned registry that defines my tech stack for ChatGPT-assisted and agentic workflows.

This repo is the **source of truth** for:
- Tool catalog (apps, models, agents)
- Routing heuristics (when to use what)
- Safety / escalation policies (what requires confirmation)
- IO contracts (how tools should be invoked and what they should return)
- Workflow blueprints (repeatable orchestrations)

---

## Repo structure

```text
registry/
  master.yaml                         # Canonical registry (source of truth)

schemas/
  agentic-policy-registry.schema.json # JSON Schema used to validate master.yaml

.github/workflows/
  validate.yaml                        # CI: yamllint + schema validation
