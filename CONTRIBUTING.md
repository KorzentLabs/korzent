# Contributing to Korzent

Korzent is a standards repository. Changes affect protocol contracts and must be treated as version events.

## Invariant Rules

1. No schema changes without version bump.
2. schema_hash must match canonical receipt.schema.json.
3. Strict verification only — no compatibility mode.
4. ZERO_HASH allowed only where explicitly defined.
5. No workflow/orchestration logic.

## Pull Requests

All changes must:

- Pass typecheck and tests.
- Include updated schema hash if receipt.schema.json changes.
- Preserve deterministic behavior.

Breaking changes require new protocol_version.
