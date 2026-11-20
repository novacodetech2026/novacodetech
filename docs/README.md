# Novacode Tech — Technical documentation

> **Public-safe documentation only.** This repository is public. Do not add credentials, account IDs, customer data, webhook URLs, internal IPs, live endpoints, or exported workflows containing secrets.

## Index
- [Architecture](architecture.md): conceptual system boundaries and request flow.
- [Service inventory](service-inventory.md): ownership and responsibilities, without secrets.
- [Security and credentials](security-and-credentials.md): handling secrets and access.
- [Operations checklist](operations-checklist.md): rollout and reliability tasks.

## Documentation conventions
- Mark each item **Verified**, **Reported**, **Pending**, or **Not checked**.
- Never treat a development test as production readiness.
- Production configuration and secret locations belong in a private access-controlled inventory, **not** this public repository.
- Changes to booking and identity workflows must be tested with multiple tenants.
