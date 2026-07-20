# Avenue Bank (avenue-bank)

Avenue Bank Ltd (ABN 24 628 073 085, AFSL 520239) is an Australian Authorised Deposit-taking Institution (ADI) regulated by APRA, holding a full (unrestricted) banking licence granted in 2024 after operating as a Restricted ADI from 2021. Founded by Dale Hurley and Colin Porter (co-founders of CreditorWatch) and majority-backed by Sherman Ma's Liberty Financial Group, Avenue is a digital business bank that is the first and only Australian bank specialising exclusively in bank guarantees for SMEs, alongside term deposits.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/avenue-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/avenue-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Data Right
- Consumer Banking
- Business Banking
- Bank Guarantees
- Australia
- ADI

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Avenue Bank CDR Product Reference Data API

UNVERIFIED. Under Australia's Consumer Data Right (CDR / Open Banking), every active ADI data holder must expose a public, unauthenticated Product Reference Data (PRD) API at the standard Consumer Data Standards (CDS) path `/cds-au/v1/banking/products`. Avenue Bank is an ADI, but as of 2026-07-20 it is not listed in the CDR Register's banking data-holder brands, and a probe of its API host returned HTTP 403 Forbidden (a WAF response, not a CDS-conformant JSON payload with a `data.products` array and `x-v` header). The base URL below is the standard CDS path on Avenue's real API host, recorded as unverified rather than a confirmed live endpoint.

- **Human URL:** [https://consumerdatastandardsaustralia.github.io/standards/#get-products](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- **Base URL:** `https://api.avenuebank.com.au/cds-au/v1/banking/products` (unverified — HTTP 403, not in CDR Register)

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://consumerdatastandardsaustralia.github.io/standards/#cdr-banking-api_get-products)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)

## Common Properties

- [Website](https://www.avenuebank.com.au/)
- [Blog](https://www.avenuebank.com.au/news/)
- [Support](https://www.avenuebank.com.au/help/)
- [Privacy Policy](https://www.avenuebank.com.au/privacy)
- [Terms of Service](https://www.avenuebank.com.au/legal/)
- [LinkedIn](https://au.linkedin.com/company/avenuebank)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
