# LeadRescue Night Shift

## Current implementation status

The first cloud-only layer is scheduled CI verification. It runs on GitHub-hosted runners, so your computer does not need to be on.

- Schedule: daily at 01:00 UTC (GitHub may delay scheduled jobs during busy periods).
- Manual run: GitHub Actions → CI → Run workflow.
- Checks: the existing backend, PostgreSQL/RLS, frontend, package-build, and documentation checks in `.github/workflows/tests.yml`.
- Safety: this workflow tests code only. It does not merge pull requests, deploy to Render, message customers, or change production settings.

## Important: this is not yet an autonomous AI coder

The repository currently has connected GitHub and Render integrations in the ChatGPT/Composio environment, but that does not give a GitHub Actions runner a persistent ChatGPT brain or an AI model endpoint. No compatible AI provider is configured for this runner yet, so this commit deliberately does not pretend that AI code generation is configured.

To enable an AI coding step while keeping spend at $0, a compatible provider with a currently available free API quota must be selected and its credential stored as a GitHub Actions repository secret. Free quotas can change or run out; the agent must stop safely when unavailable. Do not commit credentials to the repository. Do not enable paid overages.

## Intended next phase

1. Pick a model provider that has an available free API tier and is permitted for the account holder.
2. Add the provider token as a repository secret; never paste it into an issue or source file.
3. Implement a tightly scoped agent job that works only on a new branch and one queued task per run.
4. Run relevant tests and publish a draft pull request with logs and a summary.
5. Require human approval for merging or deploying. Never auto-merge or deploy.

## How to check the first layer

1. Open the repository's **Actions** tab.
2. Select **CI** and choose **Run workflow** to test the new manual trigger.
3. Inspect every job result and its logs. A successful workflow means the test suite passed for that commit; it does not prove production deployment or customer workflows are ready.
