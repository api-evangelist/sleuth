# Sleuth (sleuth)

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
