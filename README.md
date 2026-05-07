# MobileAPI.dev (mobileapi-dev)

MobileAPI.dev is a commercial REST API that provides structured device specifications, product images, and metadata for over 31,500 smartphones, tablets, smartwatches, and laptops from more than 200 brands. The API exposes 12 normalized spec categories per device (Network, Body, Display, Platform, Memory, Main Camera, Selfie Camera, Sound, Comms, Features, Battery, Misc), fuzzy search, autocomplete, manufacturer indices, and a natural-language AI query endpoint, replacing in-house scraping of GSMArena-style sources for device-catalog, comparison, e-commerce, trade-in, repair, and insurance applications.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/mobileapi-dev/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Scope

- **Type:** Index

## Tags:

 - Data API, Developer Tools, Device Specifications, Mobile Data, Phone Specs, REST API, SaaS

## Timestamps

- **Created:** 2026-05-06
- **Modified:** 2026-05-06

## APIs

### MobileAPI

REST API providing device specifications, base64-encoded product images, and pricing metadata for 31,500+ smartphones, tablets, smartwatches, and laptops across 200+ manufacturers. Endpoints support paginated device listing, fuzzy search by name or model number, autocomplete, browsing by manufacturer/year/type, per-category specification retrieval (battery, display, platform, memory, cameras, network, sound, comms, features, body, misc), high-resolution images, manufacturer directory, account introspection (`/me/`), and an AI natural-language query endpoint that translates plain-English questions into structured device results.

**Human URL:** [https://mobileapi.dev/](https://mobileapi.dev/)

**Base URL:** [https://api.mobileapi.dev/](https://api.mobileapi.dev/)

#### Tags:

 - Autocomplete, Device Catalog, Device Specifications, Fuzzy Search, Manufacturers, Mobile Devices, Natural Language Query, Product Images, REST API, Smartphones, Smartwatches, Tablets

#### Properties

- [Documentation](https://mobileapi.dev/docs/)
- [APIReference](https://mobileapi.dev/docs/)
- [OpenAPI](openapi/mobileapi-openapi.yml)
- [GettingStarted](https://mobileapi.dev/docs/)
- [Authentication](https://mobileapi.dev/docs/)
- [RateLimits](https://mobileapi.dev/docs/)
- [CodeExamples](https://mobileapi.dev/docs/)
- [JSON-LD Context](json-ld/mobileapi-dev-context.jsonld)

#### JSON Schema

- [Device](json-schema/mobileapi-device-schema.json)
- [DeviceList](json-schema/mobileapi-devicelist-schema.json)
- [Manufacturer](json-schema/mobileapi-manufacturer-schema.json)
- [Image](json-schema/mobileapi-image-schema.json)
- [Battery](json-schema/mobileapi-battery-schema.json)
- [Body](json-schema/mobileapi-body-schema.json)
- [Display](json-schema/mobileapi-display-schema.json)
- [Platform](json-schema/mobileapi-platform-schema.json)
- [Memory](json-schema/mobileapi-memory-schema.json)
- [MainCamera](json-schema/mobileapi-maincamera-schema.json)
- [SelfieCamera](json-schema/mobileapi-selfiecamera-schema.json)
- [Network](json-schema/mobileapi-network-schema.json)
- [Sound](json-schema/mobileapi-sound-schema.json)
- [Comms](json-schema/mobileapi-comms-schema.json)
- [Features](json-schema/mobileapi-features-schema.json)
- [Misc](json-schema/mobileapi-misc-schema.json)

#### JSON Structure

- 16 structure docs in [`json-structure/`](json-structure/) covering Device, DeviceList, Manufacturer, Image, and the 12 spec sub-resources.

#### Examples

- [Device](examples/mobileapi-device-example.json)
- [DeviceList](examples/mobileapi-devicelist-example.json)
- [Manufacturer](examples/mobileapi-manufacturer-example.json)
- [Autocomplete](examples/mobileapi-autocomplete-example.json)
- [AI Query](examples/mobileapi-ai-query-example.json)

## Capabilities

Naftiko capability bundles for the API are in the [`capabilities/`](capabilities/) directory.

- **shared/mobileapi-capability.yaml** - Per-resource capability covering 28 production endpoints (devices, manufacturers, images, status, account).
- **device-lookup.yaml** - Workflow: autocomplete > search > device record > images > battery/display sub-resources for trade-in, repair, and insurance flows.
- **manufacturer-catalog.yaml** - Workflow: list manufacturers > select brand > devices-by-manufacturer/year/type for catalog and brand-page builds.
- **ai-device-recommendation.yaml** - Workflow: AI natural-language query > top-match enrichment with images and camera specs (Pro/Enterprise plans).

## Spectral Rules

[`rules/mobileapi-rules.yml`](rules/mobileapi-rules.yml) - 11 rules covering operation summary requirements, Title-Case enforcement, Django-style trailing-slash paths, operationId presence, 401/429 response coverage, HTTPS-only servers, and primary-auth-method documentation.

## Vocabulary

[`vocabulary/mobileapi-dev-vocabulary.yml`](vocabulary/mobileapi-dev-vocabulary.yml) - Controlled vocabulary across 7 dimensions (ResourceTypes, SpecCategories, OperationCategories, AuthenticationMethods, CommercialTiers, RateLimitDimensions, UseCaseDomains).

## Plans, Rate Limits, and FinOps

- [Plans (API Commons Plans 0.1)](plans/mobileapi-dev-plans-pricing.yml) - Free $0 (200 req/mo, 5 req/min), Pro $15/mo (10K req/mo, 10 req/sec, 15% annual), Enterprise custom (unlimited, up to 100 req/sec, 99.9% SLA).
- [Rate Limits (API Commons Rate Limits 0.1)](rate-limits/mobileapi-dev-rate-limits.yml) - Per-key short-window plus monthly quota; X-RateLimit-* response headers; HTTP 429 on exhaustion.
- [FinOps (FOCUS 1.3 aligned)](finops/mobileapi-dev-finops.yml) - Stripe-billed monthly subscription, single primary meter (api_requests), per-key cost allocation.

## Common Properties

- [Portal](https://mobileapi.dev/)
- [Documentation](https://mobileapi.dev/docs/)
- [Pricing](https://mobileapi.dev/#pricing)
- [SignUp](https://mobileapi.dev/signup/)
- [Login](https://mobileapi.dev/signin/)
- [Blog](https://mobileapi.dev/blog/)
- [Support](mailto:support@mobileapi.dev)
- [Status Page](https://mobileapi.cronitorstatus.com/)
- [GitHub Organization](https://github.com/MobileAPI-dev)
- [Code Examples (mobileapi-examples)](https://github.com/MobileAPI-dev/mobileapi-examples)
- [Terms of Service](https://app.getterms.io/view/AG2Np/terms-of-service/en-us)
- [Privacy Policy](https://app.getterms.io/view/AG2Np/privacy/en-us)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
