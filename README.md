# Sleuth (sleuth)

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

Sleuth is a deployment-based DORA metrics platform that tracks software delivery performance. Teams register deployments, manual changes, and custom impact values through Sleuth's REST registration API and GraphQL surface, then Sleuth computes the four DORA metrics (deploy frequency, lead time, change failure rate, and mean time to recovery) across projects and environments.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sleuth/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sleuth/refs/heads/main/apis.yml)

## Tags

- DORA
- DevOps
- Deployment Tracking
- Engineering Metrics
- Continuous Delivery

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Sleuth Deployments Registration API

Registers code deployments against a project's deployment and environment by git SHA, with optional branch, tags, links, commits, files, and pull request metadata, so Sleuth can compute deploy frequency and lead time.

- **Human URL:** [https://help.sleuth.io/sleuth-dora/sleuth-api/deploy-registration](https://help.sleuth.io/sleuth-dora/sleuth-api/deploy-registration)
- **Base URL:** `https://app.sleuth.io/api/1`

#### Tags

- Deployments
- Registration
- Code Changes

#### Properties

- [Documentation](https://help.sleuth.io/sleuth-dora/sleuth-api/deploy-registration)
- [API Reference](https://help.sleuth.io/sleuth-dora/sleuth-api)
- [OpenAPI](openapi/sleuth-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sleuth.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sleuth.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Sleuth Manual Change API

Registers non-code, free-form manual changes (such as feature flag flips, infrastructure changes, or config updates) against a project so they appear on the Sleuth deploy timeline and factor into DORA metrics.

- **Human URL:** [https://help.sleuth.io/sleuth-dora/sleuth-api/manual-change](https://help.sleuth.io/sleuth-dora/sleuth-api/manual-change)
- **Base URL:** `https://app.sleuth.io/api/1`

#### Tags

- Manual Changes
- Change Sources

#### Properties

- [Documentation](https://help.sleuth.io/sleuth-dora/sleuth-api/manual-change)
- [OpenAPI](openapi/sleuth-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sleuth.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sleuth.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Sleuth Metric and Incident Impact API

Registers custom metric impact values (floats) and custom incident impact events (triggered, resolved, reopened) against an impact source so Sleuth can run anomaly detection and grade deploy health and change failure rate.

- **Human URL:** [https://help.sleuth.io/sleuth-dora/sleuth-api/custom-metric-impact-registration](https://help.sleuth.io/sleuth-dora/sleuth-api/custom-metric-impact-registration)
- **Base URL:** `https://app.sleuth.io/api/1`

#### Tags

- Impact
- Metrics
- Incidents

#### Properties

- [Documentation](https://help.sleuth.io/sleuth-dora/sleuth-api/custom-metric-impact-registration)
- [API Reference](https://help.sleuth.io/sleuth-dora/sleuth-api/custom-incident-impact-registration)
- [OpenAPI](openapi/sleuth-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sleuth.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sleuth.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Sleuth GraphQL API

Sleuth's primary public API, built on GraphQL - the same API Sleuth uses internally - for managing projects, environments, deployments, and metrics, with an interactive GraphiQL explorer at the endpoint.

- **Human URL:** [https://help.sleuth.io/sleuth-dora/sleuth-api](https://help.sleuth.io/sleuth-dora/sleuth-api)
- **Base URL:** `https://app.sleuth.io/graphql`

#### Tags

- GraphQL
- Projects
- Environments

#### Properties

- [Documentation](https://help.sleuth.io/sleuth-dora/sleuth-api)

### Sleuth Webhook Actions

Outbound webhook automation action that sends an HTTP POST with a JSON deployment payload to a URL of your choosing, signed with X-SLEUTH-TIMESTAMP and X-SLEUTH-SIGNATURE headers (Slack-style verification using your org API key).

- **Human URL:** [https://help.sleuth.io/sleuth-dora/sleuth-automations/actions/webhook](https://help.sleuth.io/sleuth-dora/sleuth-automations/actions/webhook)
- **Base URL:** `https://app.sleuth.io`

#### Tags

- Webhooks
- Automations
- Events

#### Properties

- [Documentation](https://help.sleuth.io/sleuth-dora/sleuth-automations/actions/webhook)

## Common Properties

- [GitHub Organization](https://github.com/sleuth-io)
- [LinkedIn](https://www.linkedin.com/company/sleuth-io)
- [Website](https://www.sleuth.io)
- [Documentation](https://help.sleuth.io/sleuth-dora/sleuth-api)
- [Plans](plans/sleuth-plans-pricing.yml)
- [Rate Limits](rate-limits/sleuth-rate-limits.yml)
- [Fin Ops](finops/sleuth-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
