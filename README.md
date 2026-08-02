# Artisight

Artisight is a smart hospital platform company founded in 2015 out of Northwestern Medicine. It pairs NVIDIA GPU-powered edge sensors — dual 4K cameras, multi-microphone arrays and RTLS radios — with computer vision, speech recognition and deep learning to deliver virtual nursing, ambient clinical documentation, operating-room coordination, patient-safety monitoring, asset and staff tracking, environmental monitoring and predictive analytics across 400+ hospitals in 30+ US health systems.

- Website: https://artisight.com/
- Platform: https://artisight.com/smart-hospital-technology/
- Partners (Epic, Oracle Cerner and others): https://artisight.com/partners/
- Blog: https://artisight.com/blog/
- Press: https://artisight.com/press-releases/

## API posture

Artisight publishes **no public developer program, product API, SDK or OpenAPI**. EHR integration is delivered as a native, bi-directional Epic / Oracle Cerner interface ("zero API fees"), not a developer-facing API. `docs.`, `developer.`, `api.`, `app.`, `status.` and `trust.` artisight.com do not resolve in DNS.

What Artisight *does* publish, all on the corporate WordPress site and captured here:

| Surface | Location | Notes |
|---|---|---|
| WordPress REST API | `https://artisight.com/wp-json/` | 523 routes, 28 namespaces; anonymous reads |
| MCP server | `https://artisight.com/wp-json/mcp/mcp-oauth-server` | Live, but `initialize`/`tools/list` are 401 auth-gated |
| OAuth 2.0 AS metadata (RFC 8414) | `/.well-known/oauth-authorization-server` | authorization_code + refresh_token, PKCE S256, scope `mcp` |
| OAuth 2.0 protected-resource metadata (RFC 9728) | `/.well-known/oauth-protected-resource` | |
| llms.txt | `/llms.txt` | Rank Math SEO sitemap index |

No `security.txt`, no A2A agent card, no status page, no changelog, no published SDKs or Postman collection.

Compliance is published on the product page: HIPAA Expert Determination Certification, an AICPA SOC seal, AES-256 at rest / TLS 1.3 in transit, audit logging and RBAC, and on-premise video processing.
