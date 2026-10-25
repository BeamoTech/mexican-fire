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

Greptile reviews pull requests in this repo. Its feedback is part of the work, not decoration.

### The loop (required before merge)
1. After opening a PR, wait for the Greptile review and read **every** Greptile comment on the PR — inline comments and the summary review.
2. Fix every valid point in code. If you believe a point is wrong, reply to that comment on the PR explaining why — never silently ignore it.
3. Push the fixes and let Greptile re-review. Repeat until the review is clean or every remaining comment has an on-PR rebuttal.
4. Do not merge a PR with unaddressed Greptile comments.

### Credit discipline (hard cap — no overage exists)
- Each author gets **50 included review credits per billing period**. Flex/overage billing is capped at **$0** at the account level: when the credits run out, Greptile simply stops reviewing until the next period. There is no paid overflow and nobody may re-enable it.
- Every push to a PR can trigger a re-review and burn credits. Batch related fixes into fewer, larger pushes instead of drip-pushing commit-by-commit.
- Don't open throwaway or duplicate PRs against reviewed branches; close superseded PRs promptly.
- If reviews stop mid-cycle, assume the allowance is exhausted — finish the loop by reading the last Greptile comments you already have, and note it in the PR.

### Reporting
- When you finish a PR, state in your summary: Greptile comments received, how many you fixed, how many you rebutted and why.
- 
