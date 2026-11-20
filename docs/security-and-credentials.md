# Credentials and access — policy

**Never commit secrets to this public repository**, even in private-looking folders or deleted commits.

## Credential classes
- Supabase: public client key (publishable where intended), service-role/secret keys (server-only), database credentials.
- n8n: encryption key, user credentials, API keys, workflow credential stores.
- Evolution API: API authentication keys and per-instance session credentials.
- Twilio: Account SID and Auth Token/API keys, webhook signature validation material, Messaging Service identifiers.
- AI provider: model/API credentials.
- Stripe: publishable key (client-side where intended), secret keys and webhook signing secrets (server-only).

## Recommended handling
1. Keep a **private** inventory of service owner, environment, credential label, storage location, rotation date and authorized roles. Never record secret values in the inventory.
2. Store production secrets in a dedicated secrets manager or host-managed encrypted environment variables.
3. Use separate credentials for development, staging and production.
4. Apply least privilege; keep database service-role keys out of browsers and client-side apps.
5. Rotate exposed credentials immediately and audit their use.
6. Protect n8n and Evolution administration with HTTPS, strong authentication and restricted access.
7. Never share credentials in screenshots, issue bodies, chat logs or support tickets.

## Safe inventory template
| Service | Environment | Credential label | Vault reference (non-secret) | Owner role | Rotation policy | Verified? |
|---|---|---|---|---|---|---|
| Supabase | Production | Backend service key | **PRIVATE INVENTORY ONLY** | Platform admin | On incident/periodic | No |
| n8n | Production | Encryption key | **PRIVATE INVENTORY ONLY** | Platform admin | Controlled recovery plan | No |
| Evolution API | Production | API key | **PRIVATE INVENTORY ONLY** | Platform admin | On incident/periodic | No |
| Twilio | Production | Messaging API key | **PRIVATE INVENTORY ONLY** | Platform admin | On incident/periodic | No |

This table is a template, not a claim that production secrets have been configured.
