# UNSOLVED Protocol Specification v0.1

## Purpose

UNSOLVED is a public accountability protocol for determining whether a reported institutional problem has been resolved in physical reality, not merely marked complete in an administrative system.

The protocol separates four facts that are often collapsed into one:

1. a problem was reported;
2. an institution acknowledged or claimed responsibility;
3. an official system changed status;
4. independent evidence confirmed the physical condition.

A challenge is not considered verified resolved until the predeclared Resolution Contract is satisfied.

## Challenge object

Each challenge MUST define before launch:

- immutable challenge identifier;
- issue type and severity class;
- precise location or bounded area;
- candidate responsible institution;
- official case/ticket identifier when available;
- opening evidence;
- Resolution Contract;
- accepted evidence classes;
- escalation schedule and ceiling;
- creation timestamp;
- public status;
- responsibility status.

## Resolution Contract

The Resolution Contract is the precommitment that defines `done`.

It MUST be:

- objective enough for two independent reviewers to reach the same conclusion;
- defined before public escalation begins;
- tied to observable or authoritative evidence;
- narrow enough to avoid political or policy interpretation;
- preserved in version history after launch.

A Resolution Contract SHOULD specify:

- the physical condition required for closure;
- minimum evidence count;
- observation timing requirements;
- official records required, if any;
- verifier qualifications, if any;
- disqualifying evidence conditions;
- reinspection window when appropriate.

Example: a streetlight challenge may require all identified fixtures to illuminate during darkness in a timestamped, location-verified observation after an official repair disposition.

## Dual-layer verification

UNSOLVED distinguishes:

### Administrative layer
What the responsible institution or official system claims.

Examples:
- ticket status;
- permit closure;
- work-order disposition;
- public agency response.

### Physical layer
What independent evidence shows exists in the real world.

Examples:
- timestamped media;
- qualified inspection;
- sensor observation;
- independent field verification.

Administrative closure alone MUST NOT produce `VERIFIED_RESOLVED`.

## Evidence provenance

Each evidence record SHOULD include:

- uploader or source class;
- source timestamp;
- ingestion timestamp;
- location metadata when relevant;
- original file hash;
- redacted/public derivative hash when applicable;
- relationship to challenge;
- reviewer decisions;
- superseding or contradiction links.

Raw sensitive evidence does not need to be publicly distributed. Public records may expose hashes, metadata, redacted derivatives, and verification conclusions while restricted evidence remains access-controlled.

## Escalation

Phase 1 uses pledge-backed targets rather than captured funds.

The escalation target MAY increase according to a published schedule while the challenge remains unresolved. The schedule and maximum ceiling MUST be declared at challenge launch.

The target is a public mobilization metric, not money that magically compounds.

## Pilot scope

Phase 1 should contain 10–25 challenges from a single or tightly related issue category with binary or near-binary outcomes.

Preferred pilot characteristics:

- one observable condition;
- one geographic point or small bounded area;
- identifiable authority;
- public administrative trail;
- low-cost reverification;
- little or no subjective interpretation.

## Versioning

Material protocol changes require a documented Git commit and version increment.

Challenges already launched SHOULD retain the Resolution Contract and scoring methodology version that governed them, unless a correction is necessary for safety, legality, fraud, or obvious factual error. Such corrections must remain auditable.
