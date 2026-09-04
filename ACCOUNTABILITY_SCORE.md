# Accountability Score Methodology v0.1

The UNSOLVED Accountability Score is a transparent performance index derived from independently tracked cases.

## Weighting

- **30% Verified Resolution Speed** — elapsed time from challenge creation to independent verification, normalized by issue type and severity.
- **25% Verified Closure Rate** — share of eligible challenges that reach `VERIFIED_RESOLVED`.
- **20% Disputed Closure Rate** — frequency with which official closure claims are contradicted by physical verification. This component is reverse-scored: fewer disputed closures improve the score.
- **15% Aging Unresolved Cases** — volume and duration of stagnant unresolved cases, normalized by category and severity. Lower aging burden improves the score.
- **10% Responsiveness & Transparency** — acknowledgment latency, substantive response latency, ownership clarity, and quality of public engagement.

The weighted components produce a score from 0–100.

## Non-negotiable publication rules

Every published score MUST include:

- sample size;
- observation window;
- confidence level;
- applicable issue categories;
- methodology version;
- whether the score represents only UNSOLVED-tracked cases or a broader population dataset.

A score based on 12 tracked cases must never be presented as statistically equivalent to a score based on 12,000.

## Confidence bands

Initial implementation should expose a simple confidence label rather than false precision.

Suggested starting bands:

- **INSUFFICIENT** — fewer than 10 eligible verified observations;
- **LOW** — 10–29 observations;
- **MODERATE** — 30–99 observations;
- **HIGH** — 100+ observations with adequate category coverage.

These thresholds are provisional and must be validated empirically before being treated as stable.

## Selection-bias warning

UNSOLVED challenges may overrepresent difficult, visible, or long-running problems because citizens are more likely to submit them.

Until full-population administrative data is ingested and sampling bias is modeled, institutional profiles MUST use language such as:

> Among independently tracked UNSOLVED cases…

They MUST NOT imply that challenge cases alone represent all institutional work.

## Normalization

Resolution time MUST be normalized by issue category and severity. A streetlight outage cannot be scored against the same expected duration as a bridge rehabilitation project.

Normalization may eventually use:

- peer-jurisdiction baselines;
- historical category medians;
- severity classes;
- regulatory or service-level targets;
- geographic and operational context.

All normalization methods used in public scoring must be documented and versioned.

## Auditability

Score changes must be reproducible from:

1. the versioned formula;
2. the eligible case set;
3. each case's state-transition history;
4. normalization inputs;
5. confidence rules.

Commercial relationships MUST NOT alter public scoring methodology or suppress unfavorable eligible cases.
