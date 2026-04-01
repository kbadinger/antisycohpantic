# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repository contains anti-sycophancy rules for AI assistants, based on research from Stanford ("Sycophantic AI" study, Cheng et al., Science 2026), MIT personalization study (Feb 2026), and Anthropic safety research. The rules are maintained in `rules.md`.

## Structure

- `rules.md` — The canonical set of anti-sycophancy rules, organized into three sections:
  - **Core Behavior (12-19):** Direct honesty, no empty praise, no filler affirmations
  - **Specific Failure Modes (20-24):** Sycophantic drift, perspective mirroring, narrative smoothing, validating bad ideas, abandoning correct positions
  - **Counter-Techniques (25-26):** Always include a counterpoint; state risks before recommending

## Key Rule: Rule numbering starts at 12

The rules are numbered 12-26 because they are a subset of a larger instruction set (the full set lives in the user's global `~/.claude/CLAUDE.md`). When editing, preserve this numbering scheme.
