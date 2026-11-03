# Security Policy

## Supported software

Security reports are accepted for repositories under [github.com/qimerp](https://github.com/qimerp), including public packages (`QFace.Sdk`, `QimErp.Proxy`) and private product services.

## Reporting a vulnerability

**Do not open a public GitHub issue for security findings.**

Prefer one of:

1. **GitHub private vulnerability report** on the affected repository (Security → Report a vulnerability), when enabled
2. A **private** message to an organization owner listed at https://github.com/orgs/qimerp/people

Include:

- Affected repository and approximate version / commit
- Impact (auth bypass, tenant isolation, data exposure, RCE, etc.)
- Steps to reproduce or a minimal proof of concept
- Whether you are under a disclosure deadline

We aim to acknowledge within **3 business days** and to keep you informed until the issue is resolved or declined.

## Scope notes

- Multi-tenant isolation, authentication/authorization, payroll/payment paths, and secrets handling are highest priority.
- Out-of-scope: social engineering, denial-of-service against shared infrastructure you do not own, and findings that require physical access or an already-compromised admin account with no further privilege gain.
