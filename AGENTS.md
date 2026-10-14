# Agent Workflow

## Model roles

- Use GPT-6 Luna as the primary agent for planning and implementation.
- Use Claude Haiku as the independent reviewer and, when needed, the follow-up implementer.
- Use only these models for this project when the available agent tooling supports them. Do not silently substitute a different model.

## Before implementation

1. GPT-6 Luna drafts a concise plan for every user request.
2. Claude Haiku independently reviews the plan for missing requirements, risks, and simpler approaches.
3. Revise the plan based on the review and repeat until both agents explicitly agree it addresses the request.
4. If the agents cannot reach agreement, or either model is unavailable, do not claim consensus; explain the blocker and ask the user how to proceed.

## Implementation and review

1. GPT-6 Luna implements the agreed plan.
2. Claude Haiku reviews the changes against the request, the plan, and relevant project behavior. It should identify concrete issues, not make changes when none are needed.
3. If changes are needed, Claude Haiku makes the smallest necessary corrections, then GPT-6 Luna reviews those changes.
4. Repeat review and correction until both agents explicitly agree the implementation is correct and the relevant checks pass.
5. Do not claim both agents agree unless each has actually reviewed and confirmed the result. If a review cycle cannot be completed, report that clearly.

Keep plans and reviews proportionate to the task. Avoid parallel edits to the same files; hand off implementation and review sequentially.
