## E2E Seeded Journey: CLI -> API -> UI (Playwright)

This is a fully deterministic end-to-end run you can repeat.

### 0) Start backend
cd hubduck-backend
E2E_SEED_ENABLED=true E2E_SEED_SECRET=local-e2e-seed-secret-1234 npm run start:dev

### 1) Run the seeded Playwright journey (creates org, injects 3 emails, logs in, hides 1, refreshes, screenshots)
cd ../hubduck-frontend
E2E_SEED_SECRET=local-e2e-seed-secret-1234 E2E_API_URL=http://localhost:8038 npx playwright test tests/e2e/journey_email_triage_seeded.spec.ts

### 2) Find the snapshot
The test saves a full-page screenshot named seeded-triage.png under test-results/.
Example from my run:
hubduck-frontend/test-results/journey_email_triage_seede-3c222-one-persists-after-refresh--chromium/seeded-triage.png

### 3) Start frontend to inspect manually
npm run dev
Open http://localhost:3038

Notes
- The E2E seed endpoints require x-e2e-seed-secret matching E2E_SEED_SECRET.
- Emails are injected into the DB as processed_emails (no S3 needed for local E2E).
- In AWS production ingestion, SES -> S3 -> Lambda parses + writes DB; summarization happens in code that calls OpenAI (see hubduck-backend/lambda.js and lamda/*.js).
