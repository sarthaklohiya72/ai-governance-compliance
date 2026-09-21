# 2. NIST AI Risk Management Framework (AI RMF 1.0)

*Posted 21 September 2026*

Where the EU AI Act is a binding law with risk tiers and deadlines, the
**NIST AI Risk Management Framework (AI RMF 1.0)** is something different:
a voluntary, US-originated framework for *how* to think about and manage
AI risk. It's not a checklist of banned uses — it's a set of functions any
organization can layer onto its own AI development or procurement process.

Released January 26, 2023 by the National Institute of Standards and
Technology, it has become a de facto reference point even outside the US,
partly because it's flexible enough to sit underneath other regimes (a
company can use AI RMF to organize its internal controls and still need the
EU AI Act's conformity assessment on top).

## The four core functions

AI RMF organizes risk management into four functions, meant to be applied
iteratively across an AI system's lifecycle rather than as one-time steps:

1. **Govern** — Build the organizational culture and structure for AI risk
   management: policies, accountability, roles, and leadership buy-in. This
   function underpins the other three and applies throughout, not just at
   the start.

2. **Map** — Understand the context an AI system operates in: its intended
   use, who it affects, and what could go wrong technically, socially, or
   ethically. This is where you identify risks before they materialize.

3. **Measure** — Assess and track those risks with quantitative and
   qualitative methods — testing for bias, robustness, accuracy, and other
   trustworthiness characteristics.

4. **Manage** — Prioritize and act on measured risks: allocate resources,
   respond to incidents, and monitor for drift as systems and their
   environments change.

## The Generative AI Profile (NIST AI 600-1)

In July 2024, NIST published a companion document — the **Generative AI
Profile** — that applies the same four functions specifically to generative
AI. It identifies 12 GenAI-specific risk categories (things like
confabulation/hallucination, data privacy leakage, and CBRN information
risks) and maps concrete actions to each of the Govern/Map/Measure/Manage
functions. If you're deploying an LLM-based product, this profile is the
more directly useful document to work from.

## What's changing in 2026

NIST doesn't treat AI RMF as finished. Two developments worth tracking:

- The framework itself is being revised as part of the White House AI
  Action Plan, so expect updates to the core document.
- NIST is building sector- and use-case-specific **profiles** on top of the
  base framework — a concept note for a "Trustworthy AI Profile for
  Critical Infrastructure" came out in April 2026, and an AI Agent
  Interoperability Profile is expected in Q4 2026. The pattern: the core
  four functions stay stable, and profiles adapt them to specific
  industries or system types.

## What this means in practice

- **Use it as scaffolding, not a compliance target.** AI RMF has no
  certification and no penalties — its value is giving your team a shared
  vocabulary and structure for AI risk conversations.
- **Start with Govern.** Skipping straight to technical risk measurement
  without governance structure and accountability tends to produce
  measurement theater rather than actual risk reduction.
- **If you're building on generative AI, read the GenAI Profile directly**
  rather than just the base framework — it's where the concrete, actionable
  risk categories live.
- **Watch for a profile matching your sector.** If NIST publishes one for
  your industry (critical infrastructure, agents, etc.), it will likely be
  more directly applicable than the general framework alone.

## Sources

- [AI Risk Management Framework — NIST](https://www.nist.gov/itl/ai-risk-management-framework)
- [AI RMF Core Functions — NIST AIRC](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/)
- [NIST AI RMF 2025–2026 Updates: What You Need to Know](https://www.ispartnersllc.com/blog/nist-ai-rmf-2025-2026-updates-what-you-need-to-know-about-the-latest-framework-changes/)
- [NIST AI Risk Management Framework: Agentic Profile — Cloud Security Alliance](https://labs.cloudsecurityalliance.org/agentic/agentic-nist-ai-rmf-profile-v1/)

---

*This is a personal learning summary, not legal advice. Verify current
requirements against the official NIST sources above before making
compliance decisions.*
