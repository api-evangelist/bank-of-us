---
name: Look up Bank of us banking products
description: >-
  Discover Bank of us's publicly available banking products (home loans, personal
  and business banking, savings, term deposits) and retrieve full product detail —
  rates, fees, features, eligibility and constraints — via the public,
  unauthenticated CDR Product Reference Data API. No credentials or consent required.
api: openapi/bank-of-us-cds-banking-products-openapi.yml
operations:
- listBankingProducts
- getBankingProductDetail
---

# Look up Bank of us banking products

Bank of us's Product Reference Data (PRD) endpoints are **public and
unauthenticated**. The only access control is API version negotiation via the
mandatory `x-v` request header. Base URL:
`https://api.bankofus.com.au/OpenBanking/cds-au/v1`.

## Rules

- Always send the `x-v` request header. For `listBankingProducts` the currently
  served version is `4`; for `getBankingProductDetail` it is `7`. Omitting it or
  requesting an unsupported version returns `406` (Not Acceptable) with a
  `urn:au-cds:error:cds:all:header:invalid-version` error. (Confirmed live: `x-v: 3`
  -> 406, `x-v: 4` -> 200.)
- No `Authorization` header, API key, or consent is needed for these two
  operations. (All other CDR banking endpoints require ADR accreditation + MTLS +
  consumer consent, brokered via Bank of us Internet Banking — out of scope for
  this skill.)
- Responses wrap `{ data, links, meta }`. Errors use the CDS envelope
  `{ "errors": [ { "code", "title", "detail", "meta" } ] }` — see
  `errors/bank-of-us-problem-types.yml`.

## Steps

1. **List products** — call `listBankingProducts`
   (`GET /banking/products`) with header `x-v: 4`. Optionally filter with
   `effective` (`CURRENT` | `FUTURE` | `ALL`, default `CURRENT`),
   `product-category` (e.g. `RESIDENTIAL_MORTGAGES`, `TERM_DEPOSITS`,
   `TRANS_AND_SAVINGS_ACCOUNTS`, `BUSINESS_LOANS`), `brand`, and `updated-since`.
   Page with `page` / `page-size`; read `meta.totalRecords` (27 at time of review)
   and `meta.totalPages`, and follow `links.next` until absent.

2. **Pick a product** — each item in `data.products` carries a `productId`,
   `productCategory`, `name`, and `description`.

3. **Get full detail** — call `getBankingProductDetail`
   (`GET /banking/products/{productId}`) with header `x-v: 7`, passing the
   `productId` from step 2. The response's `data` (BankingProductDetailV7) includes
   `features`, `constraints`, `eligibility`, `fees`, `depositRates`,
   `lendingRates`, `bundles`, and `instalments`. A `404`
   (`urn:au-cds:error:cds:banking:product:invalid`) means the `productId` is not
   valid.

## Notes

- Product `productId` values are data-holder-specific and not permanence
  guaranteed — always re-list rather than caching ids long-term.
- See `conventions/bank-of-us-conventions.yml` for pagination and versioning
  details.
