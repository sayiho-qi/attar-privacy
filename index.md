# Attar Privacy Policy

_Last updated: 2026-07-12 · Applies to the Attar browser extension (hosted v1, incl. paid membership / top-up billing)_

Attar is a **hosted** browser extension. This policy states exactly what happens to your data.

## What Attar does with your data

1. **Content you choose to distill is processed on our hosted service.** When you
   click Capture or paste a link, the extension extracts the page text (and, for
   videos, downloads in your own browser the media you selected) and sends it to
   our backend, which transcribes, distills, and — if you leave 画面理解 on —
   reads key video frames. **Transient audio/video and extracted frames are
   deleted after processing** (they are not stored long-term). The uploaded video
   frames may contain identifiable third parties (bystanders / faces / private
   scenes) — we process them only to produce your note and delete them after use.
2. **Cookies never leave your browser.** The extension never reads, stores or
   transmits cookies, session tokens or login state. The backend actively
   **rejects** any request containing cookie/session/key-shaped fields.
3. **Account.** We store your **email** and your **usage counts** (次数) to run
   your account and enforce quota. Login is a 6-digit email code — no password.
4. **Anonymous usage analytics (you can turn it off).** We collect anonymous
   behavior events — an **action name, timestamp and short result code** plus
   low-cardinality context (platform, content type, a coarse duration bucket).
   This **never** includes your page text, transcripts, note bodies, links with
   content, cookies, keys, email or precise device/IP. Events are keyed by an
   internal numeric user id (not your email). **You can turn analytics off** in
   the extension's Setup — when off, the extension does not send any events and
   clears its local buffer. Passive analytics detail is retained ~90 days, then
   deleted (aggregates may be kept).
5. **Ratings & feedback you submit.** When you rate a result (👍/👎) or send
   feedback, we store what you submit: for a 👎, the reason chips + any optional
   text you type; for feedback, your message (and an optional contact email if you
   give one). A rating also carries zero-content context tags (result type /
   platform / duration bucket, etc.) so we can see what's working — the rating UI
   discloses this, and it applies even if you turned analytics off (rating is
   something you actively submit).
6. **Payment (membership & top-up).** Attar has a free monthly quota plus optional
   paid plans (annual membership and a top-up pack). **Payment is processed by
   third-party payment providers** — **Stripe** (overseas card payments) and
   **虎皮椒 / Xunhupay** (domestic WeChat Pay / Alipay). You enter your card or
   wallet details **on the payment provider's page, not in Attar**. We **never**
   receive or store your card number, CVV, bank/wallet credentials or full payment
   receipt. What we store is **order metadata only**: an
   internal order id, the plan/SKU you bought, the amount and currency, the order
   status, timestamps, and the provider's transaction reference — linked to your
   account so we can grant your quota. Membership is a one-time annual charge, **not
   auto-renewing**. Refund handling follows the Terms of Service.

## Third-party processors

We share the minimum data needed with the following processors. We do **not** sell
your data to anyone.

- **Anthropic** (Claude Haiku) — content distillation + key-frame vision. Receives
  the extracted text / frames of the content you chose to distill.
- **ASR (speech-to-text) provider** — **OpenAI** (OpenAI-compatible Whisper),
  with **Groq** / **Deepgram** as interchangeable alternates. Receives the audio of
  the video you chose, to transcribe it. Transient audio is deleted after use.
- **Resend** — transactional email delivery. Receives your email address to send
  your 6-digit login code. It is not used for marketing.
- **Stripe** — overseas card payment processing. You transact on Stripe's page;
  Attar receives only order metadata (above).
- **虎皮椒 / Xunhupay** — domestic (China) WeChat Pay / Alipay aggregation. You
  transact on the provider's page; Attar receives only order metadata (above).
- **Cloudflare** — DNS, TLS and edge/CDN in front of `api.useattar.com`. Sees
  request metadata (e.g. IP) in transit as part of routing.
- **Vultr** — cloud server hosting for our backend and database.

## What Attar stores locally (in your browser's extension storage)

- Your session token + email (so login survives a restart) and Setup preferences
  (including the 使用分析 opt-out toggle and the pending-event buffer).
- Saved notes are plain `.md` files you download to your disk — they are yours.

## Data deletion

- **Delete your account from the extension** (Setup → 注销账号并删除我的数据):
  this removes your account email, usage/behavior events, ratings and feedback,
  and anonymizes your metering records. Irreversible.
- Uninstalling the extension removes local extension storage.
- Downloaded `.md` files are on your disk — delete them yourself.

## Data disclosure summary (Chrome Web Store form basis)

- **Collected by developer:** account email; anonymous usage analytics; user-
  submitted ratings/feedback; processed content (transiently, deleted after use);
  **order metadata** for purchases (no card data).
- **Not collected by developer:** card numbers / payment credentials (handled by
  the payment providers); browser cookies / login state (rejected in transit).
- **Sold:** nothing.
- **Processing location:** our hosted backend; third-party processors above.

## Your rights (GDPR / CCPA-lite posture, overseas users)

You may request access to or deletion of your data; account deletion is
self-service in Setup. Contact us for any other request.

## Contact

Owner: sayiho@gmail.com
