# UNSOLVED Protocol

> **Public accountability, verified.**

UNSOLVED is an open public-accountability protocol for tracking whether reported institutional problems are actually resolved in the physical world.

The protocol is built around a simple distinction:

**Officially closed does not necessarily mean actually fixed.**

UNSOLVED creates a public, auditable record that connects a reported problem to the responsible institution, official administrative status, independent evidence, and a final verified resolution state.

## Core hypothesis

Can a transparent protocol systematically capture and prove the gap between **administrative closure** and **physical reality**?

Phase 1 exists to test that question with 10–25 tightly scoped infrastructure challenges whose outcomes can be verified objectively.

## Minimum Viable Protocol

1. **Challenge Page** — a public record of one problem, one location, one responsible authority, an escalation target, and a clock.
2. **Evidence Locker** — provenance-preserving evidence for reports, case numbers, timestamps, media, and verification events.
3. **Resolution Oracle** — compares official administrative disposition against independently verified physical conditions.
4. **Institutional Profile** — aggregates public cases into transparent performance metrics and accountability scores.

## Resolution lifecycle

```text
REPORTED → OPEN → CLAIMED_RESOLVED → VERIFIED_RESOLVED
                              ↘ DISPUTED
                              ↘ UNVERIFIABLE
```

Responsibility is tracked separately from resolution so a challenge can remain OPEN while institutional ownership is ACCEPTED, DISPUTED, or UNASSIGNED.

## Accountability Score

The public score methodology is designed to be inspectable rather than mysterious:

- 30% Verified Resolution Speed
- 25% Verified Closure Rate
- 20% Disputed Closure Rate
- 15% Aging Unresolved Cases
- 10% Responsiveness & Transparency

Scores are normalized by issue type and severity and must always be published with sample-size and confidence information.

See `ACCOUNTABILITY_SCORE.md` for the full methodology.

## Transparency principles

- Public scoring rules are versioned in Git.
- Resolution criteria are defined before a challenge launches.
- Evidence conclusions must be reproducible by an independent reviewer.
- Official claims and observed reality are stored as separate facts.
- Score changes must be explainable from published methodology and underlying case history.
- Public data must not expose sensitive raw evidence unnecessarily.

## What is intentionally *not* open here

UNSOLVED separates public trust infrastructure from commercial and security-sensitive implementation.

This repository does **not** publish private authentication systems, billing, customer data, abuse defenses, anti-gaming heuristics, private moderation tooling, infrastructure secrets, or sensitive raw evidence.

Transparency does not require publishing a manual for defeating the verification system.

## Phase 1 pilot

The first pilot will use pledge-backed challenges with capped targets and no platform fee. No funds need to be held by UNSOLVED during this phase.

Initial challenges should focus on objectively verifiable infrastructure conditions such as streetlight outages, where official closure status can be compared with subsequent physical observation.

### Phase 1 success criteria

- ≥80% correct authority assignment
- ≥80% independently reverifiable after official disposition
- At least one meaningful official/physical discrepancy captured correctly
- ≥90% inter-reviewer agreement on final resolution state
- Evidence review measured in minutes, not hours
- Conclusions understandable without insider explanation
- No pilot case requires subjective political judgment to determine whether it is complete

## Commercial model

The public protocol is the acquisition and trust layer. Sustainable revenue can be generated around it through:

- UNSOLVED Pro for journalists, researchers, and civic organizations
- UNSOLVED Institutional for official response and resolution workflows
- UNSOLVED Intelligence API for programmatic institutional-performance data
- Verification coordination services
- Sponsored challenge programs
- Enterprise data licensing and, later, predictive resolution intelligence

Public methodology remains public regardless of whether an institution is a paying customer.

## Repository status

**Protocol version:** `0.1-draft`  
**Pilot status:** Pre-launch  
**License:** No open-source license has been granted at this time. Standard copyright applies to repository contents, subject to GitHub's platform terms.

## Documents

This repository is being built in public. The first protocol package will include:

- `PROTOCOL.md`
- `RESOLUTION_STATES.md`
- `ACCOUNTABILITY_SCORE.md`
- `EVIDENCE_STANDARD.md`
- `GOVERNANCE.md`
- `COMMERCIAL_BOUNDARY.md`
- machine-readable challenge and resolution schemas

---

**UNSOLVED**  
*Don't trust the status. Verify the reality.*
