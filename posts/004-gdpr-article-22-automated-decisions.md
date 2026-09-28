# 4. GDPR & AI: Automated Decision-Making (Article 22)

*Posted 28 September 2026*

Long before the EU AI Act existed, the GDPR already regulated AI — just not by
name. Article 22 governs **decisions made about people by machines**, and
because it's been enforceable since 2018 with real case law behind it, it is
often the more immediate legal risk for a company deploying a scoring or
screening model in Europe.

## The three-part test

Article 22 only bites when all three conditions are met:

1. **There is a decision** — including profiling.
2. **It is based *solely* on automated processing** — no meaningful human
   involvement.
3. **It produces legal effects or similarly significantly affects** the
   person — loan refusals, job rejections, insurance pricing, benefits
   decisions.

If all three apply, the decision is **prohibited by default**, unless it rests
on one of three narrow bases: explicit consent, necessity for entering or
performing a contract, or authorisation by Member State/EU law. Even then you
owe the Article 22(3) safeguards: the right to human intervention, the right
to express a view, and the right to contest the decision.

## "Solely automated" is narrower than teams assume

The most common compliance error is assuming a human in the loop switches
Article 22 off. It doesn't. Per EDPB guidance, human involvement only counts
as meaningful if the reviewer has **actual authority to override** the output,
**access to the underlying data**, **understanding of the logic** behind the
recommendation, and the ability to factor in information the model never saw.
A caseworker clicking "approve" on 200 model outputs an hour is
rubber-stamping — legally the decision is still solely automated.

## Two CJEU rulings that changed the practical picture

**SCHUFA (C-634/21, December 2023).** A German credit agency produced a score;
the bank refused the loan on the strength of it. The Court held that
*generating the score itself* was an automated decision under Article 22 where
the downstream party draws "strongly" on it. The consequence is significant:
liability attaches to the **scoring provider**, not just the organisation that
acts on the score. If you sell risk scores, screening outputs, or
recommendations that customers rely on heavily, you may be the Article 22
decision-maker.

**Dun & Bradstreet Austria (C-203/22, February 2025).** The Court clarified
the "right to explanation" under Article 15(1)(h). Two things you cannot do:
hand over the algorithm or a mathematical formula, or dump an exhaustive
step-by-step description. The explanation must be concise and intelligible
enough that the person can actually exercise their Article 22(3) rights.
Trade secrecy is **not** a blanket shield — where there's a genuine conflict,
the disputed information goes to the supervisory authority or court to
balance, not into a black box.

## How this interacts with the EU AI Act

They stack; they don't substitute. The AI Act regulates the system and its
provider; Article 22 gives the affected individual directly enforceable
rights. Article 86 of the AI Act mirrors the explanation duty for high-risk
systems. In practice one screening model can trigger a DPIA and Article 22
safeguards under GDPR *and* high-risk obligations under the AI Act — with
GDPR enforceable today and, per the Digital Omnibus delay, the high-risk
tier not applying until December 2027.

One caveat worth tracking: the Commission's proposed GDPR reform (still in
the legislative process as of late 2026) would widen some Article 22
exceptions, particularly for public-sector processing of non-sensitive data.
The core prohibition is expected to survive.

## What this means in practice

- **Audit your "human review" honestly.** Ask whether reviewers ever
  actually overturn the model. If the override rate is near zero, you're
  probably in Article 22 territory regardless of your process diagram.
- **Write the explanation before you ship.** If you can't describe in plain
  language which factors drove an individual outcome, you cannot satisfy
  Article 15(1)(h) — and "our vendor won't tell us" is not a defence.
- **Check whether you're the scorer.** Post-SCHUFA, upstream providers of
  scores and recommendations can be on the hook even without a customer
  relationship with the affected person.
- **Run a DPIA.** Systematic automated decisions with significant effects
  effectively always require one under Article 35.

## Sources

- [Article 22 GDPR — full text](https://gdpr-text.com/read/article-22/)
- [Rights related to automated decision-making including profiling — ICO](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/individual-rights/rights-related-to-automated-decision-making-including-profiling/)
- [SCHUFA: CJEU rules on the scope of Article 22 — TLT](https://www.tlt.com/insights-and-events/insight/schufa-case-cjeu-rules-on-scope-of-article-22)
- [CJEU decision on algorithmic transparency and trade secrets (C-203/22) — Bird & Bird](https://www.twobirds.com/en/insights/2025/cjeu-decision-on-algorithmic-transparency-and-secret-protection-(cjeu-c-20322))
- [Key takeaways from the CJEU's automated decision-making rulings — IAPP](https://iapp.org/news/a/key-takeaways-from-the-cjeus-recent-automated-decision-making-rulings)

---

*This is a personal learning summary, not legal advice. Verify current
requirements against the official sources above before making compliance
decisions.*
