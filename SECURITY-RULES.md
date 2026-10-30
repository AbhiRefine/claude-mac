# Security rules (this repo is PUBLIC)

Everything here is visible to anyone: files, git history, Actions logs and artifacts. History can't be taken back once pushed.

## Never commit, post or log
- Passwords, tokens, API keys, OAuth secrets, VNC passwords, sign-in or one-time codes
- Tailnet IPs (100.x.x.x), hostnames, device names
- Emails, account names, people's names, customer or company data
- Internal URLs, product code, internal chat or ticket text
- Screenshots, recordings, transcripts or notes from test sessions
- Coordination boards, handoff notes, test results

## Only these live here
- The Mac session workflow, this file, the README, and the guard script.
- Everything private goes in **repo secrets** (Settings → Secrets → Actions) or stays on the owner's PC.

## Before every commit
`sh .githooks/pre-commit` runs automatically (`git config core.hooksPath .githooks`). Any hit blocks the commit. If unsure, don't push.

## Workflow
- Only `workflow_dispatch`, by the repo owner. No PR or schedule triggers.
- No artifacts uploaded. Secrets and derived values are masked, never echoed, no `set -x`.
- One session at a time, wiped on exit.
