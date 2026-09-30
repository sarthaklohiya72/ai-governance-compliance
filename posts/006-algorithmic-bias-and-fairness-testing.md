# 6. Algorithmic Bias & Fairness Testing

*Posted 30 September 2026*

Every framework so far — the EU AI Act, NIST's AI RMF, ISO/IEC 42001, GDPR
Article 22, the OECD Principles — requires you to manage harmful bias. None of
them tells you which number to compute. That gap is where most AI governance
programmes actually get stuck, because "is this model fair?" turns out to have
several mutually incompatible right answers.

## The three metrics you will actually be asked about

**Demographic parity** (also called statistical parity or independence).
The model selects people from each group at the same rate, regardless of the
underlying base rate. Simple to explain to a non-technical stakeholder, and
the closest match to how anti-discrimination law tends to think.

**Equalized odds.** True positive rates *and* false positive rates are equal
across groups. Unlike demographic parity, this rewards being accurate and
penalises a model that only works well on the majority group. Usually the
better metric when the outcome being predicted is real and measurable
(loan default, disease presence).

**Calibration.** A predicted score of 0.7 means the same thing for every
group. Risk-scoring teams tend to default to this one without realising it is
a fairness choice.

## The impossibility result — and why it matters commercially

Chouldechova's 2017 result proves these cannot all hold at once when base
rates genuinely differ between groups. You can have calibration, or equal
false positive and false negative rates, but not both. This is a mathematical
fact, not an engineering shortfall.

The practical consequence: **there is no defensible way to pick a fairness
metric without a documented, human judgement about which kind of error hurts
whom.** A false positive in fraud screening (a legitimate customer blocked)
and a false negative in cancer screening (a missed diagnosis) are not the
same kind of harm, and the metric should follow the harm. Regulators and
auditors are increasingly less interested in *which* metric you chose than in
whether you can show who chose it, on what reasoning, and when.

## The four-fifths rule

The oldest and most widely referenced threshold comes from US employment law:
the EEOC's **four-fifths (80%) rule**. If a protected group's selection rate
falls below 80% of the most-favoured group's rate, that counts as evidence of
adverse impact. It is a rough heuristic — it has no statistical significance
built in and behaves badly on small samples — but it remains the default
benchmark in hiring-adjacent AI audits, and it is where most bias-audit
disclosure regimes anchor their reporting.

## Where in the pipeline to intervene

- **Pre-processing** — reweight or resample the training data. Easiest to
  implement, model-agnostic, but you are changing the data rather than the
  decision rule, and the fix can wash out downstream.
- **In-processing** — bake the fairness constraint into the optimiser
  (adversarial debiasing, constrained ERM). Hardest to build, generally the
  best accuracy/fairness trade-off.
- **Post-processing** — adjust thresholds per group after the fact. Very
  effective and easy to audit, but explicitly group-conscious, which can
  itself be legally fraught in some jurisdictions.

Recent cross-domain evaluations find post-processing constraints sometimes
*harm* the groups they are meant to help, so the intervention needs its own
evaluation — you cannot assume applying a fairness correction made things
better.

## Practical pitfalls

**Intersectionality.** A model can pass every single-axis test (gender, race,
age separately) and fail badly for a specific intersection. Single-axis
testing is necessary but nowhere near sufficient.

**You need the protected attribute to test for bias on it.** This is the
central operational tension — GDPR and equivalent laws restrict collecting
special-category data, but you cannot measure disparate impact on data you do
not hold. Common workarounds are proxy inference (Bayesian Improved Surname
Geocoding and similar), a consented sub-sample used only for fairness
measurement, or a trusted third-party audit arrangement. All three need their
own privacy justification documented.

**Bias is not only in the model.** Historical label bias (the training
outcome itself encodes past discrimination), sampling bias, and deployment
bias — where a fair model is used differently on different populations — all
sit outside the model weights and outside most automated tooling.

**Drift.** Fairness properties decay. A model tested at launch and never
retested is, for most audit purposes, untested.

## Tooling

**Fairlearn** (Microsoft) is the practical default for group fairness metrics
and mitigation, with scikit-learn integration. **Aequitas** (University of
Chicago) offers a bias-audit toolkit with a web interface aimed at
non-engineers. Both are open source. Neither picks your metric for you — that
is still a governance decision, not a library call.

## What to do first

Write down, before you compute anything: who the affected groups are, which
error type harms them most, which metric therefore applies, what threshold
counts as a problem, who signs off, and how often you will retest. That
document is the deliverable auditors actually want. The numbers are the easy
part.

## Sources

- [Common fairness metrics — Fairlearn documentation](https://fairlearn.org/main/user_guide/assessment/common_fairness_metrics.html)
- [The Impossibility Theorem of Machine Fairness: A Causal Perspective (arXiv)](https://arxiv.org/pdf/2007.06024)
- [When Post-Processing Fairness Constraints Help and When They Harm: Evidence from Eight Cross-Domain Evaluations (arXiv)](https://arxiv.org/pdf/2609.26955)
- [AI Bias Audit Requirements: Compliance & Testing Guide (2026) — Secure Privacy](https://secureprivacy.ai/blog/ai-bias-audit-requirements)

---

*This is a personal learning summary, not legal advice. Verify current
requirements against primary sources or qualified counsel before making
compliance decisions.*
