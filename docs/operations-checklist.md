# Operations and launch checklist

## P0 — Reliability
- [ ] Confirm permanent hosting for n8n and Evolution API.
- [ ] Configure stable HTTPS endpoints and restricted administration.
- [ ] Verify persistent volumes and restore a test backup.
- [ ] Configure health checks, incident alerts and workflow error reporting.
- [ ] Document production/staging environments in a private inventory.

## P0 — Data security
- [ ] Audit Supabase RLS on every tenant table.
- [ ] Test tenant A cannot read or modify tenant B.
- [ ] Check idempotency on inbound provider message IDs and appointment creation.
- [ ] Verify customer identity before appointment lookup/cancellation.
- [ ] Ensure service credentials never reach frontend or public logs.

## P1 — Messaging
- [x] Twilio A2P 10DLC campaign approval **reported by owner**; not independently verified.
- [ ] Confirm approved campaign is linked to the correct Messaging Service and sender number.
- [ ] Configure and authenticate SMS inbound webhook.
- [ ] Test inbound and outbound SMS with real devices and check delivery logs.
- [ ] Verify opt-in/opt-out compliance and STOP/HELP handling.
- [ ] Verify Evolution API WhatsApp sessions and routing per tenant.
- [ ] Run a full message → availability → booking → dashboard test.

## P1 — Product and commercial readiness
- [ ] Confirm production deployment of business dashboard at intended app subdomain.
- [ ] Validate business onboarding, invitations, services and schedules.
- [ ] Test booking notifications and support incident flow.
- [ ] Connect website lead intake to a backend if desired; current form opens email client.
- [ ] Prepare a demo video using synthetic customers and clearly marked sample data.
- [ ] Configure Stripe subscriptions and verify billing webhook handling.

## Change control
Use feature branches and pull requests. Record test evidence and rollback steps before changing production infrastructure.
