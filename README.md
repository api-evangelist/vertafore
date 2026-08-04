# Vertafore (vertafore)

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

Vertafore is an insurance technology provider whose software runs a large share of the North American property and casualty (P&C) distribution channel - agency management systems (**AMS360** and **Sagitta**), the **ImageRight** document and content management platform, and the **PL Rating** personal-lines comparative rater. Vertafore exposes developer APIs across these products through the Vertafore API Developer Portal ([developer.vertafore.com](https://developer.vertafore.com/)) and the Orange Partner Program.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vertafore/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vertafore/refs/heads/main/apis.yml)

## Access model (important)

Vertafore's developer APIs are **real but partner-gated**. Reaching the reference documentation, OpenAPI, and live endpoints requires:

- A **Vertafore Single Sign-On (VSSO)** account
- A **licensed Vertafore Developer Portal** contract
- **Per-API scopes** the agency has contracted for (a scope is an instance of an API your agency has contracted with Vertafore to use)
- Building in a **Sandbox** and promoting to **Live** only after Vertafore Customer Support approval

Third-party software vendors typically enter through the **Orange Partner Program**, which grants an integration toolkit for the relevant management system and access to a test instance.

Because the specifications live behind that login, the endpoints in `apis.yml` are marked `endpointsModeled: true` and are honestly modeled from public help pages and product documentation - they are **not** harvested from an open specification. No specific fabricated endpoint surface is claimed.

## Tags

- Insurance
- InsurTech
- Agency Management
- Property and Casualty
- AMS360
- Sagitta
- ImageRight
- Comparative Rating
- Partner Gated

## Timestamps

- **Created:** 2026-07-10
- **Modified:** 2026-07-10

## APIs

### Vertafore AMS360 EMS API

The newest and preferred REST API for AMS360, the flagship P&C agency management system. It exposes agency data as REST resources - Customers, Policies, Service Agreements, Invoices, Billing, Deposits, and Personnel - secured with OAuth Bearer tokens. Public tutorials show a sandbox host `api-sandbox.vertafore.com` and a Customers endpoint under `/authgrant/v1/api`.

- **Human URL:** [https://developer.vertafore.com/](https://developer.vertafore.com/)
- **Base URL:** `https://api.vertafore.com`
- **Endpoints modeled:** yes (portal-gated)

### Vertafore AMS360 WSAPI

The established SOAP web service for AMS360 (versions 2.4 and 3.0), exposed as `WSAPIService.svc` and authenticated with a per-agency username and password. Public references name operations such as `CustomerGet`, `PolicyGet`, and `SearchByPhoneNumber` under a `/v3/WSAPIService.svc` path.

- **Human URL:** [Web Service API Setup](https://help.vertafore.com/ams360/content/contextsensitive/download-integration/cswebserviceapisetup.htm)
- **Endpoints modeled:** yes (WSDL is partner-gated)

### Vertafore AMS360 OData API

An OData connection method for AMS360 used to automatically retrieve customer, policy, and accounting data for reporting and downstream integrations. Access requires an AMS360 OData subscription contracted through Vertafore.

- **Endpoints modeled:** yes (portal-gated)

### Vertafore ImageRight REST API

A REST API over ImageRight, Vertafore's document and content management platform for carriers and larger agencies - document ingestion and retrieval, files and folders, tasks, and workflow objects, authenticated with a token obtained from ImageRight credentials. A public ImageRight 6.8 REST API reference PDF documents the auth flow and resource model.

- **Human URL:** [https://developer.vertafore.com/](https://developer.vertafore.com/)
- **Endpoints modeled:** yes (deployment-specific base URLs)

### Vertafore PL Rating API

A rating and quoting API surface over PL Rating, Vertafore's personal-lines comparative rater connected to more than 300 carriers across 48 states and DC, including the newer in-rater bind capability. The portal refers to a Vertafore Rating API secured with API credential keys.

- **Human URL:** [PL Rating](https://www.vertafore.com/products/insurance-comparative-rater/pl-rating)
- **Endpoints modeled:** yes (contracts are partner-gated)

### Vertafore Sagitta API

Integration APIs over Sagitta, Vertafore's agency management system for larger and more complex commercial agencies and brokers. Documented integrations bridge Sagitta customer, contact, address, and policy data into other Vertafore products and certified Orange Partner solutions.

- **Human URL:** [AMS360 & Sagitta Integrations](https://help.vertafore.com/commercialsubmissions/content/howto/managementsystemintegration.htm)
- **Endpoints modeled:** yes (portal-gated)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/vertafore)
- [Website](https://www.vertafore.com)
- [Documentation](https://developer.vertafore.com/)
- [Orange Partner Program](https://www.vertafore.com/why-vertafore/orange-partner-program)
- [Plans](plans/vertafore-plans-pricing.yml)
- [Fin Ops](finops/vertafore-finops.yml)
- [Blog](https://www.vertafore.com/resources/blog)

## WebSocket review

Vertafore does **not** expose a documented public WebSocket API. Its developer surface is request/response (REST, SOAP, OData), and near-real-time delivery in AMS360 is handled by the Outbound Notification Service (a webhook that POSTs to a customer HTTP endpoint), not a WebSocket. See `review.yml`.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
