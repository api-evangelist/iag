# Insurance Australia Group (iag)

Insurance Australia Group (ASX: IAG) is the largest general insurance company in Australia and New Zealand, headquartered in Sydney and operating a portfolio of underwriting brands rather than a single consumer-facing label. In Australia it trades as NRMA Insurance, CGU, WFI, Swann Insurance and the digital-native ROLLiN'; in New Zealand as State, AMI, NZI and Lumley. Its lines of business are property and casualty — home and contents, motor, commercial, rural and farm, compulsory third party and specialty — split across a Direct Insurance Australia arm and an Intermediated Insurance Australia arm that sells through brokers and authorised representatives.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/iag/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/iag/refs/heads/main/apis.yml)

## Tags

- Insurance
- Australia
- New Zealand
- Property and Casualty
- General Insurance
- Carrier
- Underwriting
- Claims
- Broker
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

**None.** IAG publishes no public, self-serve API.

This is a deliberate, verified finding rather than a gap in the research. Every conventional developer hostname and path was probed across `iag.com.au`, `cgu.com.au`, `nrma.com.au` and `iag.co.nz` on 2026-07-25:

- `developer.` / `developers.` / `developerportal.` / `gateway.` / `partners.` subdomains — **DNS does not resolve**
- `docs.iag.com.au` — **HTTP 200, but redirects straight to Microsoft Entra ID sign-in**. Internal corporate documentation behind SSO, not a developer portal.
- `api.iag.com.au`, `api.cgu.com.au`, `api.nrma.com.au` — **HTTP 404 with an Apigee fault**: `Unable to identify proxy for host: https_vhost / https_cgu_vhost / https_nrma_vhost`. A production Apigee API gateway is live behind all three brands, and not one proxy on it is publicly routed or documented.
- `www.iag.com.au/developers`, `/api`, `/developer`, `/partners`, `/integrations` — **HTTP 403 (Akamai bot mitigation)**; no such developer surface is referenced anywhere on the public site.
- No OpenAPI or Swagger document, no GraphQL endpoint, no `.proto`, no AsyncAPI, no webhook catalogue, no public Postman workspace.

## ACORD posture

**No ACORD reference found.** Nothing in IAG's public material mentions ACORD, ACORD XML, AL3, NGDS or ACORD certification. Australia does not run on the ACORD/IVANS agency-download stack used in North America — broker-to-carrier trading here moves over the **Ebix Sunrise Exchange** and the **Steadfast Client Trading Platform (SCTP)**, plus carrier-specific broker portals. CGU is connected to both, and has launched **PolicyPlace**, its own digital quote-and-bind front end for brokers, which IAG has said is additive to Sunrise and SCTP rather than a replacement. All three are human-facing platforms, not published APIs.

## Quote / bind / issue / FNOL

Quote and bind genuinely exist — for **brokers**, through PolicyPlace, Sunrise and SCTP. Issue is internal. FNOL is taken through brand web forms and call centres. **None of the four verbs is exposed as a public API.**

## Regulatory context

APRA supervises IAG prudentially and ASIC governs conduct, alongside the General Insurance Code of Practice. Australia has the legal machinery for open insurance and no live obligation: the **Consumer Data Right** that already opened banking and energy was flagged for extension to general insurance, then paused and de-prioritised. General insurance is **not** a designated CDR sector, so nothing compels IAG to publish product, policy or claims data through an API.

## Source code

- [github.com/InsuranceAustraliaGroup](https://github.com/InsuranceAustraliaGroup) — official IAG organisation (Sydney). One public repository: a fork of Google's AppAuth-iOS OAuth/OIDC SDK. No API definitions.
- [github.com/iagcl](https://github.com/iagcl) — "IAG Customer Labs". Four public repositories (`data_pipeline`, `watchmen`, `bakery`, `mark59`), all internal platform tooling and mostly unmaintained. No API definitions.

## Links

- **Website:** [https://www.iag.com.au/](https://www.iag.com.au/)
- **Newsroom:** [https://www.iag.com.au/newsroom](https://www.iag.com.au/newsroom)
- **CGU Partner Portal (login wall):** [https://www.cgu.com.au/eai/help](https://www.cgu.com.au/eai/help)
- **Supplier Portal:** [https://www.iag.com.au/supplier-portal](https://www.iag.com.au/supplier-portal)
- **LinkedIn:** [https://www.linkedin.com/company/iag](https://www.linkedin.com/company/iag)
- **GitHub:** [https://github.com/InsuranceAustraliaGroup](https://github.com/InsuranceAustraliaGroup)

See [`review.yml`](review.yml) for the full probe log with HTTP statuses.
