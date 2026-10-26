# Mojang (mojang)

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
