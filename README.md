# Recraft (recraft-ai)

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
