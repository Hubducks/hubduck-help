---
layout: default
title: Testing Playbook
nav_order: 10
---

# Testing Playbook (Meta Pattern)

The core delivery principle for HubDuck is:

**Requirements -> Build -> Data -> Verify**

Every story ships with:

- A written journey contract (Given/When/Then) that names routes, UI selectors, and API contracts.
- Seed data generation so the UI can be verified immediately.
- An executable E2E that proves the journey and captures a screenshot.

This avoids "build it, then hunt for data" and makes every step explainable.

## What "Explainability" Means Here

- Requirements are executable: journeys exist as Playwright specs.
- Data is deterministic: a seed/fixture API creates org + users + ducks + emails.
- UI verification is concrete: screenshots and stable `data-testid` selectors.

## Local Setup

HubDuck runs locally as:

- Backend: `http://localhost:8038`
- Frontend: `http://localhost:3038`

### Start Backend

```bash
cd hubduck-backend
E2E_SEED_ENABLED=true E2E_SEED_SECRET=local-e2e-seed-secret-1234 npm run start:dev
```

### Start Frontend

```bash
cd hubduck-frontend
npm run dev
```

## Seed + Fixture Injection (For E2E)

Backend provides local-only endpoints:

- `POST /e2e/seed` (creates org + users + ducks)
- `POST /e2e/fixtures/emails` (injects processed emails into a duck)
- `POST /e2e/cleanup` (deletes seeded org data)

All `/e2e/*` endpoints require the `x-e2e-seed-secret` header matching `E2E_SEED_SECRET`.

## Playwright Journeys

The minimum bar for a journey spec:

1. Seed org/users/ducks
2. Inject emails
3. Login in the UI
4. Verify key UI state
5. Take an action (hide, pin, acknowledge, add-to-calendar, etc.)
6. Refresh and prove persistence
7. Screenshot
8. Cleanup

## Core Conventions

- Use stable selectors: `data-testid` instead of text queries.
- Avoid flaky dependencies (LLM calls, emails, time) inside core E2E journeys.
- Separate "AI quality" tests from "UI journey" tests.

