# Governance

## Purpose

Hold a public, checkable list of AI anomalies. Separate the product (the arena) from the evidence (the record).

## Roles

- **Reporter** — files an incident or a locker pack
- **Curator** — checks sources, hashes, and schema. Does not “vote the truth”
- **Maintainer** — merges PRs, cuts releases of `index.html` and the catalog

For now maintainers are the repository owners. When three active curators exist, add them in this file by handle.

## Status machine

```
alleged  →  hashed  →  documented
                ↘ rejected
```

- `alleged` — claim only
- `hashed` — locker manifest with at least one SHA-256
- `documented` — primary URL that a stranger can open
- `rejected` — fails the contributing rules; stays out of the default feed

Votes never change status.

## Decision rule

A curator may promote to `documented` when **one** of these is true:

- The lab or deployer published it
- A court or regulator published it
- A newsroom published a methods-backed audit with the underlying documents

A curator may not promote on “everyone knows” or on an anonymous screenshot alone.

## Corrections

Wrong model, date, or quote: open a PR that adds a `correction` note on the same `id`. Do not delete the row. The catalog is an append-mostly ledger.
