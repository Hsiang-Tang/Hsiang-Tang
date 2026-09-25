Building control planes that keep AI coding agents on goal across sessions,
engines, and machines.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/pacp-control-plane-dark.svg">
  <img alt="PACP flow: owner intent becomes a Goal Ladder; an agent session works the running goal; a convergence gate counts only accepted items and returns COMPLETE, CONTINUE, REALIGN, or CIRCUIT_BREAK; a Task Footer records one validated state, is enforced by Claude Code hooks, and rebuilds a fresh session when context runs out." src="assets/pacp-control-plane-light.svg">
</picture>

**[Canopus](https://github.com/Hsiang-Tang/canopus)** is the open-source core:
frozen acceptance envelopes, convergence gates, circuit breakers, and a Claude
Code Stop-hook latch, in standard-library Python.
