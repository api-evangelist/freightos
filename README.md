# Freightos (freightos)

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
