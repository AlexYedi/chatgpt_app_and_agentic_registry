# Agentic Policy Registry

This repo is a structured catalog of models/tools/agents with routing heuristics, constraints,
interfaces, and safety guardrails.

## Canonical file
- `registry/master.yaml` (source of truth)

## How to use with ChatGPT (this chat)
1. Upload `registry/master.yaml` directly into the chat when you want it applied.
2. Ask: “Use the policy registry to route this task. Output:
   - selected tool_id
   - decision rationale (bullets)
   - the handoff artifact as JSON.”

### Recommended prompt pattern
Paste this above a task:

**Policy Context:** (attached: `registry/master.yaml`)
**Task:** <what you want>
**Output Contract:** JSON with:
- `selected_tool_id`
- `decision_trace` (bullets)
- `handoff_artifact` (object)

## How to use with orchestrators
- Parse `registry/master.yaml` into your router (n8n, a custom service, etc.)
- Enforce schema validation in CI using the included workflow.
