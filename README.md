# Insurance Australia Group

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

Insurance Australia Group (IAG, ASX: IAG) is the largest general insurance company in Australia and New Zealand, headquartered in Sydney and operating a portfolio of underwriting brands rather than a single consumer-facing label. In Australia it trades as NRMA Insurance, CGU, WFI, Swann Insurance and the digital-native ROLLiN'; in New Zealand as State, AMI, NZI and Lumley. Its lines of business are property and casualty — home and contents, motor, commercial, rural and farm, compulsory third party and specialty — split across a Direct Insurance Australia arm and an Intermediated Insurance Australia arm that sells through brokers and authorised representatives. IAG has no public, self-serve API surface. Probing every conventional developer hostname on iag.com.au, cgu.com.au and nrma.com.au found no developer portal and no published reference documentation; docs.iag.com.au exists but immediately redirects to a Microsoft Entra ID sign-in and is an internal wall, not a portal. What the probes did confirm is a real Apigee API gateway fronting three brand virtual hosts — api.iag.com.au, api.cgu.com.au and api.nrma.com.au — each returning an Apigee ApplicationNotFound fault at the root, meaning proxies exist but none is discoverable or documented to the public. A second round of probing added a fourth brand virtual host, api.wfi.com.au, and a publicly resolvable non-production Apigee organisation at test-api.iag.com.au. IAG has also deployed MuleSoft's Anypoint API Experience Hub and is migrating roughly 600 APIs onto it, with a stated intent to make them agent aware — a substantial API estate that is entirely internal. Broker and partner integration in this market runs through human-facing trading portals — CGU's PolicyPlace quote-and-bind platform, the Ebix Sunrise Exchange and the Steadfast Client Trading Platform — not through an open API programme. IAG does run a HackerOne vulnerability disclosure programme, and published an RFC 9116 security.txt across seven brand domains until it was withdrawn in mid-2025. Australia has the legal machinery for open insurance and no live obligation: the Consumer Data Right that opened banking and energy was flagged for general insurance and then paused, so nothing compels IAG to publish. This record is therefore an honest stub: a partner-gated carrier with a private gateway and zero public specifications.

**Areas:** Insurance · Australia · New Zealand · Property and Casualty · General Insurance · Carrier · Underwriting · Claims

## Insurance Australia Group on APIs.io

Everything profiled for Insurance Australia Group is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/iag/](https://apis.io/providers/iag/)** — or go straight to one of the APIs or properties below.

### APIs (1)

- [Insurance Australia Group API Gateway (private)](https://apis.io/apis/iag/iag-api-gateway/) — IAG runs an Apigee gateway with brand virtual hosts api.iag.com.au, api.cgu.com.au, api.nrma.com.au and api.wfi.com.au (plus the non-production…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Iag Context](https://apis.io/jsonld/iag/iag-context/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Insurance Australia Group API Rules](https://apis.io/rules/iag/iag-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Iag Authentication](https://apis.io/security/iag/iag-authentication/)
- [Iag Domain Security](https://apis.io/security/iag/iag-domain-security/)
- [Iag Vulnerability Disclosure](https://apis.io/security/iag/iag-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Iag Plans Pricing](https://apis.io/plans/iag/iag-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Iag Rate Limits](https://apis.io/rate-limits/iag/iag-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.iag.com.au/)
- [Getting started](https://docs.hackerone.com/en/articles/8509950-response-program-setup)
- [Security](https://hackerone.com/iag)
- [GitHub](https://github.com/InsuranceAustraliaGroup)

## API Evangelist rating

**Kin Score 17.6** — emerging · rubric 0.24.0 · scored 2026-10-20

| Facet | Score |
|---|---|
| Discoverability | 74.1 |
| Contract quality | 14.7 |
| Contract governance | 22.0 |
| Operational transparency | 13.2 |
| Developer ergonomics | 11.9 |
| Access clarity | 0.0 |

**Agent readiness 2.5** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 14.9** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/iag/](https://apis.io/providers/iag/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Insurance Australia Group: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/iag/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
