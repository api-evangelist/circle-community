# Circle (circle-community)

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

Circle ([circle.so](https://circle.so)) is an all-in-one community platform for creators, coaches, and brands - hosting discussions, courses, events, live streams, memberships, paywalls, and chat under a single branded space, serving communities run by creators and institutions worldwide.

> **Disambiguation:** This entry documents **Circle the community platform at circle.so**, NOT Circle the USDC / stablecoin financial-services company. All APIs here are for community, courses, memberships, and chat.

Circle exposes a documented public developer platform:

- an **admin-authenticated Admin API (V2)** for automations, migrations, and bulk administration (base `https://app.circle.so/api/admin/v2`, `Authorization: Token AUTH_TOKEN`);
- a **Headless offering** - a **Member API** (base `https://app.circle.so/api/headless/v1`) for embedding Circle features into your own website or app, and an **Auth API** that exchanges a community token for a member-scoped JWT access token; and
- a **beta ActionCable WebSocket** at `wss://app.circle.so/cable` for realtime chat and notifications.

**Access model:** API access is plan-gated. The Admin API and the entire Headless offering (Member API, Auth API, and the beta WebSocket) require the **Business plan or above**. Admin API requests are admin-authenticated with a workspace token generated on the community's **Developers -> Tokens** page. Headless Member API and WebSocket requests are member-authenticated with a JWT access token that **expires after one hour** and is refreshed via the Auth API. The published Admin API rate limit is **2000 requests per 5 minutes per IP**.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/circle-community/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/circle-community/refs/heads/main/apis.yml)

## Tags

- Community
- Creators
- Courses
- Memberships
- Events
- Chat
- Community Platform

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Circle Admin Members API

Admin-authenticated management of community members - list, search, create, update, ban, and delete members; manage member tags and tagged members; and assign members to access groups.

- **Human URL:** [https://api.circle.so/apis/admin-api](https://api.circle.so/apis/admin-api)
- **Base URL:** `https://app.circle.so/api/admin/v2`

### Circle Admin Spaces API

Manage the foundational containers of a community - spaces, space groups, and their memberships (single and bulk).

- **Human URL:** [https://api.circle.so/apis/admin-api](https://api.circle.so/apis/admin-api)
- **Base URL:** `https://app.circle.so/api/admin/v2`

### Circle Admin Posts and Comments API

Create, list, retrieve, update, move, and delete posts across spaces, manage their comments, generate AI post summaries, and administer topics.

- **Human URL:** [https://api.circle.so/apis/admin-api](https://api.circle.so/apis/admin-api)
- **Base URL:** `https://app.circle.so/api/admin/v2`

### Circle Admin Events API

Create, list, get, update, duplicate, and delete community events, and manage event attendees.

- **Human URL:** [https://api.circle.so/apis/admin-api](https://api.circle.so/apis/admin-api)
- **Base URL:** `https://app.circle.so/api/admin/v2`

### Circle Admin Courses API

Administer course curricula - create, list, get, update, and delete course sections and lessons, and set a member's course lesson progress.

- **Human URL:** [https://api.circle.so/apis/admin-api](https://api.circle.so/apis/admin-api)
- **Base URL:** `https://app.circle.so/api/admin/v2`

### Circle Headless Member API

Member-authenticated server-side API for building your own member-facing experience - home feed, spaces, posts, comments, likes and reactions, bookmarks, events and RSVPs, courses and lessons, direct messages and chat rooms, notifications, and profile. Requests carry a member-specific JWT access token issued by the Auth API.

- **Human URL:** [https://api.circle.so/apis/headless/member-api](https://api.circle.so/apis/headless/member-api)
- **Base URL:** `https://app.circle.so/api/headless/v1`

### Circle Headless Auth API

Server-to-server authentication API that exchanges a community-level headless auth token for a member-scoped JWT access token (and refresh token) used to call the Member API. Access tokens expire after one hour. Auth SDKs exist for Node.js, Ruby, Go, and Python.

- **Human URL:** [https://api.circle.so/apis/headless/quick-start](https://api.circle.so/apis/headless/quick-start)
- **Base URL:** `https://app.circle.so/api/v1/headless`

### Circle Realtime WebSocket API

Beta ActionCable (Rails) WebSocket surface for realtime chat and notifications, connected at `wss://app.circle.so/cable` with a member Bearer access token and a whitelisted Origin header. Exposes a NotificationChannel and three chat channels (member room events, room-wide messages, thread events).

- **Human URL:** [https://api.circle.so/get-started/websockets-beta](https://api.circle.so/get-started/websockets-beta)
- **Base URL:** `wss://app.circle.so/cable`

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/circleco)
- [Website](https://circle.so)
- [Documentation](https://api.circle.so)
- [Plans](plans/circle-community-plans-pricing.yml)
- [Rate Limits](rate-limits/circle-community-rate-limits.yml)
- [Fin Ops](finops/circle-community-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
