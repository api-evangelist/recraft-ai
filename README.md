# Recraft (recraft-ai)

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

Recraft is a London-based AI design platform — founded in 2023 by Anna Veronika Dorogush (creator of the CatBoost ML framework) — that builds production-grade image and vector generation models tailored for professional designers and brands. Its Recraft V4.1, V4, V3, and V2 models generate photorealistic raster images, true SVG vector graphics, logos, icons, and seamless patterns with strong control over style, custom brand styles, color palettes, and text placement. The Recraft API exposes prompt-to-image, vector generation, image-to-image, inpainting, outpainting, vectorization, background tooling, upscaling, custom style creation, prompt enhancement, and account inspection over HTTPS with Bearer token authentication and an OpenAI-compatible request shape, complemented by hosted and self-hosted Model Context Protocol servers for use from Claude and other agentic AI clients.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/recraft-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/recraft-ai/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Image Generation
- Generative AI
- Vector Graphics
- Brand Design
- Design Tools
- Foundation Models
- MCP

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Recraft Images API

REST API for AI image and vector generation. Endpoints cover prompt-to-image (raster and vector), image-to-image, inpainting, outpainting, background removal/replace/generate, vectorization, crisp and creative upscaling, region erase, image variation, exploration, prompt enhancement, custom style creation, and account/credit inspection. Authenticated with a Bearer API token from the Recraft profile; metered in API units ($1 = 1,000 units) and rate-limited at 100 images/min and 5 requests/sec per user.

- **Human URL:** [https://www.recraft.ai/docs/api-reference/endpoints](https://www.recraft.ai/docs/api-reference/endpoints)
- **Base URL:** `https://external.api.recraft.ai/v1`

#### Tags

- AI
- Artificial Intelligence
- Image Generation
- Vector Graphics
- Generative AI
- Brand Design

#### Properties

- [Documentation](https://www.recraft.ai/docs/api-reference/getting-started)
- [Documentation](https://www.recraft.ai/docs/api-reference/endpoints)
- [Documentation](https://external.api.recraft.ai/doc/)
- [OpenAPI](openapi/recraft-images-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/recraft-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/recraft-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/recraft-image-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/recraft-style-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/recraft-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Recraft MCP Server

Model Context Protocol server giving Claude, Cursor, and other MCP clients access to Recraft's image and vector generation, editing, custom styles, vectorization, background tooling, and raster upscaling. Available as a hosted remote MCP server (OAuth-backed, billed against subscription credits) and a self-hosted local Node.js server (API key, billed against API units).

- **Human URL:** [https://www.recraft.ai/docs/mcp-reference/getting-started](https://www.recraft.ai/docs/mcp-reference/getting-started)
- **Base URL:** `https://mcp.recraft.ai/mcp`

#### Tags

- AI
- Artificial Intelligence
- MCP
- Model Context Protocol
- Image Generation

#### Properties

- [Documentation](https://www.recraft.ai/docs/mcp-reference/getting-started)
- [Documentation](https://www.recraft.ai/docs/mcp-reference/remote-server)
- [Documentation](https://www.recraft.ai/docs/mcp-reference/local-server)
- [Documentation](https://www.recraft.ai/docs/mcp-reference/tools)
- [Source Code](https://github.com/recraft-ai/mcp-recraft-server)
- [Postman Collection](collections/recraft-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/recraft-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.recraft.ai)
- [Documentation](https://www.recraft.ai/docs)
- [Getting Started](https://www.recraft.ai/docs/api-reference/getting-started)
- [Documentation](https://www.recraft.ai/docs/api-reference/endpoints)
- [Documentation](https://external.api.recraft.ai/doc/)
- [Documentation](https://www.recraft.ai/docs/llms.txt)
- [Portal](https://www.recraft.ai/api)
- [Sandbox](https://www.recraft.ai/projects)
- [Pricing](https://www.recraft.ai/pricing)
- [Blog](https://www.recraft.ai/blog/discover-the-power-of-recrafts-image-generation-api)
- [Blog](https://www.recraft.ai/blog)
- [GitHub Organization](https://github.com/recraft-ai)
- [SDK](https://github.com/recraft-ai/mcp-recraft-server)
- [Tool](https://github.com/recraft-ai/ComfyUI-RecraftAI)
- [LinkedIn](https://www.linkedin.com/company/recraft-ai)
- [Forum](https://discord.gg/recraft)
- [Support](https://feedback.recraft.ai)
- [Support](https://www.recraft.ai/docs/support-and-faq/FAQ)
- [Support](https://www.recraft.ai/docs/support-and-faq/contact-support)
- [Trust Center](https://www.recraft.ai/docs/trust-and-security/security)
- [Trust Center](https://www.recraft.ai/docs/trust-and-security/compliance-and-certifications)
- [Privacy Policy](https://www.recraft.ai/docs/trust-and-security/data-protection-and-privacy)
- [Documentation](https://www.recraft.ai/docs/trust-and-security/data-use-and-model-training)
- [Documentation](https://www.recraft.ai/docs/trust-and-security/ownership)
- [Documentation](https://www.recraft.ai/docs/plans-and-billing/credits)
- [Plans](https://www.recraft.ai/docs/plans-and-billing/paid-plans)
- [Plans](https://www.recraft.ai/docs/plans-and-billing/free-plan)
- [Documentation](https://www.recraft.ai/docs/plans-and-billing/billing)
- [Pricing](https://www.recraft.ai/docs/api-reference/pricing)
- [Documentation](https://www.recraft.ai/docs/api-reference/appendix)
- [Documentation](https://www.recraft.ai/docs/api-reference/styles)
- [Models](https://www.recraft.ai/docs/recraft-models/recraft-v4-1)
- [Models](https://www.recraft.ai/docs/recraft-models/recraft-V4)
- [Models](https://www.recraft.ai/docs/recraft-models/recraft-V3)
- [Models](https://www.recraft.ai/docs/recraft-models/recraft-V2)
- [Documentation](https://www.recraft.ai/docs/recraft-models/choosing-a-model)
- [Documentation](https://www.recraft.ai/docs/recraft-models/external-models)
- [Documentation](https://www.recraft.ai/docs/recraft-studio/styles/overview)
- [Documentation](https://www.recraft.ai/docs/recraft-studio/styles/curated-styles)
- [Documentation](https://www.recraft.ai/docs/best-practices/prompting-and-image-generation)
- [Documentation](https://www.recraft.ai/docs/best-practices/character-consistency)
- [Documentation](https://www.recraft.ai/docs/prompt-engineering-guide/introduction)
- [Sign Up](https://www.recraft.ai/auth)
- [Documentation](https://www.recraft.ai/profile/api)
- [Terms of Service](https://www.recraft.ai/terms)
- [Privacy Policy](https://www.recraft.ai/privacy-policy)
- [Documentation](https://www.recraft.ai/subprocessors)
- [Plans](plans/recraft-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/recraft-ai-rate-limits.yml)
- [Fin Ops](finops/recraft-ai-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
