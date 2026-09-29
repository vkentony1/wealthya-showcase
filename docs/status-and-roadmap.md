# Status and roadmap

An honest snapshot of where the project stands. It is taken from the private project's documentation and repository contents, so treat it as a self-report rather than an audit. The last column says how each line can be checked in principle; the private source is intentionally not published here.

## Where things stand

| Area | Status | Notes |
|---|---|---|
| Web app, private owner profile | Working, private | Used by the owner in a local, private runtime. |
| Web app, commercial workspace | First slice implemented | Empty-state onboarding, portfolio summary, asset create, edit and delete, settings, data export, owner-confirmed account deletion. |
| Backend and tenant isolation | First slice implemented | Tenant-scoped portfolio and asset APIs, append-only audit trail, JSON export. |
| Native iPhone and Mac app | Shell implemented, not distributed | SwiftUI, five tabs, Sign in with Apple, keychain session storage, Face ID or passcode gate, offline draft queue. |
| Financial calculation core | Implemented and tested | Exact minor-unit arithmetic, rejection of mixed currencies, automated tests. |
| Automated checks | Workflow defined | Web contract and rendering tests plus Swift core tests run in CI. Journeys on a physical iPhone remain a manual gate and are not represented as a simulated pass. |
| Billing and subscriptions | Not implemented | Launch is blocked until this is done. |
| Licensed market and news data | Not implemented | No redistribution or commercial territory is enabled without a signed licence. |
| Public release or TestFlight | Not yet | Gated by the acceptance list below. |
| Users, revenue, measured outcomes | None claimed | The project is pre-launch. |

## Timeline

The private repository's first commit is from July 2026, and active development continued through August 2026, with further work on a working branch in late September. Most commits were authored by an AI coding agent working from my specifications, which matches the AI-assisted process described in [development process](development-process.md).

## Acceptance gates before any public launch

- Real authentication, tenant isolation, encryption, export and deletion, backup and restore, and incident response are operational.
- Every high-stakes claim has provenance, a statement of uncertainty and an approval route.
- Store metadata uses synthetic accounts and makes no unverifiable performance claim.
- No financial connector, data redistribution or personalised advice is enabled without its contract or licence.
- Vietnamese and English copy is reviewed, and currency, dates and accessibility are locale-correct.

## Planned next slice

1. Finish replay and nonce tests around the Sign in with Apple identity check.
2. Add a metered intelligence entitlement (standard brief, deep research, licensed data add-ons).
3. Add a subscription and restore flow with server-side entitlement verification before TestFlight.
4. Complete privacy, security, accessibility, localisation and store-review evidence.

## Why publish a list of what is missing

A portfolio that only shows strengths is hard to trust. Naming the gaps, and the gates that stop the product from shipping before they close, is part of the product judgment this repository is meant to demonstrate. See [product decisions](product-decisions.md).
