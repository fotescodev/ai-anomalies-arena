# Whistleblower locker

The locker exists so someone inside a lab, a vendor, or a deploy can put **evidence on the record** without first trusting a server.

## What the locker does

- Accepts screenshots, PDFs, logs, transcripts, and short video
- Computes SHA-256 in the browser
- Writes an `aaa-evidence-v1` manifest you can download
- Stores the pack in this browser so you can reopen it
- Does **not** upload bytes to this project

A hash is proof that a specific file existed at pack time. It is not proof of what the file means. Curators still have to read.

## Before you drop files

Strip:

- API keys, session cookies, passwords, private keys
- Customer names, medical data, financial account numbers
- Faces and badge photos you do not have a right to publish
- Anything involving minors

If the raw log is the only proof, redact first, hash both the redacted file and (privately) the original. Put only the redacted hash in a public issue.

## Anonymity

The form does not ask for an account. GitHub issues are not anonymous. If identity is a risk, stay on the local pack and move it through a channel you already trust.

This project cannot protect you from your employer or from a court. It can only keep your bytes off our servers.

## What happens after a pack is public

1. A curator checks that the manifest is well-formed.
2. Status on the feed becomes `hashed` until a primary public source exists.
3. Status becomes `documented` only when a source that others can open is attached.
4. The original files stay with you unless you choose to send them.

## Evidence types we can use

- Eval or production transcript with timestamps
- Tool-call log that shows the action
- Court or regulator PDF
- Newsroom methods appendix
- Screenshot plus the URL and time it was taken

A cropped meme is not enough.
