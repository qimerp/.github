# Contributing to QimERP

Most repositories are private. This guide is the org default when a repository does not define its own `CONTRIBUTING.md`.

## Branches

| Branch | Role |
| --- | --- |
| `development` | Default integration branch for product work |
| `main` | Release / production-tracking line where the repo uses one |

Open pull requests against **`development`** unless the repository README says otherwise. Do not force-push shared branches.

## Pull requests

- Keep the change scoped to one concern; avoid drive-by refactors.
- Fill in the PR template (summary + test plan).
- Ensure CI on the PR is green before asking for merge.
- Prefer team reviewers via `CODEOWNERS` (`@qimerp/backend`, `@qimerp/frontend`, `@qimerp/platform-infra`, `@qimerp/core-engineering`).

## Backend (.NET)

- Each `QimErp.*` directory / repo is its own solution — build and test that solution.
- Tests use EF Core InMemory (no Docker/Testcontainers in product repos).
- Never bypass tenant filters, weaken auth checks, or commit secrets.
- Long-running work goes through Temporal, not fire-and-forget tasks.

## Frontend

- Zone apps live under `qimerp-*-web` / `qimerp-web-foundation`.
- Follow the app’s `AGENTS.md` and shared UI (`@qimerp/ui`) conventions.
- Run the package’s documented `type-check` / `lint` before pushing.

## Infrastructure & CI

- Runtime and CI are on Contabo — see `qimerp-infra`.
- Self-hosted runners use label `qimerp-ci`. Prefer `runs-on: [self-hosted, qimerp-ci]` for product workflows.
- Do not point new work at retired Railway hosts.

## Secrets

Never commit credentials, tokens, connection strings, or `.env` files with real values. Prefer repository/org secrets and documented local overrides that stay gitignored.
