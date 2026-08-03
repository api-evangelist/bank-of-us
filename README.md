# Bank of us (bank-of-us)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
