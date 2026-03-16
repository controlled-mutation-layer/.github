# Controlled Mutation Layer (CML)

Structured mutation instrumentation at the authority boundary.

The **Controlled Mutation Layer (CML)** provides tools and SDKs for **observing, structuring, and instrumenting mutation events at the authority boundary** in software systems.

When authoritative state changes, CML makes that mutation **explicit, inspectable, and reproducible**.

---

## Architecture Stack

The projects relate as follows:

- **Emergent State Machine (ESM)** — control architecture  
- **Controlled Mutation Layer (CML)** — mutation instrumentation at the authority boundary  
- **Digital Learning Companion (DLC)** — reference implementation in education  

### Project Links

- **ESM organization:** https://github.com/emergent-state-machine/.github  
- **ESM specification:** https://github.com/emergent-state-machine/esm-spec  
- **DLC organization:** https://github.com/Digital-Learning-Companion  
- **DLC meta repository:** https://github.com/Digital-Learning-Companion/dlc  

---

## Conceptual Relationship

```text
Observations / Signals
          │
          ▼
     Projection
          │
          ▼
  Authority Boundary
          │
          ▼
 Authoritative Mutation
          │
          ▼
 Structured Turn Record
```

CML operates at the point where policy-controlled authority produces a real state change.

It does not define the full reasoning architecture.
It makes the mutation boundary observable, enforceable, and replayable.

## What CML Provides

- explicit mutation instrumentation

- structured Turn records

- reproducible mutation logging

- inspectable authority-boundary events

- implementation support for deterministic systems

## Repositories

### 📘 [cml-spec](https://github.com/controlled-mutation-layer/cml-spec)

Conceptual and normative definition of the mutation boundary and structured Turn records.

### 🐍 [sdk-python](https://github.com/controlled-mutation-layer/sdk-python)

Reference Python SDK for emitting structured Turn records and mutation events.

## Relationship to ESM

The Emergent State Machine (ESM) defines the broader architectural pattern that separates:

- Signals — measurement

- Projection — interpretation

- Authority — policy-controlled state mutation

The Controlled Mutation Layer (CML) provides a concrete mechanism for enforcing and instrumenting the authoritative mutation boundary defined by ESM.

In practical terms:

- ESM defines the control architecture

- CML instruments mutation events at the authority boundary

- CML records structured Turn events whenever an authoritative state mutation occurs.

These records make system evolution:

- observable

- replayable

- auditable

## Reference Implementation

A working educational implementation of the ESM + CML architecture is available in the Digital Learning Companion (DLC) project.

DLC demonstrates deterministic instructional reasoning using the Emergent State Machine and provides a public front door to the reference implementation.

DLC organization: https://github.com/Digital-Learning-Companion

DLC meta repository: https://github.com/Digital-Learning-Companion/dlc

## Why This Matters

Many software systems blur the line between:

- interpretation

- decision authority

- mutation

CML helps make that boundary explicit.

When a system changes authoritative state, that change should be:

- deliberate

- structured

- inspectable

- reproducible

CML exists to make those mutation events first-class.

## Independence and Scope

CML instruments mutation events at the authority boundary.

ESM defines a broader turn-based control architecture built on top of structured mutation.

CML can also be adopted independently of ESM in systems that require explicit mutation instrumentation without adopting the full ESM architecture.

---

## Repositories

### 📘 [cml-spec](https://github.com/controlled-mutation-layer/cml-spec)

Conceptual and normative definition of the mutation boundary and Turn structure.

### 🐍 [sdk-python](https://github.com/controlled-mutation-layer/sdk-python)

Reference Python SDK for emitting structured Turn records.
