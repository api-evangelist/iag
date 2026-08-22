# Insurance Australia Group (iag)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
