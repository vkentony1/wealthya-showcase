# Wealthya: a two-minute case study

## Challenge

Portfolio decisions depend on records, market context and questions that deserve investigation. When these sit in separate places, the owner has to rebuild the whole picture before every decision, and stale or unsourced numbers are easy to trust by mistake.

## Approach

I framed the task as a product workflow rather than a feature list: record the portfolio, bring relevant context into view, surface the questions that need research, and keep final judgment with the human owner. Privacy, provenance and a hard "no trading" boundary were constraints from the start, not later additions. The reasoning is written up in [product decisions](product-decisions.md).

## My Role

I owned problem framing, requirements, workflow and system design, prioritization and product decisions. I translated business needs into behaviour for the product, directed AI-assisted implementation, reviewed the outputs, and drove testing and iteration. This is an AI-assisted product development case. I do not claim to have written every line of code, and I do not present myself as a traditional software engineer.

## What Was Built

The private Wealthya project (developed as OwnerOS in the app) contains:

- a web app and PWA with a private owner profile and a separate commercial workspace with empty-state onboarding;
- a native SwiftUI app for iPhone and Mac with five tabs (Overview, Assets, Watchlist, Market, Copilot);
- a versioned, tenant-scoped API with an append-only audit trail, data export and account deletion;
- a deterministic financial core (exact money, mixed-currency rejection) covered by automated tests;
- market context that carries its source, observed time and freshness;
- an optional AI Copilot and per-asset research with cited sources, which falls back to a local mode when the AI service is unavailable.

The project is pre-launch. See the [product tour](product-tour.md) and [status and roadmap](status-and-roadmap.md).

## How AI Was Used

AI accelerated implementation and iteration after the problem and the expected behaviour had been specified. It was a collaborator for execution, while priorities, acceptance and the decision about what not to build stayed human.

## How Outputs Were Reviewed

I reviewed generated work against the requirements, checked it for unsupported assumptions, ran the relevant tests, and revised the product when gaps appeared. A passing local check is evidence for that check only; it is not proof of every user-facing or production behaviour. Journeys on a physical iPhone are kept as a manual gate rather than counted as an automated pass.

## Technical Exposure

The project required learning across web interface work, application workflows, data modelling, native iOS and macOS development, and API design. I worked with AI tools throughout and kept a clear view of user needs and system boundaries.

## Outcome and Learning Demonstrated

The result is a real, evolving software product and a repeatable way to move from a business problem to tested software. It demonstrates practical contribution potential for team projects at the intersection of AI Business & Product and AI Applications. No user counts, revenue, investment performance or other unverified outcome is claimed.
