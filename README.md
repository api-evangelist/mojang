# Mojang

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

**Areas:** Minecraft · Gaming · Identity · Player Profiles · Sessions · Public APIs · Video Games

## Mojang on APIs.io

Everything profiled for Mojang is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/mojang/](https://apis.io/providers/mojang/)** — or go straight to one of the APIs or properties below.

### APIs (14)

- [Mojang Attributes API](https://apis.io/apis/mojang/mojang-attributes-api/) — Profanity filter, friends, chat preferences
- [Mojang Authentication API](https://apis.io/apis/mojang/mojang-authentication-api/) — Exchange Xbox Live tokens for Minecraft access tokens
- [Mojang Blocklist API](https://apis.io/apis/mojang/mojang-blocklist-api/) — Player privacy blocklist
- [Mojang Capes API](https://apis.io/apis/mojang/mojang-capes-api/) — Cape selection and visibility
- [Mojang Entitlements API](https://apis.io/apis/mojang/mojang-entitlements-api/) — Account ownership and entitlement checks
- [Mojang Friends API](https://apis.io/apis/mojang/mojang-friends-api/) — Friends graph (list, add, remove)
- [Mojang Identity API](https://apis.io/apis/mojang/mojang-identity-api/) — Player UUID and username lookup
- [Mojang Keys API](https://apis.io/apis/mojang/mojang-keys-api/) — Signature keypairs and Mojang public keys
- [Mojang Presence API](https://apis.io/apis/mojang/mojang-presence-api/) — Online / playing presence reporting
- [Mojang Profile API](https://apis.io/apis/mojang/mojang-profile-api/) — Authenticated profile and name management
- [Mojang Server API](https://apis.io/apis/mojang/mojang-server-api/) — Server-policy artifacts (blocked servers)
- [Mojang Session API](https://apis.io/apis/mojang/mojang-session-api/) — Login-handshake session verification
- [Mojang Skins API](https://apis.io/apis/mojang/mojang-skins-api/) — Skin selection, upload, and reset
- [Mojang Textures API](https://apis.io/apis/mojang/mojang-textures-api/) — Player skin and cape texture lookup

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Mojang Agentic Access](https://apis.io/agentic-access/mojang/mojang-agentic-access/)

#### JSON Schema (34)

The data models the API reads and writes.

- [AuthenticatedProfile](https://apis.io/schemas/mojang/minecraft-services-authenticated-profile/)
- [BanStatus](https://apis.io/schemas/mojang/minecraft-services-ban-status/)
- [Blocklist](https://apis.io/schemas/mojang/minecraft-services-blocklist/)
- [Cape](https://apis.io/schemas/mojang/minecraft-services-cape/)
- [CapeSelection](https://apis.io/schemas/mojang/minecraft-services-cape-selection/)
- [ChangeSkinRequest](https://apis.io/schemas/mojang/minecraft-services-change-skin-request/)
- [EntitlementItem](https://apis.io/schemas/mojang/minecraft-services-entitlement-item/)
- [Entitlements](https://apis.io/schemas/mojang/minecraft-services-entitlements/)
- [Friend](https://apis.io/schemas/mojang/minecraft-services-friend/)
- [FriendUpdateRequest](https://apis.io/schemas/mojang/minecraft-services-friend-update-request/)
- [FriendsList](https://apis.io/schemas/mojang/minecraft-services-friends-list/)
- [FriendsPreferences](https://apis.io/schemas/mojang/minecraft-services-friends-preferences/)
- [MinecraftAccessToken](https://apis.io/schemas/mojang/minecraft-services-minecraft-access-token/)
- [NameAvailability](https://apis.io/schemas/mojang/minecraft-services-name-availability/)
- [NameChangeInfo](https://apis.io/schemas/mojang/minecraft-services-name-change-info/)
- [PlayerAttributes](https://apis.io/schemas/mojang/minecraft-services-player-attributes/)
- [PlayerAttributesUpdate](https://apis.io/schemas/mojang/minecraft-services-player-attributes-update/)
- [PlayerCertificates](https://apis.io/schemas/mojang/minecraft-services-player-certificates/)
- [PresenceEntry](https://apis.io/schemas/mojang/minecraft-services-presence-entry/)
- [PresenceReport](https://apis.io/schemas/mojang/minecraft-services-presence-report/)
- [PrivilegeMap](https://apis.io/schemas/mojang/minecraft-services-privilege-map/)
- [ProfanityFilterPreferences](https://apis.io/schemas/mojang/minecraft-services-profanity-filter-preferences/)
- [Profile](https://apis.io/schemas/mojang/minecraft-services-profile/)
- [PublicKeyEntry](https://apis.io/schemas/mojang/minecraft-services-public-key-entry/)
- [PublicKeys](https://apis.io/schemas/mojang/minecraft-services-public-keys/)
- …and 9 more published on APIs.io

#### JSON Structure (34)

Data models expressed in JSON Structure.

- [Minecraft Services Authenticated Profile Structure](https://apis.io/json-structure/mojang/minecraft-services-authenticated-profile-structure/)
- [Minecraft Services Ban Status Structure](https://apis.io/json-structure/mojang/minecraft-services-ban-status-structure/)
- [Minecraft Services Blocklist Structure](https://apis.io/json-structure/mojang/minecraft-services-blocklist-structure/)
- [Minecraft Services Cape Selection Structure](https://apis.io/json-structure/mojang/minecraft-services-cape-selection-structure/)
- [Minecraft Services Cape Structure](https://apis.io/json-structure/mojang/minecraft-services-cape-structure/)
- [Minecraft Services Change Skin Request Structure](https://apis.io/json-structure/mojang/minecraft-services-change-skin-request-structure/)
- [Minecraft Services Entitlement Item Structure](https://apis.io/json-structure/mojang/minecraft-services-entitlement-item-structure/)
- [Minecraft Services Entitlements Structure](https://apis.io/json-structure/mojang/minecraft-services-entitlements-structure/)
- [Minecraft Services Friend Structure](https://apis.io/json-structure/mojang/minecraft-services-friend-structure/)
- [Minecraft Services Friend Update Request Structure](https://apis.io/json-structure/mojang/minecraft-services-friend-update-request-structure/)
- [Minecraft Services Friends List Structure](https://apis.io/json-structure/mojang/minecraft-services-friends-list-structure/)
- [Minecraft Services Friends Preferences Structure](https://apis.io/json-structure/mojang/minecraft-services-friends-preferences-structure/)
- [Minecraft Services Minecraft Access Token Structure](https://apis.io/json-structure/mojang/minecraft-services-minecraft-access-token-structure/)
- [Minecraft Services Name Availability Structure](https://apis.io/json-structure/mojang/minecraft-services-name-availability-structure/)
- [Minecraft Services Name Change Info Structure](https://apis.io/json-structure/mojang/minecraft-services-name-change-info-structure/)
- [Minecraft Services Player Attributes Structure](https://apis.io/json-structure/mojang/minecraft-services-player-attributes-structure/)
- [Minecraft Services Player Attributes Update Structure](https://apis.io/json-structure/mojang/minecraft-services-player-attributes-update-structure/)
- [Minecraft Services Player Certificates Structure](https://apis.io/json-structure/mojang/minecraft-services-player-certificates-structure/)
- [Minecraft Services Presence Entry Structure](https://apis.io/json-structure/mojang/minecraft-services-presence-entry-structure/)
- [Minecraft Services Presence Report Structure](https://apis.io/json-structure/mojang/minecraft-services-presence-report-structure/)
- [Minecraft Services Privilege Map Structure](https://apis.io/json-structure/mojang/minecraft-services-privilege-map-structure/)
- [Minecraft Services Profanity Filter Preferences Structure](https://apis.io/json-structure/mojang/minecraft-services-profanity-filter-preferences-structure/)
- [Minecraft Services Profile Structure](https://apis.io/json-structure/mojang/minecraft-services-profile-structure/)
- [Minecraft Services Public Key Entry Structure](https://apis.io/json-structure/mojang/minecraft-services-public-key-entry-structure/)
- [Minecraft Services Public Keys Structure](https://apis.io/json-structure/mojang/minecraft-services-public-keys-structure/)
- …and 9 more published on APIs.io

#### JSON-LD (4)

Linked-data contexts for the provider's vocabulary.

- [Mojang Api Context](https://apis.io/jsonld/mojang/mojang-api-context/)
- [Mojang Minecraft Services Context](https://apis.io/jsonld/mojang/mojang-minecraft-services-context/)
- [Mojang Public Api Context](https://apis.io/jsonld/mojang/mojang-public-api-context/)
- [Mojang Session Server Context](https://apis.io/jsonld/mojang/mojang-session-server-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Mojang Vocabulary](https://apis.io/vocabularies/mojang/mojang-vocabulary/)

#### Examples (34)

Example requests and responses.

- [Minecraft Services Authenticated Profile Example](https://apis.io/examples/mojang/minecraft-services-authenticated-profile-example/)
- [Minecraft Services Ban Status Example](https://apis.io/examples/mojang/minecraft-services-ban-status-example/)
- [Minecraft Services Blocklist Example](https://apis.io/examples/mojang/minecraft-services-blocklist-example/)
- [Minecraft Services Cape Example](https://apis.io/examples/mojang/minecraft-services-cape-example/)
- [Minecraft Services Cape Selection Example](https://apis.io/examples/mojang/minecraft-services-cape-selection-example/)
- [Minecraft Services Change Skin Request Example](https://apis.io/examples/mojang/minecraft-services-change-skin-request-example/)
- [Minecraft Services Entitlement Item Example](https://apis.io/examples/mojang/minecraft-services-entitlement-item-example/)
- [Minecraft Services Entitlements Example](https://apis.io/examples/mojang/minecraft-services-entitlements-example/)
- [Minecraft Services Friend Example](https://apis.io/examples/mojang/minecraft-services-friend-example/)
- [Minecraft Services Friend Update Request Example](https://apis.io/examples/mojang/minecraft-services-friend-update-request-example/)
- [Minecraft Services Friends List Example](https://apis.io/examples/mojang/minecraft-services-friends-list-example/)
- [Minecraft Services Friends Preferences Example](https://apis.io/examples/mojang/minecraft-services-friends-preferences-example/)
- [Minecraft Services Minecraft Access Token Example](https://apis.io/examples/mojang/minecraft-services-minecraft-access-token-example/)
- [Minecraft Services Name Availability Example](https://apis.io/examples/mojang/minecraft-services-name-availability-example/)
- [Minecraft Services Name Change Info Example](https://apis.io/examples/mojang/minecraft-services-name-change-info-example/)
- [Minecraft Services Player Attributes Example](https://apis.io/examples/mojang/minecraft-services-player-attributes-example/)
- [Minecraft Services Player Attributes Update Example](https://apis.io/examples/mojang/minecraft-services-player-attributes-update-example/)
- [Minecraft Services Player Certificates Example](https://apis.io/examples/mojang/minecraft-services-player-certificates-example/)
- [Minecraft Services Presence Entry Example](https://apis.io/examples/mojang/minecraft-services-presence-entry-example/)
- [Minecraft Services Presence Report Example](https://apis.io/examples/mojang/minecraft-services-presence-report-example/)
- [Minecraft Services Privilege Map Example](https://apis.io/examples/mojang/minecraft-services-privilege-map-example/)
- [Minecraft Services Profanity Filter Preferences Example](https://apis.io/examples/mojang/minecraft-services-profanity-filter-preferences-example/)
- [Minecraft Services Profile Example](https://apis.io/examples/mojang/minecraft-services-profile-example/)
- [Minecraft Services Public Key Entry Example](https://apis.io/examples/mojang/minecraft-services-public-key-entry-example/)
- [Minecraft Services Public Keys Example](https://apis.io/examples/mojang/minecraft-services-public-keys-example/)
- …and 9 more published on APIs.io

#### Collections (17)

Postman and Open Collection request collections.

- [Minecraft Services Attributes API](https://apis.io/collections/mojang/open-mojang-attributes-api/)
- [Minecraft Services Attributes Authentication API](https://apis.io/collections/mojang/open-mojang-authentication-api/)
- [Minecraft Services Attributes Blocklist API](https://apis.io/collections/mojang/open-mojang-blocklist-api/)
- [Minecraft Services Attributes Capes API](https://apis.io/collections/mojang/open-mojang-capes-api/)
- [Minecraft Services Attributes Entitlements API](https://apis.io/collections/mojang/open-mojang-entitlements-api/)
- [Minecraft Services Attributes Friends API](https://apis.io/collections/mojang/open-mojang-friends-api/)
- [Minecraft Services Attributes Identity API](https://apis.io/collections/mojang/open-mojang-identity-api/)
- [Minecraft Services Attributes Keys API](https://apis.io/collections/mojang/open-mojang-keys-api/)
- [Minecraft Services API](https://apis.io/collections/mojang/open-mojang-minecraft-services/)
- [Minecraft Services Attributes Presence API](https://apis.io/collections/mojang/open-mojang-presence-api/)
- [Minecraft Services Attributes Profile API](https://apis.io/collections/mojang/open-mojang-profile-api/)
- [Mojang Public API](https://apis.io/collections/mojang/open-mojang-public-api/)
- [Minecraft Services Attributes Server API](https://apis.io/collections/mojang/open-mojang-server-api/)
- [Minecraft Services Attributes Session API](https://apis.io/collections/mojang/open-mojang-session-api/)
- [Mojang Session Server](https://apis.io/collections/mojang/open-mojang-session-server/)
- [Minecraft Services Attributes Skins API](https://apis.io/collections/mojang/open-mojang-skins-api/)
- [Minecraft Services Attributes Textures API](https://apis.io/collections/mojang/open-mojang-textures-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Mojang — jsonschema rules](https://apis.io/rules/mojang/mojang-jsonschema-spectral-rules/)
- [Mojang API Rules](https://apis.io/rules/mojang/mojang-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Mojang Authentication](https://apis.io/security/mojang/mojang-authentication/)
- [Mojang Domain Security](https://apis.io/security/mojang/mojang-domain-security/)

#### Rate limits (1)

Published request limits.

- [Mojang Rate Limits](https://apis.io/rate-limits/mojang/mojang-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.minecraft.net)
- [Documentation](https://minecraft.wiki/w/Mojang_API)
- [GitHub](https://github.com/Mojang)

## API Evangelist rating

**Kin Score 23.9** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 22.0 |
| Contract governance | 27.3 |
| Operational transparency | 26.3 |
| Developer ergonomics | 21.4 |
| Access clarity | 0.0 |

**Agent readiness 26.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 16.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/mojang/](https://apis.io/providers/mojang/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Mojang: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/mojang/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
