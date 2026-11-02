# QimERP

Multi-tenant ERP by **Q-FACE Solutions** — People, Finance, Payroll, Operations, Performance, Learning, plus tenant and platform admin.

## Working model

| Area | Repos |
| --- | --- |
| Backend services | `QimErp.*`, `QFace.Sdk`, `QimErp.Proxy` |
| Frontend zones | `qimerp-*-web`, `qimerp-web-foundation` |
| Mobile | `qimerp-ess-mobile` |
| Infra / CI | `qimerp-infra` |
| Legacy reference | `qimerp-saas-frontend` |

Default integration branch is **`development`**.

## Teams

- **core-engineering** — maintainers across the product
- **backend** — microservices and SDK
- **frontend** — zone apps and foundation
- **platform-infra** — Contabo runtime, CI, shared platform

## Notes

- Org is private-by-default. Only invite people through teams.
- Private branch protection needs **GitHub Team**. Public repos (`QFace.Sdk`, `QimErp.Proxy`) already have branch protection where applicable.
- CI runners use Contabo label `qimerp-ci` — see `qimerp-infra`.
