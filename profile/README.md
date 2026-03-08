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

## Relationship to ESM

The **Emergent State Machine (ESM)** defines the architectural pattern that separates:

- Signals — measurement
- Projection — interpretation
- Authority — policy-controlled state mutation

The **Controlled Mutation Layer (CML)** provides a concrete mechanism for enforcing the authoritative mutation boundary defined by ESM.

In other words:

ESM defines the architecture.  
CML provides an implementation pattern for enforcing the mutation boundary.

Learn more about the architecture here:

👉 https://github.com/emergent-state-machine/.github


CML instruments mutation events.

ESM defines a broader turn-based control architecture built on top of structured mutation.

CML can be adopted independently of ESM.
