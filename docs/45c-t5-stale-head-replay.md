# Stage 45C-2 — T5 Stale-Head and Replay Protection Test Fixture

- **Target Repository:** `akila-w/gh-check-identity-lab-20261031`
- **Base Commit:** `0b6b3e1193c76e046f9c9e81d7ee0d7813829bcb`
- **Commit Stage:** H0 (Initial Fixture Head)
- **Purpose:** Provide an isolated test fixture for verifying stale-head, stale-base, and replay protection guards under dedicated GitHub App 5555097 without modifying production or existing fixtures.

## Synthetic Verification Signals
- `catalogue.json`: `publication_signal = "PASS"` (consumed by default-branch synthetic Actions workflow `catalogue-publication-trusted.yml`).
- Prices, SKUs, and currencies remain strictly unchanged to satisfy the vendored verifier (`no-price-data-changes`).
- Trust-root paths and workflows remain strictly untouched.
