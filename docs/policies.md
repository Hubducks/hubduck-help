---
layout: default
title: Policy Management
nav_order: 6
---

# Policy Management

HubDuck helps schools create, publish, deliver, and track compliance on official policies that require staff acknowledgment.

---

## Why use HubDuck for policies?

Before HubDuck, a principal emails a policy document to staff and hopes they read it. There's no way to know who actually read it, who acknowledged it, or who needs a reminder. During a Whole-School Evaluation, the principal scrambles to prove compliance.

With HubDuck:
- Every policy has a clear lifecycle (Draft → Published → Delivered → Archived)
- Staff must explicitly acknowledge each policy
- The principal sees exactly who has acknowledged and who hasn't
- Reminders can be sent to specific people
- Compliance percentages update in real time

---

## Creating a policy

### Step 1: Go to Policies

Click **Policies** in the admin sidebar. You'll see a list of all policies with their status, category, deadline, and compliance percentage.

### Step 2: Click "Create Policy"

The creation dialog has four sections:

#### What is this policy?

- **Title** — Give it a clear name (e.g., "Child Safeguarding Statement 2026", "Anti-Bullying Policy Review")
- **Description** — Summary of what the policy covers and why staff need to read it
- **Source** — Where the policy comes from:
  - Department of Education
  - Board of Management
  - Internal (school-generated)
  - HSE
  - Tusla
  - Other
- **Category** — What type of policy:
  - General
  - Safety
  - Safeguarding
  - Attendance
  - Curriculum
  - Code of Conduct
  - Health
  - Data Protection

#### What must people do?

- **Action type** — What you're asking staff to do:
  - **Read and Acknowledge** — read the policy and confirm they've done so
  - **Sign and Return** — read, sign, and return a physical or digital copy
  - **Take Action** — do something specific (describe in the action description field)
- **Deadline** — When acknowledgment is due by

#### Attachments

Upload the actual policy document (PDF, Word, etc.). Up to 5 files. Staff will be able to download these when reviewing the policy.

#### Who receives this?

- **Select duck** — Which duck's subscribers should receive this policy
- **Target roles** — Which roles must acknowledge:
  - Teachers
  - Parents & Guardians
  - School Admin

### Step 3: Save as Draft

The policy is created in **Draft** status. It's not visible to staff yet. You can edit it, add attachments, or change the deadline before publishing.

---

## The policy lifecycle

```
DRAFT → PUBLISHED → DELIVERED → ARCHIVED
```

### Draft

The policy exists but is not visible to anyone except admins. Use this stage to:
- Review the wording
- Upload attachments
- Get Board approval before publishing
- Set the correct deadline

### Published

The policy is approved and ready for delivery. Publishing doesn't send it to anyone yet — it marks it as "approved and ready."

To publish: click the **Publish** button on a Draft policy.

### Delivered

The policy has been sent to staff. Each target member gets a `policy_acknowledgment` record with status PENDING. The policy appears in their duck inbox.

To deliver: click the **Deliver** button on a Published policy. Choose:
- **Include in next digest** — policy appears in the next scheduled digest email
- **Send immediately** — sends right away via email

### Archived

The policy is no longer active. Completed policies can be archived to keep the list clean. Archived policies retain their compliance data for audit purposes.

To archive: click **Archive** on a Delivered policy (only after delivery).

---

## Creating a policy from an email

If you receive an email about a policy (e.g., a DES circular about child protection), you can create a policy directly from it:

1. Open the email in the duck inbox
2. Click the **🛡 Policy** icon at the bottom of the email card
3. HubDuck creates a Draft policy pre-filled with the email subject and summary
4. Edit the title, category, deadline, and target roles as needed
5. Publish and deliver when ready

This is the fastest way to turn an incoming communication into a tracked obligation.

---

## Tracking compliance

### The compliance dashboard

Go to **Policies** — the top of the page shows four summary cards:
- **Active Policies** — how many are currently in PUBLISHED or DELIVERED status
- **Overall Compliance** — percentage of staff who have acknowledged across all active policies
- **Overdue Users** — staff who haven't acknowledged past the deadline
- **Needs Attention** — policies with low compliance that need a nudge

### Per-policy compliance

Click on any Delivered policy to see detailed compliance:
- **Total** — how many staff are expected to acknowledge
- **Acknowledged** — how many have done so (with date/time)
- **Pending** — who hasn't acknowledged yet
- **Overdue** — who is past the deadline

You can filter by status (Acknowledged / Pending / Overdue) to quickly find who needs attention.

### Sending reminders

From the compliance detail page:
1. Check the boxes next to the staff members who need a reminder
2. Click **Send Reminders**
3. Each selected person receives an email reminder with a link to the policy

Or click **Send to All Pending** to remind everyone who hasn't acknowledged.

---

## Measuring results

### What the numbers mean

| Metric | What it tells you |
|--------|------------------|
| **100% compliance** | Every staff member has acknowledged — you're covered for inspection |
| **High compliance (80%+)** | Most staff have responded — send reminders to the remaining few |
| **Low compliance (<50%)** | Most staff haven't responded — consider resending or raising at staff meeting |
| **0% compliance** | Nobody has acknowledged — check if the policy was actually delivered |

### Using compliance data for inspections

During a Whole-School Evaluation (WSE), inspectors check that:
- Schools have mandatory policies in place
- Staff are aware of and have acknowledged key policies (especially child protection)
- There's evidence of compliance

HubDuck provides this evidence automatically:
- **Who acknowledged** — name, email, date/time
- **When they acknowledged** — timestamp for each person
- **Overall percentage** — compliance rate at any point in time
- **Reminder history** — how many reminders were sent

Export this data as evidence for the inspector.

---

## Nudging and follow-up

### When to nudge

- **3 days before deadline** — send a gentle reminder to pending staff
- **On deadline day** — send an urgent reminder to anyone still pending
- **1 day after deadline** — flag as overdue, escalate if needed

### How to nudge effectively

1. **First nudge** (automated via digest) — the policy appears in the weekly digest with a deadline badge
2. **Second nudge** (manual reminder) — use the "Send Reminders" button on the compliance page
3. **Third nudge** (in person) — mention at the next staff meeting: "3 people still haven't acknowledged the safeguarding policy"

### Tips for high compliance

- **Set realistic deadlines** — give staff at least 5 working days
- **Include context** — explain in the description WHY this matters (e.g., "inspectors check this")
- **Keep it short** — link to the full document, but make the acknowledgment itself one-click
- **Follow up quickly** — the longer you wait, the lower your compliance rate

---

## Mandatory school policies (Ireland)

Irish primary schools must have these policies in place. Department inspectors specifically check compliance during whole-school evaluations:

| Policy | Requirement |
|--------|------------|
| **Admissions Policy** | Must be fair, transparent, and Board-approved. Published on school website. |
| **Child Safeguarding Statement** | Required by Children First Act 2015. Inspectors check compliance seriously. |
| **Code of Behaviour** | Required under Education (Welfare) Act. Board must ensure it's in place. |
| **Anti-Bullying Policy** | Must follow DES Anti-Bullying Procedures (2013). Annual review required. |
| **Health & Safety Statement** | Governance Manual requirement. Board responsible for ensuring it's in place. |

**Tip:** Create all five in HubDuck at the start of each school year, deliver them to all staff, and track acknowledgment. When the inspector arrives, you can show 100% compliance in seconds.

---

## Use cases

### New school year setup

1. Create policies for all 5 mandatory areas
2. Attach the latest documents
3. Set deadline: 2 weeks into term
4. Deliver to all staff
5. Monitor compliance weekly
6. Send reminders to stragglers

### Mid-year policy update

1. A DES circular arrives updating child protection procedures
2. Forward the email to HubDuck
3. Click 🛡 to create a policy from the email
4. Update the title and deadline
5. Deliver to affected roles
6. Track acknowledgment

### Board meeting preparation

1. Go to Policies → filter by PUBLISHED
2. Note compliance percentages for each
3. Present to the Board: "Safeguarding: 100%, Anti-Bullying: 93%, Code of Behaviour: under review"
4. The Board has evidence of governance

### Inspection readiness

1. Filter policies by category: Safeguarding
2. Show the inspector: "15/15 staff acknowledged on [date]"
3. Download acknowledgment list with timestamps
4. Inspector sees evidence of compliance

---

## Need help?

Contact us at [support@hubduck.net](mailto:support@hubduck.net)
