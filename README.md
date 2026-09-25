# Yu-Hsiang Tang

**AI Platform & Automation Engineer** · Hsinchu, Taiwan

I design the control layer around AI agents: acceptance gates, execution
harnesses, verification, and recovery, so that agent work stays reliable past
the first demo. I build with AI coding agents (Claude Code, Codex) and own the
architecture, review, and verification.

## What I am building

**PACP (Personal Agent Control Plane)** runs my day-to-day engineering. It turns
an ambiguous request into acceptance-checkable goals and keeps Codex and Claude
Code delivering across independent projects, sessions, and machines. It then
stops them when they drift, loop, or over-engineer.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/pacp-control-plane-dark.svg">
  <img alt="PACP flow: owner intent becomes a Goal Ladder; an agent session works the running goal; a convergence gate counts only accepted items and returns COMPLETE, CONTINUE, REALIGN, or CIRCUIT_BREAK; a Task Footer records one validated state, is enforced by Claude Code hooks, and rebuilds a fresh session when context runs out." src="assets/pacp-control-plane-light.svg">
</picture>

- **Goal Ladder**: breaks one objective into ordered goals. Each goal unlocks
  only after the previous one passes independent verification, never because
  the model reports it is done.
- **Session continuation**: when a session runs out of context, a fresh one is
  rebuilt from the Issue, Git checkpoint, and handoff, then verified against the
  recorded task state before work moves to it.
- **Task Footer**: one validated task state, rendered as the next agent's
  handoff and as a status view for me. Claude Code hooks enforce it; it does
  not depend on the model remembering a prompt rule.

PACP's source is not public. It is governed by 25 architecture decision records
and 16 feature specifications, with 677 automated tests passing.

## Open source

**[Canopus](https://github.com/Hsiang-Tang/canopus)** is the open-source core of
PACP: frozen acceptance envelopes, convergence gates, circuit breakers, and a
Claude Code Stop-hook latch. It uses only the Python standard library, takes
about 15 minutes to adopt, and replays four failure scenarios. Every behavior
maps to a test.

## Other work

- **Network agent validation**: for an AI field-application agent, created faults
  and configuration errors on real access points, controllers, and switches,
  then scored the agent's API calls against the expected fix. A run counts as
  correct only when the network is repaired.
- **Retrieval**: moved an internal RAG wiki from vector search to index-based
  retrieval to improve retrieval quality.
- **[Alphalia](https://apps.apple.com/tw/app/alphalia/id6804235042)**: a
  local-first SwiftUI iPhone app, taken from first definition to App Store
  release.

## Background

Field Application Engineer on networking products, then AI Engineer across RAG,
LLM workflows, and Kubernetes deployment, now focused on agent systems.
M.S. in Learning Sciences and Technologies, National Tsing Hua University.

**Tools**: Claude Code · Codex · Python · FastAPI · Docker · Kubernetes ·
OpenSearch · Ollama · GitHub Actions · SwiftUI
