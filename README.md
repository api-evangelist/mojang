# Mojang (mojang)

Mojang Studios is the developer of Minecraft. The Mojang / Minecraft Services API surface covers Minecraft player identity (UUID and profile lookup), skins and capes, name history and name change, server session verification, blocked server lists, player attributes (privacy, chat, friends settings), friends graph, presence, public keys for profile signature verification, and account entitlements. Endpoints span three hosts: the legacy api.mojang.com, the session-server sessionserver.mojang.com (Yggdrasil), and the modern Microsoft-side api.minecraftservices.com. Most read endpoints are public and unauthenticated; player-account endpoints require a Bearer Minecraft access token obtained via the Xbox Live / XSTS authentication chain.

**URL:** [Visit APIs.json URL](https://minecraft.wiki/w/Mojang_API)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Games And Comics, Minecraft, Gaming, Identity, Player Profiles, Session, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### Mojang Public API
Legacy public Mojang API (api.mojang.com) covering username-to-UUID lookup, batch UUID resolution, and historical profile endpoints. Most operations are being migrated to api.minecraftservices.com but remain live for backward compatibility.

**Human URL:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)

#### Tags:

 - Identity, Player Profiles, Public

#### Properties

- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [OpenAPI](openapi/mojang-public-api-openapi.yml)
- [NaftikoCapability — Identity](capabilities/mojang-public-api-identity.yaml)
- [NaftikoCapability — Profile](capabilities/mojang-public-api-profile.yaml)

### Mojang Session Server
Mojang's Yggdrasil session server (sessionserver.mojang.com) used during the Minecraft login handshake. Provides the canonical skin and cape texture lookup keyed by player UUID, the server-side hasJoined verification used by Minecraft servers, the join endpoint used by clients, and the blocked-servers SHA-1 hash list.

**Human URL:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)

#### Tags:

 - Session, Authentication, Textures, Server

#### Properties

- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [OpenAPI](openapi/mojang-session-server-openapi.yml)
- [NaftikoCapability — Session](capabilities/mojang-session-server-session.yaml)
- [NaftikoCapability — Textures](capabilities/mojang-session-server-textures.yaml)
- [NaftikoCapability — Server](capabilities/mojang-session-server-server.yaml)

### Minecraft Services API
Modern Microsoft-managed Minecraft Services API (api.minecraftservices.com) covering authenticated player profile management, name change, skin and cape management, player attributes (chat / friends / profanity filter), blocklist, friends graph, presence reporting, signature keypair issuance, public Mojang keys, and entitlement / ownership checks. Requires a Minecraft Bearer access token obtained via the Xbox Live authentication chain for player-scoped endpoints.

**Human URL:** [https://minecraft.wiki/w/Mojang_API](https://minecraft.wiki/w/Mojang_API)

#### Tags:

 - Identity, Player Profiles, Friends, Presence, Skins, Capes, Entitlements, Authenticated

#### Properties

- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [OpenAPI](openapi/mojang-minecraft-services-openapi.yml)
- [NaftikoCapability — Authentication](capabilities/mojang-minecraft-services-authentication.yaml)
- [NaftikoCapability — Identity](capabilities/mojang-minecraft-services-identity.yaml)
- [NaftikoCapability — Profile](capabilities/mojang-minecraft-services-profile.yaml)
- [NaftikoCapability — Skins](capabilities/mojang-minecraft-services-skins.yaml)
- [NaftikoCapability — Capes](capabilities/mojang-minecraft-services-capes.yaml)
- [NaftikoCapability — Attributes](capabilities/mojang-minecraft-services-attributes.yaml)
- [NaftikoCapability — Blocklist](capabilities/mojang-minecraft-services-blocklist.yaml)
- [NaftikoCapability — Friends](capabilities/mojang-minecraft-services-friends.yaml)
- [NaftikoCapability — Presence](capabilities/mojang-minecraft-services-presence.yaml)
- [NaftikoCapability — Keys](capabilities/mojang-minecraft-services-keys.yaml)
- [NaftikoCapability — Entitlements](capabilities/mojang-minecraft-services-entitlements.yaml)

## Common Properties

- [Website](https://www.minecraft.net)
- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [Microsoft / Xbox Authentication Flow](https://minecraft.wiki/w/Microsoft_authentication)
- [GitHubOrganization](https://github.com/Mojang)
- [Brigadier Command Parser](https://github.com/Mojang/brigadier)
- [DataFixerUpper](https://github.com/Mojang/DataFixerUpper)
- [Bedrock Network Protocol Docs](https://github.com/Mojang/bedrock-protocol-docs)
- [Bedrock Edition Add-on Samples](https://github.com/Mojang/bedrock-samples)
- [Minecraft Creator Tools](https://github.com/Mojang/minecraft-creator-tools)
- [Minecraft VS Code Debugger](https://github.com/Mojang/minecraft-debugger)
- [PublicAPIsListing](https://github.com/public-apis/public-apis)
- [Rate Limits](rate-limits/mojang-rate-limits.yml)
- [Vocabulary](vocabulary/mojang-vocabulary.yaml)
- [Spectral Rules](rules/mojang-spectral-rules.yml)
- [JSON-LD Context](json-ld/mojang-api-context.jsonld)

## Features

| Name | Description |
|------|-------------|
| Public UUID Lookup | Look up a Minecraft player's UUID by username (case-insensitive) without authentication via /users/profiles/minecraft/{username}. |
| Batch UUID Resolution | Resolve up to ten usernames to UUIDs in a single POST call to /profiles/minecraft (legacy) or /minecraft/profile/lookup/bulk/byname (modern). |
| Skin and Cape Textures | Retrieve the Base64-encoded textures property for any player via sessionserver /session/minecraft/profile/{UUID}, optionally signed. |
| Server Session Verification | Yggdrasil hasJoined / join handshake used by every Minecraft server and client to validate that a logging-in player is authenticated. |
| Blocked Server List | SHA-1 hash list of servers Mojang has flagged, served as plain text from sessionserver.mojang.com/blockedservers. |
| Authenticated Player Profile | Fetch the signed-in player's own profile including all owned skins and capes via /minecraft/profile with Bearer auth. |
| Skin and Cape Management | Change, upload, reset, hide, and show skins and capes for the authenticated player via /minecraft/profile/skins and /capes/active. |
| Name Change | Check name availability, query cooldown / change history, and rename the authenticated player via /minecraft/profile/name endpoints. |
| Friends and Presence | Manage the player's friends graph, accept and reject requests, and publish presence (offline / online / playing) for friends. |
| Player Attributes and Blocklist | Read and modify the player's profanity filter, friends preferences, and chat settings, and read the player blocklist. |
| Signature Keypair and Public Keys | Issue per-player RSA signing keypairs and serve Mojang's rotating public keys for chat signature verification. |

## Use Cases

| Name | Description |
|------|-------------|
| Minecraft Server Authentication | Minecraft Java Edition servers call sessionserver.hasJoined during the login handshake to validate a player's session against Mojang. |
| Player Skin Display | Third-party sites and tools (NameMC, MinecraftSkinStealer, server lobby plugins) read the textures property from sessionserver to render player skins and capes. |
| Username History Tools | Username history dashboards once relied on /user/profiles/{uuid}/names; since deprecation tools now snapshot lookups from the public name-to-UUID endpoint over time. |
| Launcher Authentication | The Microsoft / Xbox Live -> XSTS -> Minecraft access-token flow backs the official Minecraft launcher and every third-party launcher. |
| Blocked Server Enforcement | Client-side enforcement of Mojang's EULA blocklist by hashing the server address and checking it against /blockedservers. |
| Community Skin Galleries | Skin upload sites use the authenticated skin endpoints to push player-selected skins to a signed-in Minecraft account. |

## Integrations

| Name | Description |
|------|-------------|
| Xbox Live | Mandatory upstream identity provider for Microsoft-era Minecraft accounts; supplies the XSTS token that is exchanged for a Minecraft access token. |
| Microsoft Identity Platform | OAuth 2.0 device-code and authorization-code flows against login.microsoftonline.com originate the access token used in the Xbox Live chain. |
| Minecraft Java Edition Servers | Every Java Edition server speaks the session-server protocol to verify joining clients. |
| Minecraft Realms | Mojang's hosted Realms service consumes the same identity, friends, and presence surface for invites and join flows. |

## Solutions

| Name | Description |
|------|-------------|
| Minecraft Account Identity | Resolve, verify, and manage Minecraft player identities across the legacy Mojang and modern Minecraft Services APIs from a single surface. |
| Minecraft Server Session Trust | Use the Yggdrasil session-verification surface plus the blocked-servers list to validate clients and enforce Mojang's server policy. |
| Player Personalization at Scale | Programmatic skin, cape, profanity, and friends management for hosted Minecraft platforms and community tools. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Mojang Public API](openapi/mojang-public-api-openapi.yml) — 4 paths, 4 operations, 5 schemas
- [Mojang Session Server](openapi/mojang-session-server-openapi.yml) — 4 paths, 4 operations, 4 schemas
- [Minecraft Services API](openapi/mojang-minecraft-services-openapi.yml) — 18 paths, 21 operations, 28 schemas

### JSON Schema

34 JSON Schema files extracted from the OpenAPI components across the three Mojang surfaces. See `json-schema/`.

### JSON Structure

34 JSON Structure files generated from the JSON Schemas. See `json-structure/`.

### JSON-LD

- [Mojang Umbrella Context](json-ld/mojang-api-context.jsonld)
- [Mojang Public API Context](json-ld/mojang-public-api-context.jsonld)
- [Mojang Session Server Context](json-ld/mojang-session-server-context.jsonld)
- [Minecraft Services API Context](json-ld/mojang-minecraft-services-context.jsonld)

### Examples

34 example JSON payloads, one per JSON Schema. See `examples/`.

## Capabilities

Naftiko capabilities are emitted one-per-tag with both REST and MCP exposers inlined.

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Mojang Public API — Identity](capabilities/mojang-public-api-identity.yaml) | Mojang Public API | 2 | DeveloperTooling / ServerOperator |
| [Mojang Public API — Profile](capabilities/mojang-public-api-profile.yaml) | Mojang Public API | 2 | DeveloperTooling / Researcher |
| [Mojang Session Server — Session](capabilities/mojang-session-server-session.yaml) | Mojang Session Server | 2 | ServerOperator / LauncherDeveloper |
| [Mojang Session Server — Textures](capabilities/mojang-session-server-textures.yaml) | Mojang Session Server | 1 | SkinGalleryOperator / DeveloperTooling |
| [Mojang Session Server — Server](capabilities/mojang-session-server-server.yaml) | Mojang Session Server | 1 | ServerOperator |
| [Minecraft Services — Authentication](capabilities/mojang-minecraft-services-authentication.yaml) | Minecraft Services API | 1 | LauncherDeveloper |
| [Minecraft Services — Identity](capabilities/mojang-minecraft-services-identity.yaml) | Minecraft Services API | 3 | DeveloperTooling / LauncherDeveloper |
| [Minecraft Services — Profile](capabilities/mojang-minecraft-services-profile.yaml) | Minecraft Services API | 4 | Player / LauncherDeveloper |
| [Minecraft Services — Skins](capabilities/mojang-minecraft-services-skins.yaml) | Minecraft Services API | 2 | Player / SkinGalleryOperator |
| [Minecraft Services — Capes](capabilities/mojang-minecraft-services-capes.yaml) | Minecraft Services API | 2 | Player |
| [Minecraft Services — Attributes](capabilities/mojang-minecraft-services-attributes.yaml) | Minecraft Services API | 2 | Player |
| [Minecraft Services — Blocklist](capabilities/mojang-minecraft-services-blocklist.yaml) | Minecraft Services API | 1 | Player |
| [Minecraft Services — Friends](capabilities/mojang-minecraft-services-friends.yaml) | Minecraft Services API | 2 | Player |
| [Minecraft Services — Presence](capabilities/mojang-minecraft-services-presence.yaml) | Minecraft Services API | 1 | Player |
| [Minecraft Services — Keys](capabilities/mojang-minecraft-services-keys.yaml) | Minecraft Services API | 2 | LauncherDeveloper / ServerOperator |
| [Minecraft Services — Entitlements](capabilities/mojang-minecraft-services-entitlements.yaml) | Minecraft Services API | 1 | LauncherDeveloper / Player |

## Vocabulary

- [Mojang Vocabulary](vocabulary/mojang-vocabulary.yaml) — Unified taxonomy mapping 14 resources, 19 actions, 16 workflows, and 6 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [Mojang Spectral Rules](rules/mojang-spectral-rules.yml) — 40 rules across 12 categories enforcing the Mojang conventions (path casing, operationId verbs, Title Case summaries, Bearer auth, Microcks compatibility, deprecation handling).

## Rate Limits

- [Mojang Rate Limits](rate-limits/mojang-rate-limits.yml) — Per-IP and per-account budgets covering the legacy Mojang API, session server, and Minecraft Services API. Documents the 200-req/2-min IP budget, ~400-req/10-s session-server budget, name-availability and server-join per-account caps, and the January 2025 experimental tightening.

## Notes

- The legacy `/user/profiles/{uuid}/names` name-history endpoint is documented for archival purposes but is permanently disabled (HTTP 410) since 13 September 2022.
- Mojang Studios has no first-party MCP server or Claude Code skill at the time of profiling. The GitHub org (https://github.com/Mojang) publishes engine libraries (Brigadier, DataFixerUpper), Bedrock samples, and tooling — none of them are MCP servers.
- No paid pricing surface (the public API is free), so `plans/` and `finops/` are intentionally omitted per the pipeline guidance.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
