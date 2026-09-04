# Resolution & Responsibility States

UNSOLVED tracks **resolution** and **responsibility** as separate dimensions. A challenge can remain unresolved while ownership of the problem changes or is disputed.

## Resolution states

### `REPORTED`
The issue has been submitted with sufficient opening evidence to create a challenge, but the relevant institution has not yet acknowledged it.

### `OPEN`
The issue remains physically unresolved and has been acknowledged by the institution or otherwise accepted into the tracked process.

### `CLAIMED_RESOLVED`
An official source reports the issue as completed, closed, repaired, or otherwise finished, but independent physical verification has not yet satisfied the Resolution Contract.

### `VERIFIED_RESOLVED`
Independent evidence satisfies the predeclared Resolution Contract. This is the only state that counts as a verified successful closure.

### `DISPUTED`
Official closure directly conflicts with independent evidence showing that the physical condition remains unresolved or materially fails the Resolution Contract.

### `UNVERIFIABLE`
Available evidence is insufficient, contradictory, inaccessible, unsafe to collect, or otherwise incapable of supporting a definitive conclusion.

## Responsibility states

### `UNASSIGNED`
No responsible institution has yet been identified with sufficient confidence.

### `CANDIDATE`
One or more institutions appear plausibly responsible, but ownership has not been confirmed.

### `ACCEPTED`
A responsible institution has acknowledged ownership or authoritative records establish responsibility.

### `DISPUTED`
Responsibility is actively contested or repeatedly transferred among institutions.

### `TRANSFERRED`
Responsibility has been formally transferred to another institution, contractor, utility, or jurisdiction.

## Required transition evidence

Every state transition SHOULD record:

- prior state;
- new state;
- timestamp;
- evidence references;
- actor or automated rule that initiated the transition;
- reviewer or verification decision when required;
- protocol version.

## Why the split matters

Example:

```text
Resolution: OPEN
Responsibility: DISPUTED
```

This means the physical problem still exists while multiple agencies are bouncing ownership.

Later the same challenge may become:

```text
Resolution: VERIFIED_RESOLVED
Responsibility: ACCEPTED
Institution: Example Department of Transportation
```

Keeping these fields separate allows UNSOLVED to measure both **resolution latency** and **responsibility latency** without corrupting one with the other.
