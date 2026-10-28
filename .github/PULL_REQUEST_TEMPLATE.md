### Description
What changed and why, in 1-2 sentences. For a bug fix, say the root cause, not only the symptom. Ticket number if there is one.

<!-- Remove any section below that has no content. Don't write "N/A". -->

### Testing
Commands you ran and their output, or screenshots / a recording for UI changes. Evidence, not "tested locally".

What these checks would NOT catch (what you did not or could not test):

### Risk
Tier: low / medium / high, and why. Say whether this touches auth, billing, caching, CI workflows, prompts, or data that cannot be rebuilt.

### How to revert
The feature flag to flip, or the exact steps (revert commit, redeploy, undo a migration or data change). Say "plain revert is safe" only if it is.

### Production Readiness Review

For PRs touching hot paths (cache, locks, DB queries, request handlers, autoscaling, retry/timeout policies, third-party API calls, queue consumers), answer both questions:

**1. What happens to this code under 10x load?**
<!-- Concrete answer. Example: "It calls the DB once per item with no batching, so 1000 requests would mean 1000 queries." -->

**2. What is the failure mode if a dependency (DB, cache, third-party API) is slow or unavailable?**
<!-- Concrete answer. Example: "The sync HTTP call has a 30s default timeout and would block the whole pool." -->

If the answer to either is "I don't know" or "it would cascade", say so here and tag a senior reviewer. Remove this section for non-hot-path PRs (refactors, docs, tests, config).

### Extra Info
Screenshots, videos, deployment notes, breaking changes, follow-ups, companion PRs.
