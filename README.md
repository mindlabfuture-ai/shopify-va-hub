# Shopify VA Hub

A unified workspace for Shopify virtual assistants (VAs) and the store owners who hire them.

Status: discovery. See [`docs/research/pain-points.md`](docs/research/pain-points.md) and [`docs/design/concept.md`](docs/design/concept.md).

## Goal
Replace the patchwork of shared logins, spreadsheets, chat threads and SOP docs that owners and VAs use today with one app: scoped access, task queues driven by SOPs, bulk catalog tools with preview/undo, and an owner-visible activity log.

## Roadmap
1. Validate pain points with primary sources (Reddit, Shopify Community, VA Facebook groups, interviews).
2. Phase 1, the toolkit: free browser tools, guides and downloadable templates on mindlabfuture-ai.com. Shipped so far: CSV checker and 3 guides (sms-compliance PR #32). Next: SOP and checklist builder. See [`docs/strategy/hub-strategy.md`](docs/strategy/hub-strategy.md).
3. Instrument the site (analytics, Search Console) and set a baseline.
4. Phase 2: build the hub app (scoped access, SOP task queue, change history) as an embedded Shopify app, reusing auth/billing/API layers from VIPriority and POPLoad.
