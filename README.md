# Vertafore (vertafore)

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
