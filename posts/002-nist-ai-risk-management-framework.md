# 2. NIST AI Risk Management Framework (AI RMF 1.0)

*Posted 29 September 2026*

If the EU AI Act tells you **what you must do**, the NIST AI RMF tells you
**how to organise yourself to do it**. It is a voluntary framework — nobody
fines you for ignoring it — but it has quietly become the default operating
model for AI governance programmes, especially in the US and among vendors
selling into regulated buyers.

Published as **NIST AI 100-1 on 26 January 2023**, it is still the current
version. NIST has confirmed the framework is being revised as part of the
White House AI Action Plan, but no 2.0 exists yet.

## The four functions

The framework's core is four functions, meant to run continuously and in
parallel rather than as a linear checklist:

1. **GOVERN** — the cross-cutting one. Policies, roles, accountability lines,
   risk tolerance, training, and escalation paths. GOVERN is the only
   function that applies across the whole lifecycle all the time, and it is
   the one organisations most often skip. If nobody owns AI risk on paper,
   the other three functions produce documents nobody acts on.

2. **MAP** — establish context before you build. What is the system for, who
   is affected, what are the legal and ethical constraints, what could go
   wrong for third parties. This is where you decide whether the AI system
   is even the right solution.

3. **MEASURE** — quantify what you mapped. Metrics, test methods, evaluation
   of the trustworthiness characteristics, tracking of model performance and
   drift over time. Where you cannot measure something quantitatively, the
   framework expects you to say so explicitly rather than stay silent.

4. **MANAGE** — act on what you measured. Prioritise risks against your
   stated tolerance, allocate resources, respond to incidents, and decide
   when to decommission a system.

## The seven trustworthiness characteristics

MEASURE is anchored to a specific list, which is worth memorising because it
crosswalks cleanly onto most other frameworks: **valid and reliable; safe;
secure and resilient; accountable and transparent; explainable and
interpretable; privacy-enhanced;** and **fair, with harmful bias managed**.

NIST is explicit that these trade off against each other — optimising for
explainability can cost accuracy, optimising for privacy can cost fairness
testing. The framework asks you to make those trade-offs deliberately and
record the reasoning, not to maximise all seven.

## Companion resources that do the real work

The 48-page core document is deliberately abstract. The useful material is
in the companions:

- **AI RMF Playbook** — suggested actions, references and documentation
  prompts for each subcategory. This is what you actually implement against.
- **NIST AI 600-1, the Generative AI Profile** (released 26 July 2024) — maps
  generative-AI-specific risks such as confabulation, harmful bias, data
  privacy leakage, information integrity and CBRN misuse onto the same four
  functions. If your AI work is LLM-based, start here rather than with the
  core document.
- **Crosswalks** — official mappings from AI RMF to ISO/IEC 42001, the EU AI
  Act and OECD principles. Useful for avoiding duplicate control sets.
- **Critical Infrastructure Profile** — NIST released a concept note on
  **7 April 2026** for a profile aimed at critical infrastructure operators
  adopting AI-enabled capabilities. Still early, but worth tracking if you
  operate in that space.

## What this means in practice

- **Voluntary does not mean optional.** AI RMF alignment is increasingly a
  procurement question, and it is the framework US federal buyers and their
  supply chains reach for. "We follow NIST AI RMF" is a sentence that
  shortens vendor security reviews.
- **Start with GOVERN, not with tooling.** Named owners, a written risk
  tolerance and an inventory of AI systems in use will get you further in
  three months than any evaluation platform.
- **Use it as the scaffolding, use other frameworks as the content.** AI RMF
  deliberately does not tell you *what* threshold of bias is acceptable.
  Pair it with ISO/IEC 42001 for certifiable management-system structure and
  with the relevant regulation (EU AI Act, sectoral rules) for hard
  requirements.
- **Don't wait for 2.0.** A revision is in progress with no published date.
  The four functions are stable enough to build on now.

## Sources

- [AI Risk Management Framework — NIST](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST AI 100-1: Artificial Intelligence Risk Management Framework (AI RMF 1.0) — full PDF](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)
- [NIST AI 600-1: Generative Artificial Intelligence Profile](https://doi.org/10.6028/NIST.AI.600-1)
- [NIST AI RMF Playbook — Trustworthy & Responsible AI Resource Center](https://airc.nist.gov/airmf-resources/playbook/)
- [Concept Note: AI RMF Profile on Trustworthy AI in Critical Infrastructure (April 2026)](https://www.nist.gov/programs-projects/concept-note-ai-rmf-profile-trustworthy-ai-critical-infrastructure)

---

*This is a personal learning summary, not legal advice. Verify current
requirements against the official NIST sources above before making
compliance decisions.*
