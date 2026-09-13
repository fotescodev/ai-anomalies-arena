# Contributing

Two doors. Pick one.

## Door A — public incident (preferred)

Use this when the fact is already in the open: lab post, court order, regulator note, newsroom methods piece.

1. Open an issue with the **Incident** template, or skip straight to a PR.
2. Add a row to `data/incidents.json` that validates against `schema/incident.schema.json`.
3. Set `status` to `documented` only if a primary URL is in `sources`.
4. Keep the blurb to what the source actually says. No extra drama.

A maintainer will check the URL, the date, the model string, and the coordinates.

## Door B — whistleblower pack

Use the in-app **Locker**. Do not paste raw customer data, credentials, or private keys into a GitHub issue.

1. Hash the files locally in the locker.
2. Download `evidence-pack.json`.
3. Either keep it, or open an **Evidence** issue and paste *only* the manifest (hashes, names, sizes). Attach redacted excerpts if you must show content.

See `WHISTLEBLOWER.md`.

## What we will reject

- Claims with no source and no hash
- Weapon, exploit, or abuse instructions
- Doxxing, non-consensual intimate material, anything involving minors
- Secrets (tokens, passwords, private keys)
- PRs that rewrite someone else’s incident without a correction note

## Local check

No toolchain required. Open `index.html`. If you change the catalog, keep IDs stable (`kebab-case`).
