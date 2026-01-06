# SIGNAL REQUIRED ARTIFACTS (Canonical V1)

Engine Key: **SIGNAL**  
Semantics: **DETERMINISTIC_TRANSFORM**  
Authority: Engine Repo (Binding addendum; enforced by CORE Runtime)

This document is an addendum to:
`ScrappyHub/Core-platform/GOVERNANCE/RUN_BUNDLE_SPEC.md`

SIGNAL is a TRUTH_ADJACENT_COMPUTE engine. It performs deterministic transforms only.

---

## Required (in addition to standard RUN_BUNDLE spec)

No additional artifacts are required beyond the standard CORE run bundle.

If SIGNAL emits extra transform artifacts (e.g., spectra, coherence tables), they MUST be:
- listed in `ARTIFACT_INDEX.json`
- hashed in `SHA256SUMS.txt`
- unit-tagged where applicable per `UNITS_AND_CONVERSIONS.md`

---

## Required Output Fields (RUN_OUTPUT.json)

RUN_OUTPUT.json MUST satisfy the engine OUTPUT_SCHEMA and MUST include:
- `semantics = DETERMINISTIC_TRANSFORM`
- `inputs_hash`
- `outputs_hash`

---

## Prohibitions

SIGNAL output MUST NOT include:
- causal/attribution/intent claims
- classifications or conclusions (vertical lens only)
- identity/governance/billing fields
- peer delivery indicators (inputs are delivered by CORE only)
