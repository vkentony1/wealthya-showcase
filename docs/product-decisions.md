# Product decisions

The decisions below shaped Wealthya more than any single feature. Each one is a product judgment: what to include, what to refuse, and what to make visible. They come from the private project's own design documents and are listed here with the reasoning and the trade-off.

## 1. Decision support only, with no trading capability

**Decision.** The product records, monitors and researches. It never places orders or moves money.
**Why.** Trust and safety come before convenience. A tool that cannot act cannot act wrongly, and the owner stays accountable for every decision.
**In the product.** The backend has no trade or order endpoint. The copy states that the product does not guarantee returns or replace licensed professionals.
**Trade-off.** Less "magic". The owner still takes the final step outside the app.

## 2. Local-first and private by default

**Decision.** Start as a private, personal tool, and add a separate commercial workspace only afterwards.
**Why.** Portfolio data is among the most sensitive data a person has. Proving the workflow privately first avoids designing for scale before the product is useful.
**In the product.** The personal profile and the commercial workspace use separate sessions and do not mix data. New commercial users start from an empty workspace with guided onboarding.
**Trade-off.** Slower reach in exchange for a smaller blast radius.

## 3. Keep the arithmetic deterministic and separate from AI

**Decision.** Portfolio maths is ordinary, tested code. AI is used for research and explanation, never to compute canonical figures.
**Why.** A model can be persuasive and wrong. Numbers that drive decisions must be reproducible.
**In the product.** Net asset value is computed in exact minor units, mixed currencies are rejected rather than guessed at, and the same calculations are tested independently on the web and native sides.
**Trade-off.** More engineering effort than letting a model summarise the portfolio.

## 4. Every number carries its provenance

**Decision.** Market context is shown together with where it came from and how fresh it is.
**Why.** The dangerous case is a stale or unlicensed number that looks authoritative.
**In the product.** Each quote exposes its provider, market state, observed time, staleness and licence scope. A lower-quality fallback source is labelled as such rather than blended in silently.
**Trade-off.** A busier display, but an honest one.

## 5. AI is optional and degrades gracefully

**Decision.** The Copilot must remain useful when the AI service is unavailable.
**Why.** Dependence on a single external service is a product risk, and so is a broken screen at the moment the owner needs help.
**In the product.** Without an AI key or when the service is down, chat falls back to a local mode that answers from the owner's own records and market data. Service keys stay on the server side only.
**Trade-off.** Two modes to design and test.

## 6. A real native app, not a web wrapper

**Decision.** Build the iPhone and Mac app natively rather than wrapping the website.
**Why.** Security, accessibility and everyday feel depend on platform features a wrapper handles poorly.
**In the product.** SwiftUI app with Sign in with Apple, session storage in the system keychain, a Face ID or passcode gate before assets are shown, and an offline draft queue.
**Trade-off.** Two client codebases, mitigated by a single set of versioned API contracts.

## 7. The server is the source of truth; clients only draft

**Decision.** Offline clients never invent canonical facts. They create drafts that the server accepts, rejects or reconciles.
**Why.** Two devices editing the same record offline is the classic way to corrupt a ledger.
**In the product.** Drafts are queued with idempotency keys and synced; the server stays authoritative after sync.
**Trade-off.** A slightly less instant feel offline.

## 8. Gate the launch, not just the build

**Decision.** Define acceptance gates before public release, and refuse to launch until they pass.
**Why.** Financial products fail on trust. Shipping first and fixing later is not an option for authentication, data isolation, deletion and licensing.
**In the product.** Gates cover real authentication, tenant isolation, encryption, export and deletion, backup and restore, licensed data rights, privacy review and store review. Billing and licensed market data are deliberately not enabled yet.
**Trade-off.** Slower to market, and a clear written list of what is still missing. See [status and roadmap](status-and-roadmap.md).

## What these decisions show

Scope was set by risk, not by what was easy to build. The same pattern appears in each item: name the failure that would hurt most, then design the product so that failure is impossible or at least visible.
