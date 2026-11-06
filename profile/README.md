# QimERP

Multi-tenant ERP by **[Q-FACE Solutions](https://github.com/qimerp)** — People, Finance, Payroll, Operations, Performance, Learning, plus tenant and platform administration.

## Product surface

| Area | Repositories |
| --- | --- |
| Platform & operator | `QimErp.Platform` (auth, tenancy, billing, onboarding — formerly IAM), `QimErp.Operator` |
| Backend services | `QimErp.CoreHr`, `QimErp.Finance`, `QimErp.Operations`, `QimErp.Payroll`, `QimErp.Learning`, `QimErp.Performance`, `QimErp.HROperations`, `QimErp.Core.Reporting` |
| Shared SDK / gateway | `QFace.Sdk`, `QimErp.Proxy` |
| Frontend zones | `qimerp-people-web`, `qimerp-finance-web`, `qimerp-payroll-web`, `qimerp-operations-web`, `qimerp-performance-web`, `qimerp-learning-web`, `qimerp-operator-web`, `qimerp-tenant-admin-web`, `qimerp-self-service-web`, `qimerp-pos-web`, `qimerp-saas-frontend`, `qimerp-web-foundation` |
| Design | `qimerp-ux-designs` |
| Mobile | `qimerp-ess-mobile` |
| Infrastructure | `qimerp-infra` |

Default integration branch across product repos is **`development`**.

## How we work

- One coherent product, split into independently deployable services and Next.js apps
- Shared identity, tenant/company context, shell, and design system via foundation packages
- Contabo runtime + self-hosted CI (`qimerp-ci`) — see `qimerp-infra`
- Deployed bare-metal service names match projects where cut over (e.g. `qimerp-platform`, `qimerp-operator`)

## Teams

- **core-engineering** — maintainers across the product
- **backend** — microservices and SDK
- **frontend** — zone apps and foundation
- **platform-infra** — runtime, CI, and shared platform

> Most application repositories are private. Public entry points today include `QFace.Sdk` and `QimErp.Proxy`.
