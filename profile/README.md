# Controlled Mutation Layer (CML)

Controlled Mutation Layer (CML) provides tools and SDKs for observing and structuring mutation events at the decision boundary in software systems.

When authoritative state changes, CML makes that mutation explicit.

---

## Repositories

### 📘 cml-spec

Conceptual and normative definition of the mutation boundary and Turn structure.

### 🐍 sdk-python

Reference Python SDK for emitting structured Turn records.

---

## Relationship to Emergent State Machine (ESM)

CML instruments mutation events.

ESM defines a broader turn-based control architecture built on top of structured mutation.

CML can be adopted independently of ESM.
