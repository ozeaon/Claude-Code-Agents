# Ozeaon Agent Policy

> Applies to **assigned Ozeaon / OCIS engineering tasks** — work dispatched through the Ozeaon Task Manager or delegated by Claude PM. This rule does not apply to non-Ozeaon repositories.

## Canonical policy and retrieval

- The **AI agent delegation and coordination policy** is authored in `ozeaon/engineering-agent-skills` (skill `oz-agent-delegation-policy`). That repository is the authoritative source. No other copy — including any `status: draft` document (such as the earlier `ozeaon/knowledge-portal` docs draft) — is approved operating policy.
- Approved retrieval is through the **Knowledge Portal**: its approved-skills channel serves the Owner-approved revision, pinned to a reviewed commit of `ozeaon/engineering-agent-skills`. Retrieve the policy through the Portal rather than guessing which repository revision is approved. Fail closed: never bypass the Portal's access model, and never treat a draft, paraphrase or remembered copy as approved.

## Pre-Task Check

1. **Retrieve the approved policy first.** Before starting any assigned Ozeaon/OCIS engineering task, read the approved revision of the policy through the Knowledge Portal. Anything still marked `requestReview`, `draft` or otherwise unapproved is reading material, never an approved basis for work.
2. **If the Knowledge Portal is unavailable**, or the approved revision is not yet retrievable through it:
   - **Permitted:** read-only activities — reading, research, inspection, planning, review support and other work that commits no implementation.
   - **Blocked:** implementation that requires the approved policy context (code changes on assigned tasks). Record the retrieval blocker on the task ticket and wait for the approved context; do not implement from a draft, a paraphrase or memory.
3. **Confirm the task record.** Assignments and status tracking come from the Ozeaon Task Manager. Search for the existing ticket before creating one; never duplicate tickets or build parallel tracking systems. If an assigned task has no ticket, record one before implementation.
4. **Apply the mandatory stop condition.** The policy's operative rule, quoted verbatim:

   > If an issue is discovered that is outside the assigned scope and does not prevent completion of the original task, stop investigating that issue. Record it briefly, report it to Claude PM or the task owner, and continue the original assignment.

   Never debug, refactor or change infrastructure for out-of-scope issues; never re-investigate an issue already classified as non-blocking; never modify production systems to investigate an unrelated issue. If repeated attempts fail without producing new evidence, stop and escalate rather than continuing speculative fixes.
5. **Finish with evidence.** A task is complete only when its acceptance criteria are satisfied and supporting evidence is recorded on the ticket: commits, pull requests, tests and verification results. Implementation completion is not production deployment; deployment requires its own explicit authorization.
