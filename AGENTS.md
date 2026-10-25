# Mexican Fire — agent guide

`AGENTS.md` is the canonical project guide. Read `~/dev/AGENTS.md` for workspace
safety, CI cost and storage rules when available.

Static marketing pages live in `public/`; contact handling is in `functions/`.
Read `README.md`, `package.json` and `wrangler.jsonc` before relevant changes.

- Preserve brand copy, accessible page navigation and server-side secret
  boundaries. Contact submissions and production delivery require safe fixtures.
- `npm run dev` serves the local Pages preview on port 8787. Run commands inside
  this repository; install dependencies only when the task requires them.
- `npm run deploy` publishes `public/` to Cloudflare Pages. A guide edit does not
  authorize deployment, real contact messages or credential changes. Inspect
  any Git deployment integration before a production-bound push.
- Review the Markdown diff and run `git diff --check` for guide-only work.
  Runtime changes need applicable local HTML/function/browser checks and the
  existing release gate; do not invent a test pass or add routine hosted CI.
- Fetch current refs, preserve shared work, stage explicit owned paths and use
  normal pushes. Never commit secrets, local runtime state or generated caches.

<!-- BEGIN BEAMO UNFINISHED WORK -->
## Unfinished work

- Read the project's unfinished work record at task start. Use its existing
  canonical backlog, or `.ai/memory/unfinished-work.md` if none exists; link
  the record from `.ai/memory/MEMORY.md` when creating it. Chat is not storage.
- Always save every incomplete requested item, deferred issue, blocked check
  and pending merge/release step as they arise and before ending, pausing,
  handing off or changing tasks. Checkpoint after meaningful progress.
- Each item needs an ID/status, remaining acceptance criteria, exact next
  action, blockers/required approval, date/author, repo/branch/commit/worktree
  and relevant files or links. Separate completed checks and their evidence
  from failed, skipped and unrun checks; distinguish local, pushed and deployed
  state. Preserve partial source work without staging another agent's changes.
- Resume from the record, recheck current source and evidence, and update or
  mark items done only when their acceptance criteria pass. Record reasons for
  canceled/superseded items. Preserve useful history and others' entries; reread
  before editing and append separate items when concurrent work would overwrite
  them.
- Never store credentials or raw personal/customer records. Notes do not grant
  approval or prove deployment. If project writing is blocked, save a durable
  workspace handoff with the exact project/ref, record the blocker, and report
  its location before stopping; do not silently lose unfinished work.
<!-- END BEAMO UNFINISHED WORK -->

## Greptile review rules

### Review before merge
1. Read every Greptile summary and inline comment for the PR, including earlier review rounds.
2. Fix each valid finding in the affected source. Reply to each disputed finding on the PR with evidence; never silently discard a finding.
3. Batch related fixes into one push where practical, then inspect the review for the final head. Repeat as needed and account for every finding.
4. Do not merge with unaddressed findings, failed required checks, or unresolved safety or release gates.

### When automated review is unavailable
- A missing first review or stopped review is not proof of exhausted credits. Check available installation permissions, repository settings, review triggers, service status and quota evidence; record the confirmed cause or say it remains unknown.
- Preserve and address all earlier findings. If automated review cannot complete, require an explicit independent review of the final diff against current main, with reviewer identity, exact head SHA, scope, evidence, findings and remaining limits recorded on the PR. If that review or a required check is unavailable, keep the PR blocked.

### Cost and reporting
- Do not assert numerical credit allowances, reset dates or account billing settings without current evidence. Do not enable paid overflow, buy credits or expand access to obtain a review.
- Avoid redundant review requests and duplicate PRs. Batch pushes without reducing verification.
- Report Greptile findings received, fixed and disputed with reasons, plus review availability, final head, checks performed and outstanding blockers.
- Preserve repository specific instructions, mirrored guides, formatting rules, production freezes and authorization boundaries. Review approval does not authorize deployment, live trading, sending messages or other external effects.
