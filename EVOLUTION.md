# Korzent Evolution and Ratcheting (Informational)

**Status:** Informational  
**Version:** 1.0.0  
**Date:** 2025-03-03  

---

## Purpose

This document clarifies that evolution, ratcheting, epoch governance, authority evolution, and policy migration semantics are **out of scope** for Korzent v1.0.0.

This is an **informational** document. It does not contain normative requirements and does not modify the Korzent v1.0.0 protocol specification.

---

## Korzent v1.0.0 Invariant

Korzent v1.0.0 defines a minimal execution governance invariant that is **immutable within the version**. The protocol provides:

- Deterministic receipt structure and verification
- Schema-hash anchoring for protocol identity
- Ed25519 signature enforcement
- Authority-before-execution guarantees

These invariants do not change within v1.0.0. The protocol version and schema hash remain fixed for the lifetime of the version.

---

## Out of Scope for v1.0.0

The following concepts are intentionally **not defined** in Korzent v1.0.0:

- **Ratcheting protocols** for key rotation or policy updates
- **Epoch governance** for time-based authority transitions
- **Authority evolution** for changing trust roots over time
- **Policy migration** for updating authorization rules
- **Version negotiation** for protocol upgrades
- **Compatibility modes** for mixed-version environments

These are higher-layer concerns that belong in separate protocols built above Korzent's execution invariant.

---

## Layering Principle

Korzent is designed as a **foundational layer** that provides:

1. **Execution governance** - proof that authorized execution occurred
2. **Auditability** - verifiable receipts for past actions
3. **Authority binding** - cryptographic link between intent and outcome

Evolution and migration protocols operate **above** this layer, using Korzent receipts as their foundation while defining their own semantics for:

- Key rotation procedures
- Policy update mechanisms
- Trust root changes
- Version transition processes

---

## Implementation Guidance

Systems requiring evolution capabilities should:

1. **Use Korzent v1.0.0** as the stable execution invariant
2. **Define separate protocols** for evolution semantics
3. **Layer evolution logic** above Korzent's receipt verification
4. **Maintain clear boundaries** between execution governance and evolution logic

Korzent receipts provide the cryptographic foundation but do not prescribe how evolution should occur.

---

## Future Versions

Future versions of Korzent may define additional invariants, but:

- v1.0.0 remains stable and immutable
- Evolution between versions is not defined by the protocol itself
- Version transitions are implementation-specific concerns

This document does not imply any commitment to future versions or define any transition semantics.

---

## Relationship to PROTOCOL.md

This document is **informational only** and does not modify any normative requirements in `PROTOCOL.md`. All MUST, SHALL, and SHOULD requirements in the protocol specification remain unchanged and in full effect.

---

**End of informational document**
