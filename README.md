# RobMac Software

Static bilingual website using semantic HTML, shared CSS, system fonts and the
original brand SVGs. No JavaScript, frameworks, payment SDKs or build dependencies.
Automatic light/dark themes use `prefers-color-scheme`.

## Public routes

| English | Spanish | Purpose |
| --- | --- | --- |
| `/` | `/es/` | Brand and Engineering Toolkit introduction |
| `/support/` | `/es/support/` | Optional voluntary contributions |
| `/engineering-toolkit/privacy/` | `/engineering-toolkit/privacy/es/` | Engineering Toolkit privacy policies |

Support pages reuse `assets/css/styles.css` and unchanged brand SVGs. They include
canonical URLs, reciprocal English/Spanish and x-default alternate links, language
navigation, home links, privacy information and secure external provider links.
Engineering Toolkit remains free forever. Contributions confer no functionality,
privileges, digital goods or services, exclusive content or rewards.
Both homepages also offer compact voluntary-support cards inside the Contact
section, beneath the existing email and GitHub links.

Owner-selected destinations, without tracking parameters:

- PayPal — international / USD: <https://www.paypal.com/ncp/payment/CKD4M9EU2QCD2>
- Mercado Pago — Mexico / MXN: <https://link.mercadopago.com.mx/robmacsoftware>

Payment processing takes place externally. No checkout widgets, forms, analytics,
advertising, external fonts, accounts or backend are included. Provider links
announce new tabs and use `noopener noreferrer` plus `no-referrer`. Their presence
does not establish Google Play eligibility or availability in every country.

## Local preview

Double-click the ignored `RobMac_Local_Preview.bat`, or run Python 3.12:

```powershell
python -B RobMac_Local_Preview.py --no-browser
```

The helper binds only to `127.0.0.1:8003` and serves an isolated temporary snapshot
containing exactly 11 explicitly allowlisted public files. It never serves the
repository directory. Stop with Ctrl+C; restart after public-file edits.

Visit <http://127.0.0.1:8003/support/> or
<http://127.0.0.1:8003/es/support/>. The existing home and privacy pages are also
available. Directory listings, Git metadata, launchers, README, review drafts and
unknown routes are excluded. Keep the allowlist explicit; do not replace it with
recursive copying. The local helper, launcher, snapshots and review materials are
ignored and are not part of a future commit.

## Phase 18 publication boundary

Both privacy policies include the owner-confirmed commitments and external
contribution disclosures, revised October 16, 2026 for this authorized website
release. Review drafts, remaining confirmations, validation evidence and completion
reports remain in the ignored `privacy_review_sources/` directory and are excluded
from the release. They are not public website pages.

The local allowlist update in `RobMac_Local_Preview.py` must be retained separately
if transferring this checkout; Git will not include it automatically.

The contribution pages are separable from the app's distribution decision. Creator
recipient eligibility, processor-fee treatment, operational merchant-data details,
checkout-specific provider notices and the full app-to-checkout journey still
require review. The owner's confirmed privacy commitments are reflected in both
languages; they apply to processing controlled by RobMac Software.
Neither the website nor the absence of digital rewards establishes Google Play
approval. The owner authorized committing these eight website source files and a
normal push to `origin/main`, allowing the existing GitHub Pages mechanism to
publish them. This authorization does not cover app publication, Play Console,
payment accounts or changes to Git/hosting settings.

Phase 18 remains open. Phase 19 has not started. Local validation does not establish
live availability; the release report records separate post-push HTTP and content
verification. Website publication does not establish Google Play compliance or
overall app-release readiness.
