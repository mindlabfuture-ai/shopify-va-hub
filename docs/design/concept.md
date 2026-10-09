# Concept: Shopify VA Hub

## Users
- Owner: wants to delegate safely and see results.
- VA: wants clear tasks, the right access, and fewer tabs.

## Modules (candidate)
1. Scoped access: invite a VA with presets (Catalog, Orders, Support), optional expiry, one-click revoke. Works via staff or collaborator accounts and app-level scopes.
2. SOP task queue: owner turns an SOP into a checklist template; tasks (e.g. "list 20 products") get assigned, tracked and reviewed.
3. Bulk catalog workbench: CSV/Sheets import, diff preview before apply, undo.
4. Order and tracking board: unified view of unfulfilled orders, supplier confirmation, tracking, returns.
5. Activity log and time/output report: what changed, by whom, how long it took.
6. Support inbox (later): shared inbox with order context.

## Wedge options for MVP
| Option | Pain # | Effort | Notes |
|---|---|---|---|
| A. Scoped access + activity log | 3, 8 | Low-Med | Clear owner value, differentiated, limited by what Admin API exposes |
| B. Bulk catalog workbench with preview/undo | 1 | Med | Crowded space (bulk editors exist); win on safety and VA workflow |
| C. SOP task queue | 5 | Low | Easy to build, weak moat alone |

Recommendation: A + C as MVP (access, tasks, log), then B.

Round 2 update: undo apps already exist (each only reverts its own edits), so B should differentiate on a cross-source change history and "VA proposes, owner approves" before bulk changes apply. Add time-phased access presets to A (read-only week 1, widen by week 4), which matches the onboarding advice owners already follow by hand.

## Technical sketch
- Embedded Shopify app (Remix/React Router, Prisma, Postgres), Admin GraphQL API, webhooks for product/order change events feeding the activity log.
- Reuse auth, billing and deploy patterns from VIPriority/POPLoad.

## Open questions
- Does the native activity log cover enough that A is redundant? Validate first.
- Pricing: per store, per VA seat, or per task volume?
- Marketplace play (match owners and VAs) vs. pure tooling?
