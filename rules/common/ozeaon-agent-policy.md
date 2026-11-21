# Ozeaon Agent Policy

> Applies to **assigned Ozeaon / OCIS engineering tasks** — work dispatched through the Ozeaon Task Manager or delegated by Claude PM. This rule does not apply to non-Ozeaon repositories.

## Pre-Task Check

1. **Read the approved policy first.** Before starting any assigned Ozeaon/OCIS engineering task, read the *AI agent delegation and coordination policy* at its canonical, SHA-pinned location: [docs/ai-agent-delegation-and-coordination.md @ `fc72b51`](https://github.com/ozeaon/knowledge-portal/blob/fc72b5185dc92b2536ab1dfd9629ef090775fcff/docs/ai-agent-delegation-and-coordination.md). The canonical document is the single source of truth: never copy it into other repositories. When the policy is revised, re-pin this link to the new commit SHA.
2. **Confirm the task record.** Assignments and status tracking come from the Ozeaon Task Manager. Search for the existing ticket before creating one; never duplicate tickets or build parallel tracking systems. If an assigned task has no ticket, record one before implementation.
3. **Apply the mandatory stop condition.** The policy's operative rule, quoted verbatim:

   > If an issue is discovered that is outside the assigned scope and does not prevent completion of the original task, stop investigating that issue. Record it briefly, report it to Claude PM or the task owner, and continue the original assignment.

   Never debug, refactor or change infrastructure for out-of-scope issues; never re-investigate an issue already classified as non-blocking; never modify production systems to investigate an unrelated issue. If repeated attempts fail without producing new evidence, stop and escalate rather than continuing speculative fixes.
4. **Finish with evidence.** A task is complete only when its acceptance criteria are satisfied and supporting evidence is recorded on the ticket: commits, pull requests, tests and verification results. Implementation completion is not production deployment; deployment requires its own explicit authorization.

## Retrieval

The canonical policy lives in the private `ozeaon/knowledge-portal` repository and requires appropriate GitHub access. If you cannot read the canonical document, report the access blocker on the task ticket instead of working from memory, a paraphrase or a stale copy.
