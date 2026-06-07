# Job language mapping

Use this dictionary to recognize honest matches and related experience. It does not authorize adding absent facts.

| Job term | Plain concept | Related concepts | Resume evidence that counts |
|----------|---------------|------------------|-----------------------------|
| Ledger | Source-of-truth financial state | balances, credits, debits, transactional consistency | Explicit finance/accounting state ownership only |
| Exactly-once | Duplicate-safe processing | deduplication, idempotency, replay handling, outbox | Source text naming duplicate prevention or replay safety |
| Idempotency | Safe repeated execution | idempotency keys, retry-safe handlers, duplicate suppression | Explicit retry or duplicate-handling facts |
| Usage-based billing | Bill by measured consumption | usage records, metering, overages, quotas | Source text naming measured usage feeding charges |
| Metering | Collect and aggregate usage events | event aggregation, windows, late-arrival handling | Source text naming usage event collection or aggregation |
| Reconciliation | Compare expected vs actual state | invoice accuracy, settlement checks, anomaly review | Source text naming comparison or correction of financial state |
| Entitlement | Product access based on plan/state | feature gates, plan limits, workspace settings | Source text naming access control tied to customer/account state |
| Proration | Mid-cycle billing adjustment | plan changes, partial periods, credits | Source text naming mid-cycle charge or credit handling |
| Observability | Production visibility | metrics, logs, traces, dashboards, alerts | Source text naming monitoring, alerting, or debugging systems |
| On-call | Production ownership | incident response, runbooks, alerts | Source text naming on-call or production response |
| CI/CD | Automated delivery | preview deploys, release pipelines, checks | Source text naming automated build, test, or deploy paths |
| Code review | Engineering quality process | design docs, reviews, mentorship | Source text naming review or technical guidance |
| Hiring | Team growth | interviews, rubrics, onboarding | Source text naming hiring or onboarding work |
| Mentorship | Raise team capability | coaching, pairing, design review | Source text naming engineers mentored or guided |
| Cross-functional | Work across teams | product, design, support, finance, CS | Source text naming partner teams or shared workflows |
| Reliability | Product correctness under change | alerts, validation, tests, rollback, support escalation reduction | Source text naming defects, monitoring, tests, or support impact |

When a job term maps only to a related concept, treat it as a bridge or suggestion-mining lead, not a direct match.
