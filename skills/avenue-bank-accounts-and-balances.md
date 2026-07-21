---
name: Read consented accounts and balances
description: For a consumer who has authorised sharing under the CDR ADR model, list their Avenue Bank accounts and retrieve balances (single, bulk, or for specific accounts).
api: openapi/avenue-bank-cds-banking-openapi.json
method: generated
generated: '2026-07-21'
operations:
  - listBankingAccounts
  - getBankingAccountDetail
  - getBankingBalance
  - listBankingBalancesBulk
  - listBankingBalancesSpecificAccounts
---

# Read consented accounts and balances

This flow is **consumer-authorised**: it is available only to an Accredited Data Recipient
(ADR) after the customer authorises data sharing under the CDR security profile
(OAuth2 / OIDC + FAPI + MTLS-bound tokens — see `authentication/avenue-bank-authentication.yml`).
Required scope: `bank:accounts.basic:read` (plus `bank:accounts.detail:read` for detail).

## Steps

1. **`listBankingAccounts`** (`GET /banking/accounts`) — list the consented accounts.
   Send `x-v` and the FAPI headers (`x-fapi-interaction-id`, `x-fapi-auth-date`). Paginate with `page`/`page-size`.
2. Optionally **`getBankingAccountDetail`** (`GET /banking/accounts/{accountId}`) for full detail
   (requires `bank:accounts.detail:read`).
3. Retrieve balances by whichever shape fits:
   - **`getBankingBalance`** (`GET /banking/accounts/{accountId}/balance`) — one account.
   - **`listBankingBalancesBulk`** (`GET /banking/accounts/balances`) — all consented accounts.
   - **`listBankingBalancesSpecificAccounts`** (`POST /banking/accounts/balances`) — pass an
     `accountIds` array in the body (this POST is a read; it changes no state).

## Rules

- Always send `x-fapi-interaction-id` and echo/log it for tracing (`conventions/`).
- Only request accounts within the consented set; out-of-scope ids return
  `urn:au-cds:error:cds-banking:Authorisation/InvalidBankingAccount` (see `errors/`).
- No idempotency key is needed — every operation here is a read.
