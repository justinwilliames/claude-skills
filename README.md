> **⚠️ Moved (2026-07-03):** all skills now maintained in [justinwilliames/skills](https://github.com/justinwilliames/skills) — this repo is archived.

# claude-skills

Battle-tested Claude Code skills: multi-model delegation/orchestration, spec hardening, autonomous work loops, OpenAI Codex bridges, and personal-ops utilities (weekly self-review, calendar hygiene). Sanitized from daily production use.

---

## Skills

| Skill | One-line contract |
|---|---|
| [`intelligent-delegation`](intelligent-delegation/) | Orchestrates complex builds by decomposing tasks, fanning work to Sonnet sub-sessions and Codex in parallel, and presenting a unified diff — without bloating the main session's context. |
| [`claude-build-hardening`](claude-build-hardening/) | Runs structured multi-round adversarial review on a spec/PRD/RFC across Engineering, UX, Security, and Accessibility lenses (36 reviewer runs, model-diverse) before handing to engineers or Claude Code. |
| [`infinite-working-skill`](infinite-working-skill/) | Drives any long-running decomposable task to completion unattended — surviving usage limits, crashes, and closed sessions via a durable resumer and an idempotency ledger. |
| [`codex`](codex/) | Delegates single-focus coding tasks, reviews, and deliberations to OpenAI Codex (GPT-5.5) as a genuine second brain — `think` for analysis, `run` for implementation. |
| [`codex-imagegen`](codex-imagegen/) | Delegates raster image generation and editing to Codex CLI, handling attachment flow, prompt skeletons, and output capture. |
| [`computer-control`](computer-control/) | Routes any screen-driving task to the right engine — Claude in Chrome for web automation, the Codex bridge for native macOS app control, osascript for scriptable tasks. |
| [`self-performance-review`](self-performance-review/) | Weekly evidence-based self-review — pulls your comms/calendar/session data, benchmarks against management canon (Grove, Drucker, Bezos), grades last week's targets. |
| [`calendar-review`](calendar-review/) | Calendar hygiene audit — protects focus blocks, finds slots, flags conflicts with concrete fallbacks. |

---

## Install

```bash
git clone https://github.com/justinwilliames/claude-skills
```

Then copy any skill into your Claude Code skills directory:

```bash
cp -R claude-skills/<skill-name> ~/.claude/skills/<skill-name>
```

Restart Claude Code (or reload skills) — it will pick up the new skill automatically.

Individual skills may have their own prerequisites (e.g. `jq` for `intelligent-delegation`, the Codex CLI for the `codex*` and `computer-control` skills). See each skill's `README.md`.

---

## See also

[github.com/justinwilliames/skills](https://github.com/justinwilliames/skills) — universal operating doctrine and craft (voice, delegation instincts, context discipline, build hardening). This repo is the heavier machinery those principles run on.

---

## License

MIT — see [LICENSE](LICENSE).
