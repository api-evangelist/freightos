# Freightos (freightos)

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

Freightos (NASDAQ CRGO) operates a global freight booking marketplace and, through WebCargo by Freightos, a rate-management and eBooking platform used by freight forwarders and carriers to price and book air, ocean, and trucking shipments in real time across 55+ carriers. Freightos publishes a developer portal (`developers.freightos.com`, with a legacy portal at `developer.freightos.com`) exposing freight-rate estimation, HS-code duties classification, and CO2 emissions APIs, plus the public Shipping Calculator on the marketplace at `https://ship.freightos.com/api/shippingCalculator`.

**Access model (be honest about it):** Freightos's API surface is mixed. The public Shipping Calculator returns marketplace price-range data with no API key (subject to Freightos attribution terms); a private Custom Site API key unlocks a subscriber's own rates. The developer-portal Estimator, Duties, and CO2 APIs are documented as **beta / provided as-is** and are provisioned to registered developers/partners. The WebCargo **booking (eBooking)** and **shipment/tracking** capabilities are **partner-gated** under commercial agreements (forwarders, carriers, and TMS/ERP/RTTV partners) rather than open self-service. Where the full endpoint surface is not publicly documented, this entry marks endpoints as **modeled** rather than fabricating a complete API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/freightos/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/freightos/refs/heads/main/apis.yml)

## Tags

- Freight
- Logistics
- Shipping
- Freight Marketplace
- Air Cargo
- Ocean Freight
- Rates
- Booking

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Freightos Shipping Calculator API

Public marketplace quote endpoint returning freight price ranges (min/max), transit-time ranges, and shipping mode (air, LCL, FCL, trucking) for a given origin, destination, weight, and load type. Supports GET with URL parameters or POST for richer requests, and JSON or XML responses. Public marketplace rates require no key (subject to attribution terms); private Custom Site rates use an API key parameter. Documented as beta / provided as-is.

- **Human URL:** [https://ship.freightos.com/api/shippingCalculator](https://ship.freightos.com/api/shippingCalculator)
- **Base URL:** `https://ship.freightos.com/api`

### Freightos Freight Rate Estimator API

Developer-portal JSON API that returns instant freight estimates for air, ocean, and trucking across core global import/export lanes, drawn from Freightos Marketplace live rates and a large historical rate database. The documented route is a POST that accepts origin, destination, and load definition and returns estimated cost and transit-time ranges per leg. Endpoints modeled from portal docs; access is provisioned per developer/partner.

- **Human URL:** [https://developers.freightos.com/docs/freightos---freight-estimator/1/overview](https://developers.freightos.com/docs/freightos---freight-estimator/1/overview)

### Freightos Duties API

HS-code classification API that takes a free-text commodity description and returns a ranked list of matching Harmonized System (HS) codes with match probabilities and descriptions, supporting duty estimation for US and international import/export. Documented on the developer portal as a beta API; endpoints modeled.

- **Human URL:** [https://developers.freightos.com/apis](https://developers.freightos.com/apis)

### Freightos CO2 Calculation API

Emissions API returning EU-standard CO2 estimates across air, ocean, and trucking modes for a shipment leg or route, for carbon reporting and greener routing decisions. Documented on the developer portal as a beta utility API; endpoints modeled.

- **Human URL:** [https://developers.freightos.com/docs/internalutility/1/overview](https://developers.freightos.com/docs/internalutility/1/overview)

### WebCargo Booking API

Partner-gated booking surface behind WebCargo by Freightos, giving freight forwarders and carriers live, bookable air/ocean capacity and real-time eBooking across 55+ carriers (Lufthansa, Air France KLM, IAG Cargo, United, and others), plus booking status updates. Exposed to forwarder, carrier, and TMS/ERP partners under commercial agreements rather than open self-service. Endpoints modeled — not publicly documented in full.

- **Human URL:** [https://www.webcargo.co/](https://www.webcargo.co/)

### Freightos Shipment Management and Tracking API

Partner-gated shipment lifecycle surface for managing shipments across providers — documentation management, messaging, milestone tracking, and shipment status updates — typically integrated into a forwarder or shipper TMS/ERP. Endpoints modeled — provisioned per partner and not publicly documented in full.

- **Human URL:** [https://developer.freightos.com/getting-started-freightos-integrations](https://developer.freightos.com/getting-started-freightos-integrations)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/freightos)
- [Website](https://www.freightos.com/)
- [Documentation](https://developers.freightos.com/apis)
- [GitHub Organization](https://github.com/Freightos)
- [Plans](plans/freightos-plans-pricing.yml)
- [Rate Limits](rate-limits/freightos-rate-limits.yml)
- [Fin Ops](finops/freightos-finops.yml)
- [Blog](https://www.freightos.com/blog/)

## Review

A WebSocket review is recorded in [review.yml](review.yml): Freightos does **not** expose a documented public WebSocket API. Its public and developer-portal APIs are request/response HTTP (JSON, plus XML on the Shipping Calculator), and booking/tracking are partner-gated HTTP integrations into TMS/ERP systems — no `ws://`/`wss://` endpoint is documented.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
