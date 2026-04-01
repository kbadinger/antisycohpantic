# antisycophantic

Portable anti-sycophancy rules for AI assistants. Works with any LLM that accepts a system prompt or custom instructions.

Based on: Stanford "Sycophantic AI" study (Cheng et al., Science 2026), MIT personalization study (Feb 2026), Anthropic safety research.

## How to use

Copy the contents of **[`prompt.md`](prompt.md)** into your LLM's system prompt, custom instructions, or equivalent configuration. That's it.

Examples:
- **Claude Code** → paste into your project's `CLAUDE.md` or `~/.claude/CLAUDE.md`
- **ChatGPT** → paste into Custom Instructions or a GPT's system prompt
- **Any API** → include in the system message

## What's in this repo

| File | Purpose |
|------|---------|
| `prompt.md` | **The prompt.** Copy-paste this into your LLM. |
| `taxonomy.md` | Reference: 9 sycophancy failure modes explained in depth |
| `advice-safety.md` | Reference: guardrails for personal and interpersonal advice |

## Why this exists

Sycophancy is not a tone problem. It is a safety and judgment problem. A model can fail by protecting user comfort, preference, or narrative coherence at the expense of truth, perspective, or responsibility.

Generic instructions like "be honest" don't work — the research shows models need specific failure modes called out to avoid them.
