# Evidence Standard v0.1

UNSOLVED exists to distinguish administrative claims from physical reality. Evidence therefore needs to be reproducible, attributable, and tamper-evident without forcing sensitive raw media into a public repository.

## Evidence classes

### Administrative evidence
Examples:
- 311 or service-request records;
- work-order status;
- permit closure;
- inspection disposition;
- official agency correspondence;
- contractor completion notice.

### Physical evidence
Examples:
- timestamped photo or video;
- qualified inspection report;
- sensor reading;
- independent field observation;
- authoritative geospatial imagery when timing and resolution are sufficient.

### Corroborating evidence
Examples:
- multiple independent observations;
- local news reporting;
- public meeting record;
- official maintenance history.

Corroborating evidence may strengthen a conclusion but does not automatically satisfy a Resolution Contract.

## Minimum provenance record

Each evidence item SHOULD capture:

- evidence ID;
- challenge ID;
- source class;
- source or submitter identifier where lawful and appropriate;
- capture timestamp;
- ingestion timestamp;
- location metadata where relevant;
- media/document MIME type;
- SHA-256 hash of the original asset;
- SHA-256 hash of any public/redacted derivative;
- retention classification;
- reviewer notes;
- supersedes/contradicts relationships.

## Public versus restricted evidence

Public transparency does not require publishing sensitive raw files.

Raw evidence MAY remain restricted when it contains:

- faces of minors or uninvolved persons;
- home addresses or private interiors;
- license plates or identifying documents;
- phone numbers, email addresses, or account numbers;
- precise location data that creates a safety risk;
- metadata that would expose a vulnerable submitter.

In such cases UNSOLVED SHOULD publish only the minimum necessary derivative, provenance metadata, cryptographic hash, and verification conclusion.

## Review standard

For Phase 1, final verification SHOULD be independently reproducible by two reviewers using the Resolution Contract and admissible evidence.

Reviewer agreement is itself a pilot metric.

## Contradictory evidence

When credible evidence conflicts:

1. preserve both records;
2. do not overwrite prior conclusions;
3. record the contradiction relationship;
4. move the case to `UNVERIFIABLE` or `DISPUTED` when appropriate;
5. document what additional evidence would resolve the conflict.

## Evidence immutability

An evidence file may need redaction, access restriction, or lawful deletion. UNSOLVED must therefore avoid claiming that files are literally immutable.

Instead, the protocol preserves an auditable event history showing what was received, what hash it carried, what transformations occurred, and why availability changed.

No blockchain is required for Phase 1. Conventional cryptographic hashes, signed logs, controlled storage, and append-oriented audit events are sufficient.
