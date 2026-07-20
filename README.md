# Bank of us (bank-of-us)

Bank of us is Tasmania's only customer-owned bank, a mutual authorised deposit-taking institution (ADI) trading as B&E Ltd (brand "BNE LTD") and headquartered in Launceston, Tasmania. Formed from the former Bass & Equitable Building Society and rebranded to Bank of us in 2016, it is owned by its members rather than shareholders and offers home loans, personal and business banking, savings, and term deposits. As a regulated ADI it participates in Australia's Consumer Data Right (CDR / Open Banking) as a data holder, exposing a public, unauthenticated Product Reference Data (PRD) API that conforms to the Data Standards Body (DSB) Consumer Data Standards, and enabling customers to share account and transaction data with accredited data recipients under ACCC oversight.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bank-of-us/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bank-of-us/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Tasmania
- Mutual
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Bank of us CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data (PRD) API. A live GET on `https://api.bankofus.com.au/OpenBanking/cds-au/v1/banking/products` returns HTTP 200 with an `x-v` response header of 4 and a `data.products` array (27 products across home loans, personal/business banking, savings, and term deposits at the time of review). The endpoint conforms to the DSB Consumer Data Standards CDR Banking API (v1.36.0) and supports `GET /banking/products` and `GET /banking/products/{productId}`.

- **Human URL:** [https://www.bankofus.com.au/open-banking](https://www.bankofus.com.au/open-banking)
- **Base URL:** `https://api.bankofus.com.au/OpenBanking/cds-au/v1`

#### Tags

- Open Banking
- CDR
- Product Reference Data
- Banking
- Products

#### Properties

- [Documentation](https://www.bankofus.com.au/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/bank-of-us-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.bankofus.com.au/)
- [Documentation](https://www.bankofus.com.au/open-banking)
- [LinkedIn](https://www.linkedin.com/company/bank-of-us/)
- [Blog](https://www.bankofus.com.au/blog)
- [Privacy Policy](https://www.bankofus.com.au/privacy-policy)
- [Support](https://www.bankofus.com.au/contact)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
