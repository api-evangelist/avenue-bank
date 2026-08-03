# Avenue Bank (avenue-bank)

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
