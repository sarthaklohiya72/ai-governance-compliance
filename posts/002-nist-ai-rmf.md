# 2. NIST AI Risk Management Framework (AI RMF 1.0)

*Posted 18 September 2026*

Where the EU AI Act is a binding law with fines attached, the NIST AI Risk
Management Framework is the opposite kind of document: **voluntary, U.S.-based,
and written to be usable by any organization regardless of sector or size.**
Released January 26, 2023, it's become the de facto reference point that
other frameworks and even regulators point to when they want to describe
"reasonable" AI risk management practice.

## The core idea: four functions, not a checklist

AI RMF 1.0 isn't a list of controls to tick off — it's organized around four
functions that are meant to operate continuously and feed into each other:

1. **Govern** — the foundation. Policies, roles, accountability structures,
   and culture around AI risk. This is the only function that applies
   organization-wide rather than to a single AI system.

2. **Map** — establishing context for a specific AI system: what it does,
   who it affects, what could go wrong, and what risks are even relevant
   before you try to measure anything.

3. **Measure** — applying quantitative and qualitative methods to analyze
   and track the risks identified in Map (bias testing, robustness
   evaluation, performance monitoring, etc.).

4. **Manage** — actually treating the risks: prioritizing them, deciding
   what to mitigate versus accept, and building incident response processes
   for when something goes wrong.

Across the four functions there are roughly 72 subcategories of specific
outcomes — but the framework deliberately avoids prescribing *how* to
achieve them, leaving implementation to the organization.

## The Generative AI Profile (NIST AI 600-1)

In July 2024, NIST published a companion document — the Generative AI
Profile — that maps 12 risk categories specific to or amplified by generative
AI back onto the four RMF functions. These include things like confabulation
(what most people call hallucination), prompt injection, data privacy
leakage, harmful content generation, cybersecurity vulnerabilities, and
intellectual property risks. If you're deploying LLMs specifically, this
profile is the more directly useful document day-to-day.

## What's changed going into 2026

NIST hasn't published a formal "AI RMF 2.0," but the framework has been
evolving through addenda and sector profiles rather than a single rewrite:

- **Political-content revisions.** The White House AI Action Plan (July 23,
  2025) directed NIST to revise the AI RMF to remove references to
  misinformation, diversity/equity/inclusion, and climate change — a
  notable shift in scope driven by policy rather than technical findings.
- **Sector-specific profiles are the growth area.** In April 2026, NIST
  released a concept note for an AI RMF Profile on Trustworthy AI in
  Critical Infrastructure, aimed at operators layering AI into industrial
  and infrastructure systems.
- **More profiles and granular evaluation guidance are expected through
  2026**, extending the base framework into specific domains rather than
  replacing it.

## What this means in practice

- **It's a common vocabulary, not a compliance gate.** Unlike the EU AI Act,
  nothing requires you to adopt AI RMF — but auditors, customers, and
  insurers increasingly use its Govern/Map/Measure/Manage language as a
  reference point, so fluency in it has practical value even outside the US.
- **Start with Govern.** Organizations that skip straight to technical risk
  measurement without an accountability structure in place tend to produce
  assessments nobody acts on.
- **If you're working with LLMs, read the Generative AI Profile
  specifically** — the base RMF is too general to catch issues like prompt
  injection or confabulation on its own.

## Sources

- [AI Risk Management Framework — NIST](https://www.nist.gov/itl/ai-risk-management-framework)
- [Artificial Intelligence Risk Management Framework (AI RMF 1.0) — NIST](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-ai-rmf-10)
- [NIST AI RMF 2025–2026 Updates: What You Need to Know — IS Partners](https://www.ispartnersllc.com/blog/nist-ai-rmf-2025-2026-updates-what-you-need-to-know-about-the-latest-framework-changes/)
- [NIST AI RMF: Govern, Map, Measure, Manage Explained — Balanced Security](https://blog.balancedsec.com/p/original-inside-the-nist-ai-risk)

---

*This is a personal learning summary, not legal advice. Verify current
requirements against the official NIST sources above before making
compliance decisions.*
