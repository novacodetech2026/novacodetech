# Service inventory (public-safe)

| Component | Responsibility | Known status | Production verification |
|---|---|---|---|
| GitHub | Version control and website source | Website repository in use | Branch protection and deployment checks not reviewed |
| GitHub Pages | Public marketing website | Published from repository | Check build/deployment status after changes |
| Supabase | Database, Auth, RLS, booking RPCs | In use in development/tests | Review RLS, backups, migration tracking and capacity |
| Google AI Studio | Dashboard development | Development environment reported | Confirm production hosting and build |
| n8n | Workflow orchestration | Previously operated locally | Deploy durable hosting, health checks, persistence |
| Evolution API | WhatsApp channel integration | Local integration tested | Verify production connection and per-tenant isolation |
| Twilio | SMS messaging | A2P campaign approved (user-reported) | Check Messaging Service sender, delivery and webhooks |
| Stripe | Subscription billing | Configuration pending | Set up products, subscriptions, webhooks and access policy |

## Environments
- **Development**: local/test instances and sample tenants; never assume 24/7 uptime.
- **Staging (planned)**: realistic tests with non-production credentials and synthetic data.
- **Production (planned/partially deployed)**: durable hosted services with HTTPS, secrets management, monitoring and recovery.

## Ownership model
- Novacode platform administrators provision messaging channels.
- Business users manage their own services, hours, appointments and customers through scoped permissions.
- Platform administrators see aggregated usage and actionable incidents rather than individual routine bookings.

## Information deliberately omitted
No API keys, tokens, secret identifiers, tenant identifiers, phone numbers, customer records, service URLs, or private network topology are stored here.
