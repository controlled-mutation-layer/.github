# Controlled Mutation Layer (CML)

Structured mutation instrumentation at the authority boundary.

The Controlled Mutation Layer (CML) defines and enforces a structured boundary for authoritative state mutation in software systems.

When authoritative state changes, CML ensures that the mutation is:

- explicit
- authorized
- inspectable
- replayable

Every authoritative mutation emits a structured Turn record describing why the change was authorized and executed.

## Architecture Stack

The projects relate as follows:

- **Emergent State Machine (ESM)**: control architecture
- **Controlled Mutation Layer (CML)**: mutation boundary and instrumentation
- **Digital Learning Companion (DLC)**: reference implementation for education

## Project Links

- **ESM organization**: [github.com/emergent-state-machine/.github](https://github.com/emergent-state-machine/.github)
- **ESM specification**: [github.com/emergent-state-machine/esm-spec](https://github.com/emergent-state-machine/esm-spec)
- **DLC organization**: [github.com/Digital-Learning-Companion](https://github.com/Digital-Learning-Companion)
- **DLC meta repository**: [github.com/Digital-Learning-Companion/dlc](https://github.com/Digital-Learning-Companion/dlc)

## Conceptual Relationship

```text
Observations / Signals
          │
          ▼
     State Construction
          │
          ▼
      Projection
          │
          ▼
 Relevance Determination
          │
          ▼
   Policy Evaluation
          │
          ▼
  Authority Boundary (CML)
          │
          ▼
 Authoritative Mutation
          │
          ▼
 Structured Turn Record
```

CML operates at the point where policy-controlled authority produces a real state change.

It does not define the full reasoning architecture. It makes the mutation boundary explicit, enforceable, and replayable.

## What CML Provides

- enforced mutation boundary for authoritative state changes
- structured Turn records for every mutation
- reproducible, deterministic mutation logging
- inspectable decision-boundary events
- SDKs and tooling for instrumenting governed systems

## Repositories

### [cml-spec](https://github.com/controlled-mutation-layer/cml-spec)

Conceptual and normative definition of the mutation boundary and structured Turn records.

### [sdk-python](https://github.com/controlled-mutation-layer/sdk-python)

Reference Python SDK for emitting structured Turn records and mutation events.

## Relationship to ESM

The Emergent State Machine (ESM) defines a control architecture that separates:

- **Signals**: measurement
- **State Construction**: coherent interpretation
- **Projection**: policy-space representation
- **Relevance Determination**: decision engagement
- **Authority**: policy-controlled outcome selection

The Controlled Mutation Layer (CML) provides the mechanism that enforces and records the authoritative mutation boundary defined by ESM.

In practical terms:

- ESM defines the reasoning and decision architecture
- CML enforces where authority is applied
- CML emits a Turn record for every authorized mutation

These Turn records make system evolution:

- observable
- replayable
- auditable

## Reference Implementation

A working implementation of the ESM + CML architecture is available in the Digital Learning Companion (DLC) project.

DLC demonstrates deterministic reasoning using ESM and exposes CML Turn records as part of system behavior.

- **DLC organization**: [github.com/Digital-Learning-Companion](https://github.com/Digital-Learning-Companion)
- **DLC meta repository**: [github.com/Digital-Learning-Companion/dlc](https://github.com/Digital-Learning-Companion/dlc)

## Why This Matters

Many systems blur the boundary between:

- interpretation
- decision authority
- state mutation

CML makes this boundary explicit.

When a system changes authoritative state, that change should be:

- authorized by policy
- structurally represented
- inspectable after the fact
- reproducible under the same conditions

CML transforms mutation from an implicit side effect into a governed operation.

## Independence and Scope

CML focuses specifically on instrumenting and enforcing the authority boundary where state mutation occurs.

While it is designed to operate within ESM, CML can be adopted independently in systems that require:

- explicit mutation tracking
- auditability of decisions
- deterministic mutation control

ESM defines the broader architecture. CML defines and enforces the mutation boundary within it.
