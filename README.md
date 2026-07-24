# Paymentus (paymentus)

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
