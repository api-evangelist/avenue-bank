---
name: List Avenue Bank products (public CDR PRD)
description: Retrieve Avenue Bank's publicly available banking products and product detail via the unauthenticated Consumer Data Right Product Reference Data (PRD) surface.
api: openapi/avenue-bank-cds-banking-openapi.json
method: generated
generated: '2026-07-21'
operations:
  - listBankingProducts
  - getBankingProductDetail
---

# List Avenue Bank products (public CDR PRD)

The Product Reference Data (PRD) family is **public and unauthenticated** under the
Consumer Data Standards. No OAuth token or consumer consent is required.

> Note: Avenue Bank's live CDR data-holder surface is unverified — a probe of
> `https://api.avenuebank.com.au/cds-au/v1/banking/products` returned HTTP 403 (WAF)
> on 2026-07-21. Treat these steps as the standard contract, not a confirmed live endpoint.

## Steps

1. Call **`listBankingProducts`** (`GET /banking/products`).
   - Send the version header `x-v: 4` (and optionally `x-min-v`).
   - Optional filters: `product-category`, `effective`, `updated-since`, `brand`.
   - Paginate with `page` / `page-size`; read `meta.totalPages` and follow `links.next`.
2. For each product of interest, call **`getBankingProductDetail`**
   (`GET /banking/products/{productId}`) with `x-v` set, using the `productId` from step 1.

## Rules

- No authentication; do not attach a bearer token to PRD calls.
- Handle errors from the `ResponseErrorListV2` envelope (see `errors/avenue-bank-problem-types.yml`);
  a `406` means an unsupported `x-v` version.
- Follow the pagination and versioning conventions in `conventions/avenue-bank-conventions.yml`.
