# Recraft (recraft-ai)

Recraft is a London-based AI design platform — founded in 2023 by Anna Veronika Dorogush, the creator of the CatBoost ML framework — that builds production-grade image and vector generation models tailored for professional designers and brands. The Recraft external HTTP API exposes prompt-to-image, vector generation, image-to-image, inpainting, outpainting, vectorization, background tooling, upscaling, custom style creation, prompt enhancement, and account inspection with Bearer-token authentication and an OpenAI-compatible request shape, complemented by hosted and self-hosted Model Context Protocol servers for use from Claude and other agentic AI clients.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/recraft-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- AI, Artificial Intelligence, Image Generation, Generative AI, Vector Graphics, Brand Design, Design Tools, Foundation Models, MCP

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Models

| Model | Family | Release | Raster | Vector | Max Prompt | Notes |
|---|---|---|---|---|---|---|
| Recraft V4.1 | V4 | 2026-05 | Yes | Yes | 10,000 chars | Flagship; sharper and more polished than V4. |
| Recraft V4.1 Pro | V4 | 2026-05 | Yes | Yes | 10,000 chars | 2x resolution of V4.1. |
| Recraft V4.1 Utility / Utility Pro | V4 | 2026-05 | Yes | Yes | 10,000 chars | General-purpose variants. |
| Recraft V4 / V4 Pro | V4 | 2025 | Yes | Yes | 10,000 chars | Prior flagship. |
| Recraft V3 / V3 Vector | V3 | 2024 | Yes | Yes | 1,000 chars | Supports custom styles via `/styles`. |
| Recraft V2 / V2 Vector | V2 | 2024 | Yes | Yes | 1,000 chars | Lowest-cost tier. |

External models available inside Recraft Studio include Flux, Ideogram, GPT Image, HiDream, Imagen, Qwen Image, Seedream, Grok Image, and Nano Banana, with Grok Video, Veo, Kling, and Sora for video.

## APIs

### Recraft Images API

REST API for AI image and vector generation. Endpoints cover prompt-to-image (raster and vector), image-to-image, inpainting, outpainting, background removal/replace/generate, vectorization, crisp and creative upscaling, region erase, image variation, exploration, prompt enhancement, custom style creation, and account/credit inspection.

**Base URL:** `https://external.api.recraft.ai/v1`

**Authentication:** `Authorization: Bearer $RECRAFT_API_TOKEN`

**Human URL:** [https://www.recraft.ai/docs/api-reference/endpoints](https://www.recraft.ai/docs/api-reference/endpoints)

- [Documentation — Getting Started](https://www.recraft.ai/docs/api-reference/getting-started)
- [Documentation — Endpoints](https://www.recraft.ai/docs/api-reference/endpoints)
- [Documentation — Swagger UI](https://external.api.recraft.ai/doc/)
- [OpenAPI](openapi/recraft-images-api-openapi.yml)
- [JSON Schema — Image](json-schema/recraft-image-schema.json)
- [JSON Schema — Style](json-schema/recraft-style-schema.json)
- [JSON-LD](json-ld/recraft-ai-context.jsonld)
- [Naftiko Capability — Generation](capabilities/images-generation.yaml)
- [Naftiko Capability — Vector](capabilities/images-vector.yaml)
- [Naftiko Capability — Editing](capabilities/images-editing.yaml)
- [Naftiko Capability — Background](capabilities/images-background.yaml)
- [Naftiko Capability — Upscaling and Prompt Enhancement](capabilities/images-upscale-vectorize.yaml)
- [Naftiko Capability — Styles](capabilities/styles.yaml)
- [Naftiko Capability — Users](capabilities/users.yaml)

### Recraft MCP Server

Model Context Protocol server giving Claude, Cursor, and other MCP clients access to Recraft image and vector tooling. Available as a hosted remote MCP server (OAuth, subscription credits) and a self-hosted local Node.js server (API key, API units).

**Human URL:** [https://www.recraft.ai/docs/mcp-reference/getting-started](https://www.recraft.ai/docs/mcp-reference/getting-started)

- [Documentation — Remote MCP](https://www.recraft.ai/docs/mcp-reference/remote-server)
- [Documentation — Local MCP](https://www.recraft.ai/docs/mcp-reference/local-server)
- [Documentation — Tools](https://www.recraft.ai/docs/mcp-reference/tools)
- [SourceCode — recraft-ai/mcp-recraft-server](https://github.com/recraft-ai/mcp-recraft-server)

## Endpoints

All endpoints are `POST` to `https://external.api.recraft.ai/v1` unless noted.

| Endpoint | Purpose | Cost (V4.1 raster / vector) |
|---|---|---|
| `/images/generations` | Create image from prompt | 40 / 80 units |
| `/images/generations/raster` | Create raster only | 40 units |
| `/images/generations/vector` | Create vector only | 80 units |
| `/images/imageToImage` | Variation preserving composition | 40 / 80 units |
| `/images/inpaint` | Regenerate masked region | 40 / 80 units |
| `/images/outpaint` | Extend image beyond edges | 40 / 80 units |
| `/images/replaceBackground` | Replace background | 40 / 80 units |
| `/images/generateBackground` | Fill masked background | 40 / 80 units |
| `/images/vectorize` | Raster to SVG | 10 units |
| `/images/removeBackground` | Strip background | 10 units |
| `/images/crispUpscale` | Sharp upscale | 4 units |
| `/images/creativeUpscale` | Detail-adding upscale | 250 units |
| `/images/eraseRegion` | Object removal | 2 units |
| `/images/variateImage` | Visual remix | 40 units |
| `/images/explore` | Diverse variations | 40 units |
| `/images/explore/similar` | Source-resembling variations | 40 units |
| `/prompts/enhance` | Expand short prompt | 10 units |
| `/styles` | Create custom style (V3) | 40 units |
| `GET /users/me` | Current user and credit balance | free |

USD $1.00 = 1,000 API units. Pro models charge 250 (raster) / 300 (vector) units. Failed operations are not billed.

## Limits

- Per user: 5 requests per second
- Per user: 100 images per minute
- Generated assets retained ~24 hours behind signed URLs
- 14 supported aspect ratios (1:1, 2:1, 1:2, 3:2, 2:3, 4:3, 3:4, 5:4, 4:5, 6:10, 14:10, 10:14, 16:9, 9:16)
- Prompt length: 10,000 chars (V4/V4.1), 1,000 chars (V2/V3)

## Common Properties

- [Portal — recraft.ai](https://www.recraft.ai)
- [Documentation — docs](https://www.recraft.ai/docs)
- [GettingStarted — API](https://www.recraft.ai/docs/api-reference/getting-started)
- [Documentation — Endpoints](https://www.recraft.ai/docs/api-reference/endpoints)
- [Documentation — Swagger](https://external.api.recraft.ai/doc/)
- [Documentation — llms.txt](https://www.recraft.ai/docs/llms.txt)
- [Portal — Recraft API](https://www.recraft.ai/api)
- [Sandbox — Recraft Studio](https://www.recraft.ai/projects)
- [Pricing](https://www.recraft.ai/pricing)
- [Pricing — API](https://www.recraft.ai/docs/api-reference/pricing)
- [Plans — Paid](https://www.recraft.ai/docs/plans-and-billing/paid-plans)
- [Plans — Free](https://www.recraft.ai/docs/plans-and-billing/free-plan)
- [Blog](https://www.recraft.ai/blog)
- [Blog — Image Generation API](https://www.recraft.ai/blog/discover-the-power-of-recrafts-image-generation-api)
- [GitHubOrganization](https://github.com/recraft-ai)
- [SDK — MCP Recraft Server](https://github.com/recraft-ai/mcp-recraft-server)
- [Tool — ComfyUI Recraft Node](https://github.com/recraft-ai/ComfyUI-RecraftAI)
- [LinkedIn](https://www.linkedin.com/company/recraft-ai)
- [Forum — Discord](https://discord.gg/recraft)
- [Support — Feedback Portal](https://feedback.recraft.ai)
- [Support — FAQ](https://www.recraft.ai/docs/support-and-faq/FAQ)
- [Support — Contact](https://www.recraft.ai/docs/support-and-faq/contact-support)
- [TrustCenter — Security](https://www.recraft.ai/docs/trust-and-security/security)
- [TrustCenter — Compliance and Certifications](https://www.recraft.ai/docs/trust-and-security/compliance-and-certifications)
- [PrivacyPolicy — Data Protection](https://www.recraft.ai/docs/trust-and-security/data-protection-and-privacy)
- [Documentation — Data Use and Training](https://www.recraft.ai/docs/trust-and-security/data-use-and-model-training)
- [Documentation — Commercial Ownership](https://www.recraft.ai/docs/trust-and-security/ownership)
- [Documentation — Credits](https://www.recraft.ai/docs/plans-and-billing/credits)
- [Documentation — Billing](https://www.recraft.ai/docs/plans-and-billing/billing)
- [Documentation — API Appendix](https://www.recraft.ai/docs/api-reference/appendix)
- [Documentation — API Styles](https://www.recraft.ai/docs/api-reference/styles)
- [Models — Recraft V4.1](https://www.recraft.ai/docs/recraft-models/recraft-v4-1)
- [Models — Recraft V4](https://www.recraft.ai/docs/recraft-models/recraft-V4)
- [Models — Recraft V3](https://www.recraft.ai/docs/recraft-models/recraft-V3)
- [Models — Recraft V2](https://www.recraft.ai/docs/recraft-models/recraft-V2)
- [Documentation — Choosing a Model](https://www.recraft.ai/docs/recraft-models/choosing-a-model)
- [Documentation — External Models](https://www.recraft.ai/docs/recraft-models/external-models)
- [Documentation — Styles Overview](https://www.recraft.ai/docs/recraft-studio/styles/overview)
- [Documentation — Curated Styles](https://www.recraft.ai/docs/recraft-studio/styles/curated-styles)
- [Documentation — Prompting Best Practices](https://www.recraft.ai/docs/best-practices/prompting-and-image-generation)
- [Documentation — Character Consistency](https://www.recraft.ai/docs/best-practices/character-consistency)
- [Documentation — Prompt Engineering Guide](https://www.recraft.ai/docs/prompt-engineering-guide/introduction)
- [SignUp](https://www.recraft.ai/auth)
- [Documentation — API Token Management](https://www.recraft.ai/profile/api)
- [TermsOfService](https://www.recraft.ai/terms)
- [PrivacyPolicy](https://www.recraft.ai/privacy-policy)
- [Documentation — Subprocessors](https://www.recraft.ai/subprocessors)

## Artifacts

Machine-readable API specifications organised by format.

### OpenAPI

- [Recraft Images API](openapi/recraft-images-api-openapi.yml)

### JSON Schema

- [Recraft Image Schema](json-schema/recraft-image-schema.json)
- [Recraft Style Schema](json-schema/recraft-style-schema.json)

### JSON-LD

- [Recraft Context](json-ld/recraft-ai-context.jsonld)

### Examples

- [Create Image](examples/recraft-create-image-example.json)
- [Create Vector](examples/recraft-create-vector-example.json)
- [Create Custom Style](examples/recraft-create-style-example.json)
- [Get Current User](examples/recraft-get-current-user-example.json)

### Capabilities (Naftiko)

- [Generation](capabilities/images-generation.yaml)
- [Vector](capabilities/images-vector.yaml)
- [Editing](capabilities/images-editing.yaml)
- [Background](capabilities/images-background.yaml)
- [Upscaling and Prompt Enhancement](capabilities/images-upscale-vectorize.yaml)
- [Styles](capabilities/styles.yaml)
- [Users](capabilities/users.yaml)

### Vocabulary

- [Recraft Vocabulary](vocabulary/recraft-ai-vocabulary.yml)

### Commercial artifacts

- [Plans / Pricing](plans/recraft-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/recraft-ai-rate-limits.yml)
- [FinOps Definition](finops/recraft-ai-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
