# LeadRescue product plan

## Mission
Help service businesses reduce preventable sales leakage caused by missed inquiries, forgotten quote follow-ups, and unclear ownership of the next action.

## Initial ideal customer profile (hypothesis)
Home-service businesses with a steady stream of inbound leads and relatively high-value jobs. Test renovation contractors and HVAC companies first; do not assume this niche is validated until owners confirm pain and willingness to pay.

## Core job to be done
"When an inquiry or quote is still open, tell the right person exactly what needs to happen next, make the follow-up easy, and show the outcome."

## MVP requirements
1. Lead/quote follow-up status and due date.
2. Owner for each lead and a visible overdue queue.
3. Configurable follow-up tasks, initially manual or task-based rather than automatic outbound messaging.
4. Dashboard with new leads, overdue follow-ups, quotes awaiting a response, won/lost outcomes, and recorded deal value.
5. Clear reporting definitions: pipeline value is not revenue; estimated recovery is not realized recovery.
6. CSV import/export and an audit trail for changes.
7. Permission checks and tenant isolation for every new record and report.

## Later, only after customer validation
- Email/calendar integrations.
- Approved WhatsApp or SMS integration where legal and provider terms permit.
- Configurable automation rules and human approval before sending.
- AI-assisted draft replies with human review.
- Attribution and cohort reporting where data quality supports it.

## Validation gates
- Gate 1: 10 interviews; at least 5 independently describe the same costly follow-up failure.
- Gate 2: 2 businesses agree to a paid pilot with a defined success metric.
- Gate 3: pilot users consistently use the workflow and the measured result supports continued payment.
- Gate 4: standardize delivery and pricing only after retention evidence.

These are internal decision thresholds, not market facts or guaranteed outcomes.

## Metrics
- Median first-response time (only where timestamps are reliable).
- Share of open leads with an assigned owner and next action.
- Overdue follow-ups.
- Quote follow-up completion.
- Lead-to-won conversion, with a defined denominator and period.
- Won revenue recorded in the CRM.
- Customer retention, support time, and gross margin.

## Out of scope for the first MVP
- Generic AI chatbot.
- Unreviewed automated mass messaging.
- Claims that the software guarantees sales or recovered revenue.
- Rebuilding the entire CRM before verifying the follow-up workflow.

## Risks and safeguards
- **Wrong niche:** validate with interviews and paid pilots.
- **Poor data quality:** show missing data; do not invent attribution.
- **Spam or privacy risk:** customer authorization, consent, provider terms, and applicable law must be checked before outbound integrations.
- **Tenant leakage:** tests must confirm users cannot access other organizations' data.
- **Open-source obligations:** preserve upstream MIT notices and review dependencies and assets before commercial redistribution.
