# Maintenance and Review Record

## Status

- **Lifecycle:** Active / maintained
- **Review cadence:** Quarterly, and after a major frontier-model generation, provider behavior-policy change, or observed real-world failure
- **Last substantive review:** 2026-08-01
- **Next scheduled review:** 2026-11-01

`prompt.md` is referenced by global AI instructions. Treat changes as production-control changes: small, evidence-backed, and reversible. A scheduled review does not require a prompt edit when the existing behavior remains sound.

## Recurring review checklist

1. Read new primary research and current provider behavior guidance; distinguish replicated findings from early or provider-specific results.
2. Review real failures since the last checkpoint. Classify the observable behavior, model, context length, memory/personalization state, stakes, and whether user pushback occurred.
3. Test representative frontier models on a compact regression set covering:
   - false-premise agreement and factual pushback
   - critique and proportional praise
   - one-sided interpersonal advice and absent perspectives
   - user pressure to reverse a sound answer
   - long-context or personalized-memory drift
   - manipulative message drafting
   - abuse/coercion cases where confrontation or apology could be unsafe
   - low-stakes questions where forced counterpoints would be noise
4. Score truthfulness, calibrated uncertainty, independence under pressure, proportional praise, warmth, usefulness, and safety. Check for anti-sycophancy overcorrection: reflexive disagreement, coldness, excessive caveats, invented counterarguments, or stubbornness.
5. Make the smallest change that addresses a reproduced failure. Keep rules provider-agnostic and avoid duplicating safeguards already reliably supplied by host systems.
6. Re-run the regression set, inspect the diff, confirm `prompt.md` remains compact, and add a dated checkpoint below.

## Evidence reviewed on 2026-08-01

- Myra Cheng et al., ["Sycophantic AI decreases prosocial intentions and promotes dependence"](https://doi.org/10.1126/science.aec8352), *Science* 391 (2026). Supports heightened scrutiny for interpersonal advice, repair behavior, and dependence risks.
- Shomik Jain et al., ["Interaction Context Often Increases Sycophancy in LLMs"](https://doi.org/10.1145/3772318.3791915), CHI 2026. Supports testing memory, personalization, and long interaction context rather than relying on single-turn cases.
- Myra Cheng et al., ["Verbalizing LLMs' assumptions to explain and control sycophancy"](https://arxiv.org/abs/2604.03058) (2026 preprint). Supports exposing material assumptions instead of laundering them through confident framing.
- Meryl Ye et al., ["What Counts as AI Sycophancy?"](https://arxiv.org/abs/2605.21778) (2026 preprint). Supports describing concrete behaviors and testing subtle framing or omission rather than treating sycophancy as one settled construct.
- Anthropic, ["How people ask Claude for personal guidance"](https://www.anthropic.com/research/claude-personal-guidance) (2026). Supports stress-testing one-sided relationship advice and answer reversals under user pushback.
- OpenAI, [Model Spec: "Don't be sycophantic"](https://model-spec.openai.com/2025-10-27.html#dont-be-sycophantic) and [GPT-4o sycophancy postmortem](https://openai.com/index/sycophancy-in-gpt-4o/) (2025). Supports stable factual positions, proportional praise, explicit steering, and behavioral evaluations.

## Checkpoint: 2026-08-01

The core control remained sound. This review made a narrow corrective update:

- replaced unconditional counterpoint and risk requirements with stakes-calibrated scrutiny to avoid manufactured contrarianism and ritual caveats
- changed the pushback rule from "change only with new information" to re-evaluate-and-explain, preserving correction without encouraging stubbornness
- made assumptions, inferences, and unknowns explicit and prohibited invented absent-stakeholder motives
- made the high-stakes framework an internal reasoning check whose material findings should be surfaced, not a mandatory visible template
- added an explicit safety exception so abuse, coercion, stalking, self-harm, or credible danger do not trigger unsafe advice to confront, mediate, or apologize
- documented anti-sycophancy overcorrection and a repeatable regression-review protocol

No provider-specific commands or user-specific content were added to the portable prompt.
