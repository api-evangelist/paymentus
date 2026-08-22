# Paymentus (paymentus)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Paymentus (NYSE: PAY) is an Addison, Texas-based cloud billing and payment technology company founded in 2004 that runs one of the largest electronic bill presentment and payment (EBPP) networks in North America. Its Intelligent Payment Platform, Instant Payment Network (IPN), BillWallet, and Profit by Paymentus (AP/AR) products let utilities, government agencies, insurers, telecom, healthcare, higher education, and financial institutions accept and disburse payments across web, mobile, IVR, call center, and agent channels using cards, ACH/eCheck, cash, and digital wallets (PayPal, Venmo, Apple Pay, Google Pay). Home market: United States.

Paymentus is API-native, but its developer surface is access-controlled. The developer portal at [developer.paymentus.io](https://developer.paymentus.io/) is live and public, yet the full API reference, specifications, and testing environment sit behind a request-access / NDA gate. No downloadable OpenAPI/Swagger specification is published on the public web. The real payment (XOTP) surface, JWT/pre-shared-key authentication, and granular scopes are documented publicly through the Paymentus Node.js Server SDK on npm.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/paymentus/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/paymentus/refs/heads/main/apis.yml)

## Tags

- Payments
- United States
- Bill Payment
- Electronic Bill Presentment
- Payment Processing
- Payment Gateway
- Disbursements
- ACH
- Real-Time Payments
- Tokenization

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Paymentus XOTP API

The XOTP (Paymentus payment) API exposes core Service Commerce operations — make payment (Sale), account inquiry, payment history, void/cancel payment, customer profile CRUD and list, wallet/payment-method tokenization, linked accounts, and AutoPay management. Requests carry a Bearer JWT and are scoped with granular XOTP scopes.

- **Human URL:** [https://developer.paymentus.io/docs/Reference](https://developer.paymentus.io/docs/Reference)
- **Base URL:** `https://api.paymentus.com`

#### Tags

- Payments
- Bill Payment
- Tokenization
- AutoPay
- Disbursements

#### Properties

- [Documentation](https://developer.paymentus.io/)
- [API Reference](https://developer.paymentus.io/docs/Reference)
- [SDK](https://www.npmjs.com/package/@paymentus/xotp)

### Paymentus Authentication API

Issues short-lived JWT access tokens for the XOTP payment surface. A client signs a request with a pre-shared key (identified by a key id / kid and three-letter application acronym / tla), declares the granular scopes it needs (or a pixel that maps to those scopes), and receives a Bearer token used on subsequent XOTP calls.

- **Human URL:** [https://developer.paymentus.io/](https://developer.paymentus.io/)
- **Base URL:** `https://api.paymentus.com`

#### Tags

- Authentication
- JWT
- Scopes

#### Properties

- [Documentation](https://developer.paymentus.io/)
- [SDK](https://www.npmjs.com/package/@paymentus/auth)

## Common Properties

- [Website](https://www.paymentus.com/)
- [Developer Portal](https://developer.paymentus.io/)
- [API Reference](https://developer.paymentus.io/docs/Reference)
- [Status Page](https://status.paymentus.com/)
- [GitHub Organization](https://github.com/paymentus)
- [LinkedIn](https://www.linkedin.com/company/paymentus/)
- [Terms of Service](https://www.paymentus.com/customer-terms-privacy/website-condition-of-use/)
- [Privacy Policy](https://www.paymentus.com/customer-terms-privacy/website-privacy-notice-united-states/)
- [Investor Relations](https://ir.paymentus.com/)

## Review

No downloadable OpenAPI/Swagger specification is published publicly. The developer portal is live (HTTP 200) but request-access/NDA-gated; the payment (XOTP) API, JWT/pre-shared-key auth model, and scope catalog are documented via the public npm SDK. See [`review.yml`](review.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
