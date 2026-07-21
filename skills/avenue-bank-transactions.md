---
name: Retrieve consented account transactions
description: For a consumer who has authorised sharing, list transactions on an Avenue Bank account and fetch transaction detail under the CDR ADR model.
api: openapi/avenue-bank-cds-banking-openapi.json
method: generated
generated: '2026-07-21'
operations:
  - listBankingTransactions
  - getBankingTransactionDetail
---

# Retrieve consented account transactions

Consumer-authorised (CDR ADR model). Required scope: `bank:transactions:read`
(and `bank:accounts.basic:read` to resolve the account). See
`authentication/avenue-bank-authentication.yml`.

## Steps

1. **`listBankingTransactions`** (`GET /banking/accounts/{accountId}/transactions`).
   - Send `x-v` and FAPI headers.
   - Narrow with `oldest-time` / `newest-time`, `min-amount` / `max-amount`, or `text`.
   - Paginate with `page` / `page-size`; follow `links.next` until `meta.totalPages`.
2. For a specific transaction, **`getBankingTransactionDetail`**
   (`GET /banking/accounts/{accountId}/transactions/{transactionId}`).

## Rules

- Datetime filters are RFC 3339 / ISO 8601 UTC (`conventions/avenue-bank-conventions.yml`).
- A `404` with `urn:au-cds:error:cds-all:Resource/NotFound` means the transaction id is not on
  that account or is outside the consented window (`errors/avenue-bank-problem-types.yml`).
- Reads only — no idempotency key required.
