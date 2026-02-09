---
layout: default
title: E2E Journeys
nav_order: 20
---

# E2E Journeys

This is the canonical list of end-to-end journeys we maintain.

## Email Triage (Seeded)

Contract:

- Given a seeded org with a teacher user and a teacher duck
- And injected processed emails
- When the teacher logs in and opens the dashboard
- Then emails render
- When the teacher hides an email
- Then it disappears
- And after refresh it remains hidden

Implementation reference:

- Frontend: `hubduck-frontend/tests/e2e/journey_email_triage_seeded.spec.ts`

