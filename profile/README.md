# QimERP

Multi-tenant ERP by **[Q-FACE Solutions](https://github.com/qimerp)** — People, Finance, Payroll, Operations, Performance, Learning, plus tenant and platform administration.

## Product surface

| Area | Repositories |
| --- | --- |
| Backend services | `QimErp.CoreHr`, `QimErp.Finance`, `QimErp.IAM`, `QimErp.Operations`, `QimErp.Payroll`, `QimErp.Learning`, `QimErp.Performance`, `QimErp.Core.Reporting` |
| Shared SDK / gateway | `QFace.Sdk`, `QimErp.Proxy` |
| Frontend zones | `qimerp-*-web`, `qimerp-web-foundation` |
| Mobile | `qimerp-ess-mobile` |
| Infrastructure | `qimerp-infra` |

Default integration branch across product repos is **`development`**.

## How we work

- One coherent product, split into independently deployable services and Next.js apps
- Shared identity, tenant/company context, shell, and design system via foundation packages
- Contabo runtime + self-hosted CI (`qimerp-ci`) — see `qimerp-infra`

## Teams

- **core-engineering** — maintainers across the product
- **backend** — microservices and SDK
- **frontend** — zone apps and foundation
- **platform-infra** — runtime, CI, and shared platform

> Most application repositories are private. Public entry points today include `QFace.Sdk` and `QimErp.Proxy`.
