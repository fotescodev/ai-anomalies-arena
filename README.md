# AI Anomalies Arena

Open arena for **documented** AI anomalies. Not a vibe check. Not a scoreboard for labs.

The product question is narrow: *did this system do something the public record can show?* Votes are not proof. Screenshots without a hash are not proof. A lab note, a court filing, a logged trial, or a hashed original file can be.

## Use it

Open `index.html` in a browser. No build step.

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

Do not invent model names, quotes, or coordinates. If the model is unknown, say so.

## Whistleblow without standing up a server

The locker runs in the browser.

- Files never leave the device unless *you* download the pack or attach it somewhere
- Each file is hashed with SHA-256 so you can prove later that a given file existed
- The pack is a JSON manifest (`aaa-evidence-v1`) plus your originals
- You can open a GitHub issue from the generated body, or keep the pack offline

Read `WHISTLEBLOWER.md` before you drop production logs.

## Repo layout

```
index.html                 arena app
data/incidents.json        public catalog
schema/incident.schema.json
WHISTLEBLOWER.md           how evidence is handled
CONTRIBUTING.md
GOVERNANCE.md
SECURITY.md
LICENSE                    Apache-2.0
```

## License

Apache License 2.0. See `LICENSE`.
