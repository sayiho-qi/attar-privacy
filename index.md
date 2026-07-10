# Attar Privacy Policy

_Last updated: 2026-07-10 · Applies to the Attar browser extension v0.3.x_

Attar is a local-first browser extension. This policy states exactly what the
extension does with data — aligned with the project's architecture decisions
(ADR 0002 privacy boundary, ADR 0005 key boundary), which are enforced in code
and covered by automated tests.

## What Attar does with your data

1. **Page content goes only to your own machine.** When you click Capture (or
   run Creator Watch), the extension extracts the visible text of the page and
   sends it to a **companion API service running on your own computer at
   `http://127.0.0.1:8000`**. Nothing is sent to any server operated by us —
   we do not operate any server.
2. **Cookies never leave your browser.** The extension never reads, stores or
   transmits cookies, session tokens or login state. The companion service
   actively **rejects** any request containing cookie/session/key-shaped
   fields (middleware-enforced).
3. **No telemetry. No analytics. No crash reporting.** There is none — so this
   policy says "none".
4. **Cloud engine is opt-in and user-configured.** If — and only if — you put
   your own OpenAI API key into the companion service's environment (`.env` on
   your machine) **and** explicitly select the cloud engine (or explicitly
   click "Synthesize DNA (cloud)"), the companion service on your machine
   sends the **already-extracted text** (and, for DNA synthesis, distilled
   five-dimension text plus item identifiers) directly to OpenAI. This payload
   never contains cookies, API keys, or identity fields. Your API key is never
   stored in, displayed by, or transmitted through the extension.
5. **Scheduled watching is off by default** and bounded by a kill switch, a
   daily run quota and a per-creator cap. Every run is recorded in a local run
   log, including which engine it used.

## What Attar stores locally (in your browser's extension storage)

- Extension configuration (engine preference, one-time notice acknowledgement).
- Creator Watch configuration (creators you added, schedules).
- Review-queue drafts (distilled notes pending your review) and account DNA
  documents.
- De-duplication ledgers (which items were already processed — prevents
  double-billing) and a local run log.

Saved notes are plain `.md` files downloaded to your disk — they are yours.

## Data deletion

Uninstall the extension (removes all extension storage) and delete any `.md`
files you downloaded. If you configured a cloud key, remove it from your
companion service `.env`. There is no server-side data to delete — none exists.

## Data disclosure summary (Chrome Web Store form basis)

- Collected by developer: **nothing**.
- Sold: **nothing**.
- Processing location: **the user's own machine**; cloud tier is the user's
  own key, direct from the user's machine to OpenAI, opt-in per the above.

## Contact

Owner: sayiho@gmail.com

_Hosting note (OQ-6): publish this document at a publicly readable URL (GitHub
Pages / gist / repo raw) and paste that URL into the store listing's privacy
policy field — Owner decides the final URL at submission time._
