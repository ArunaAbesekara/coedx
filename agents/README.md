# Virtual Software Team (Codex Agents)

This package defines a practical multi-agent setup for your stack:
- **Frontend:** React JS
- **Backend:** Java 21
- **Database:** PostgreSQL

## Team Roles
1. Architect Agent
2. Backend Developer Agent
3. Frontend Developer Agent
4. QA Agent
5. Code Reviewer Agent
6. Security Agent
7. CI/CD Pipeline Agent

## Suggested Execution Order
1. Architect creates the implementation plan and acceptance criteria.
2. Backend and Frontend agents implement in parallel from the same contract.
3. QA agent writes and executes test plans.
4. Code Reviewer and Security agents review generated changes.
5. CI/CD agent updates and validates pipeline rules.

## How to Use
Use each prompt file in `agents/prompts/` as the system prompt (or first instruction block) for a dedicated Codex run.

For each task:
1. Share the same product requirement with all agents.
2. Keep artifacts under feature folders (design docs, API contracts, test evidence).
3. Require each agent to output:
   - Summary of work
   - Changed files
   - Risks
   - Next handoff target

See `agents/workflows/feature-delivery-playbook.md` for a full handoff model.
