# LeadRescue — Revenue Recovery CRM

**Catch the leads your team forgets. Follow up on every quote. See where sales are slipping away.**

LeadRescue is an early-stage, industry-focused product built on the open-source BottleCRM foundation. Our first hypothesis is that home-service businesses lose profitable work when inbound inquiries and quotes do not receive timely, consistent follow-up.

This repository is the working product, not a claim that the recovery features are already complete. We are validating the problem with real businesses before promising revenue results or charging for features that are not ready.

## The problem we are testing

A business can pay for advertising, receive a quote request, and still lose the job because the lead was not answered, the quote was not followed up, or nobody owned the next step. Existing CRMs can store the record, but a record alone does not ensure the right person acts on it.

**Initial customer hypothesis:** small-to-medium home-service companies (starting with renovation and HVAC contractors) that handle valuable inbound inquiries and quotes.

We will validate this with customer interviews and paid pilots before locking the product to one vertical.

## Product direction

### Built on the existing BottleCRM foundation
- Lead, contact, account, opportunity, task and activity management
- Sales pipeline and deal tracking
- Invoices, tickets, and a documented API
- Existing web app, backend and mobile app from the upstream project

### LeadRescue features to build and verify
- **Follow-up queue:** highlight leads and quotes that have no next step or have passed their follow-up date.
- **Response-time tracking:** record how quickly inquiries receive a first response when the data is available.
- **Next-action reminders:** assign an owner and due date to each open lead; make overdue work visible.
- **Quote recovery workflow:** create a repeatable follow-up sequence for quotes that have not received a response.
- **Revenue recovery dashboard:** distinguish pipeline value, won revenue, and estimated opportunities; never label an estimate as recovered revenue.
- **Audit-friendly reporting:** show what was contacted, when, by whom, and what happened next.

These items are a roadmap, not a statement that they are implemented today. Automatic customer messaging, email/WhatsApp integrations, and AI-written replies must be added, tested, and configured safely before being advertised.

## Our first validation plan

1. Interview 10 owners or sales managers in the target niche.
2. Ask how inquiries arrive, how quotes are followed up, and what happens when staff are busy.
3. Estimate the cost of missed follow-up using their real numbers—not generic industry claims.
4. Offer a clearly scoped paid pilot to businesses that confirm the problem.
5. Track baseline and pilot outcomes. Continue only if customers use the workflow and can see measurable value.

## Commercial model to test

- One-time setup, pipeline configuration and data import
- Monthly fee for managed workflows, reporting and support
- Later: standardized hosted software subscription if multiple customers need the same workflow

Pricing will be tested with customers. No savings, conversion uplift, or revenue recovery is guaranteed.

## Development principles

- Build the smallest feature that addresses a verified customer problem.
- Preserve tenant isolation and permissions; never weaken security to make a demo easier.
- Do not send messages to customers without the business's authorization and appropriate consent.
- Keep credentials and customer data out of source control.
- Test all changes and document deployment before using real customer data.
- Keep estimates clearly separated from realized revenue.

## Technical foundation and attribution

LeadRescue is a modified working fork of [BottleCRM / Django-CRM](https://github.com/Django-CRM/Django-CRM), which uses Django REST Framework, SvelteKit, Flutter and PostgreSQL. Upstream project and contributor notices remain applicable. The upstream repository is MIT licensed; see [LICENSE](LICENSE) and preserve the required copyright and permission notice in redistributions.

For the inherited application's original installation instructions and architecture, see the upstream project's documentation and the local `docs/` directory. This fork's LeadRescue-specific scope and roadmap are documented in [PRODUCT_PLAN.md](PRODUCT_PLAN.md).

## Current status

**Early build / validation stage.** The repository has been forked and branded for the LeadRescue direction. The customer problem, target niche, and proposed recovery workflows still need validation and implementation. Do not use this as a production service with real customer data until deployment, security, backup, privacy, and workflow tests are complete.
