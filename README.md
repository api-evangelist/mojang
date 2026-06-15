# Mojang (mojang)

Mojang Studios is the developer of Minecraft. The Mojang / Minecraft Services API surface covers Minecraft player identity (UUID and profile lookup), skins and capes, name history and name change, server session verification, blocked server lists, player attributes (privacy, chat, friends settings), friends graph, presence, public keys for profile signature verification, and account entitlements. Endpoints span three hosts: the legacy api.mojang.com, the session-server sessionserver.mojang.com (Yggdrasil), and the modern Microsoft-side api.minecraftservices.com. Most read endpoints are public and unauthenticated; player-account endpoints require a Bearer Minecraft access token obtained via the Xbox Live / XSTS authentication chain.

**APIs.json:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)

## Tags

- Games And Comics
- Minecraft
- Gaming
- Identity
- Player Profiles
- Session
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### Mojang Public API

Legacy public Mojang API (api.mojang.com) covering username-to-UUID lookup, batch UUID resolution, and historical profile endpoints. Most operations are being migrated to api.minecraftservices.com but remain live for backward compatibility.

- **Human URL:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)
- **Base URL:** `https://api.mojang.com`

#### Tags

- Identity
- Player Profiles
- Public

#### Properties

- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [OpenAPI](openapi/mojang-public-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mojang-public-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mojang-public-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mojang Session Server

Mojang's Yggdrasil session server (sessionserver.mojang.com) used during the Minecraft login handshake. Provides the canonical skin and cape texture lookup keyed by player UUID, the server-side hasJoined verification used by Minecraft servers, the join endpoint used by clients, and the blocked-servers SHA-1 hash list.

- **Human URL:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)
- **Base URL:** `https://sessionserver.mojang.com`

#### Tags

- Session
- Authentication
- Textures
- Server

#### Properties

- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [OpenAPI](openapi/mojang-session-server-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mojang-session-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mojang-session-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Minecraft Services API

Modern Microsoft-managed Minecraft Services API (api.minecraftservices.com) covering authenticated player profile management, name change, skin and cape management, player attributes (chat / friends / profanity filter), blocklist, friends graph, presence reporting, signature keypair issuance, public Mojang keys, and entitlement / ownership checks. Requires a Minecraft Bearer access token obtained via the Xbox Live authentication chain for player-scoped endpoints.

- **Human URL:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)
- **Base URL:** `https://api.minecraftservices.com`

#### Tags

- Identity
- Player Profiles
- Friends
- Presence
- Skins
- Capes
- Entitlements
- Authenticated

#### Properties

- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [OpenAPI](openapi/mojang-minecraft-services-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mojang-minecraft-services.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mojang-minecraft-services.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.minecraft.net)
- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [Documentation](https://minecraft.wiki/w/Microsoft_authentication)
- [GitHub Organization](https://github.com/Mojang)
- [GitHub Repository](https://github.com/Mojang/brigadier)
- [GitHub Repository](https://github.com/Mojang/DataFixerUpper)
- [GitHub Repository](https://github.com/Mojang/bedrock-protocol-docs)
- [GitHub Repository](https://github.com/Mojang/bedrock-samples)
- [GitHub Repository](https://github.com/Mojang/minecraft-creator-tools)
- [GitHub Repository](https://github.com/Mojang/minecraft-debugger)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [Rate Limits](rate-limits/mojang-rate-limits.yml)
- [Vocabulary](vocabulary/mojang-vocabulary.yaml)
- [Spectral Rules](rules/mojang-spectral-rules.yml)
- [JSON-LD](json-ld/mojang-api-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
