Building control planes that keep AI coding agents on goal across sessions,
engines, and machines, and using them to deliver working software in
unfamiliar domains quickly and verifiably.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/pacp-control-plane-dark.svg">
  <img alt="PACP flow: owner intent becomes a Goal Ladder; an agent session works the running goal; a convergence gate counts only accepted items and returns COMPLETE, CONTINUE, REALIGN, or CIRCUIT_BREAK; a Task Footer records one validated state, is enforced by Claude Code hooks, and rebuilds a fresh session when context runs out." src="assets/pacp-control-plane-light.svg">
</picture>

## Projects

| Project | What it proves | Try it |
| --- | --- | --- |
| [Canopus](https://github.com/Hsiang-Tang/canopus) | The method: frozen acceptance envelopes, convergence gates, circuit breakers, and a Claude Code Stop-hook latch that keep long-running agents on goal. Standard-library Python. | [Dashboard](https://hsiang-tang.github.io/canopus/assets/dashboard-sample.html) · [Adopt in 15 minutes](https://github.com/Hsiang-Tang/canopus/blob/main/playbooks/adopting-canopus.md) |
| [keyflip](https://github.com/Hsiang-Tang/keyflip) | Systems work in Rust: a Zhuyin (Bopomofo) input method that tells Chinese from English by itself. Core engine, C FFI, and a macOS input-method shell, in daily use. | [Film (34 s)](https://github.com/Hsiang-Tang/keyflip/releases/download/v0.1.1/keyflip-demo.mp4) · [Releases](https://github.com/Hsiang-Tang/keyflip/releases) |
| [tradclip](https://github.com/Hsiang-Tang/tradclip) | Data-driven text conversion: Simplified Chinese on the macOS clipboard becomes Traditional with Taiwan character forms as you copy. Rust core, Swift menu bar app, accuracy measured on held-out data. | [Film (17 s)](https://github.com/Hsiang-Tang/tradclip/releases/download/v0.1.0/tradclip-demo.mp4) · [Releases](https://github.com/Hsiang-Tang/tradclip/releases) |
| [network-switch-anatomy](https://github.com/Hsiang-Tang/network-switch-anatomy) | Interactive UI and networking domain knowledge: an 8-port switch drawn as a crafted machine, with a learning-bridge model, explode views, and pin-out sheets. | [Live demo](https://hsiang-tang.github.io/network-switch-anatomy/) |
| Alphalia | A shipped iOS product: a local-first investment tracker, released and iterated through App Review. | [App Store](https://apps.apple.com/tw/app/alphalia/id6804235042) |

## How I work

- Specification and acceptance criteria come first; each task is frozen
  before implementation starts.
- AI agents implement against that envelope; out-of-scope findings are
  deferred instead of growing the task.
- Every claim in a README maps to a test or a documented check, and the
  checks are run and verified locally before a change is pushed.
