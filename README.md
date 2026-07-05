# Circle (circle-community)

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
