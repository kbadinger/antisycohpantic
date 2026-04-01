# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repo maintains portable anti-sycophancy rules for AI assistants. The primary artifact is `prompt.md` — a self-contained prompt block that can be pasted into any LLM's system prompt or custom instructions.

## Structure

- `prompt.md` — **The product.** 20 rules + high-stakes advice framework. Keep this compact (under ~150 lines) so it fits in system prompts.
- `taxonomy.md` — Reference doc explaining 9 sycophancy failure modes. Supports `prompt.md` but is not meant to be pasted into prompts.
- `advice-safety.md` — Deep reference on personal advice guardrails. Same role as taxonomy.
- `README.md` — How to use the repo. Primary instruction: "copy prompt.md."

## Editing guidelines

- `prompt.md` rules are numbered 1-20. When adding rules, append to the appropriate section and increment.
- Keep `prompt.md` LLM-agnostic. No references to specific users, specific tools, or specific model providers.
- `taxonomy.md` and `advice-safety.md` can be as detailed as needed — they're reference docs, not prompt constraints.
