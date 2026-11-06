# Review: label the own-vessel track with its configured name

**Owner review only. No pull request or upstream issue has been submitted.**

Upstream: https://github.com/SignalK/tracks
Base: `423c6e5cf42b4379e358fd7c05d1495a2c11cce7`

## Problem and proposed behavior

The own-vessel track is always labelled Own Ship despite a configured vessel name. Reuse the existing name lookup and retain Own Ship for missing/blank names; AIS labels stay unchanged.

## Scope and decisions

No recording, database schema, historical migration, retention, thinning or sampling changes. Test vessel names are examples, not production constants.

## Validation status

The branch was prepared from current upstream source. Patch applicability and
diff whitespace checks are verified during preparation. These are review drafts,
not a claim of passing CI, deployment readiness or completed hardware validation.

## Before upstream submission

- [ ] Run the included name, wrapped-value, whitespace and fallback regression tests and the full upstream checks.

Keep boat identity, credentials, live data, custom release suffixes and deployment
scripts out of an upstream submission. Publish nothing to the parent until approved.

## Preparation results — 6 November 2026

Fresh local validation on Node 26.12.1: npm ci, upstream typecheck and npm test succeeded; 1,320 tests passed and 6 were skipped. The candidate includes the vessel-name regression.
