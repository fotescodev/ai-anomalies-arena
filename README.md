# AI Anomalies Arena

Open arena for **documented** AI anomalies. Not a vibe check. Not a scoreboard for labs.

The product question is narrow: *did this system do something the public record can show?* Votes are not proof. Screenshots without a hash are not proof. A lab note, a court filing, a logged trial, or a hashed original file can be.

Live repo: https://github.com/fotescodev/ai-anomalies-arena

## Use it

Open `index.html` in a browser. No build step. Catalog loads from `data/incidents.js` on `file://` and from `data/incidents.json` over HTTP.

- **Feed** — incidents, Reddit-style scoring, filters by model and type
- **Map** — where the disclosure or impact sat
- **Proof** — model, operator, date, excerpt, primary sources
- **Locker** — whistleblower evidence pack: drop files, get SHA-256, download a manifest
- **Project** — how the wheel turns (schema, PR, issue)

## Trust layers

| Layer | What it means |
| --- | --- |
| `documented` | Primary public source (lab writeup, court, regulator, named newsroom audit) |
| `alleged` | Community report waiting on a source |
| `hashed` | Original file hashed in the locker; contents not published |

The arena does not answer “is AI an issue.” It publishes the record so anyone can look.

## Contribute an incident

1. Copy `schema/incident.schema.json`.
2. Add one object to `data/incidents.json`.
3. Every `documented` row needs at least one working source URL.
4. Open a pull request. Template is in `.github/PULL_REQUEST_TEMPLATE.md`.

## Whistleblow without standing up a server

The locker runs in the browser. Files never leave the device unless you download the pack or attach a hash manifest to an Evidence issue. Read `WHISTLEBLOWER.md`.

## License

Apache License 2.0. See `LICENSE`.
