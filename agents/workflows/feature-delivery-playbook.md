# Feature Delivery Playbook for Multi-Agent Codex Team

## 1) Architect Agent Output (first)
Must produce:
- Context and assumptions
- C4-lite architecture notes (component-level)
- API contracts (request/response + error model)
- DB migration strategy for PostgreSQL
- Non-functional requirements (security, observability, performance)
- Implementation slices for backend/frontend
- Definition of Done and acceptance criteria

## 2) Backend + Frontend Development (parallel)
Backend agent owns:
- Java 21 service implementation
- Validation and business rules
- Repository/service/controller separation
- SQL migrations and indexes
- Unit/integration tests

Frontend agent owns:
- React component/state architecture
- API service integration
- Error/loading UX
- Form validation
- UI tests

## 3) QA Agent
QA agent produces:
- Test plan mapped to acceptance criteria
- Positive/negative/API/UI/edge test scenarios
- Regression matrix
- Test evidence and defect reports

## 4) Code Reviewer Agent
Code reviewer focuses on:
- Correctness and maintainability
- Readability and duplication
- API contract consistency
- Test quality and missing edge cases

## 5) Security Agent
Security review checks:
- Input validation and output encoding
- Authentication/authorization boundaries
- Secrets/config handling
- SQL injection and dependency risk
- Logging and PII exposure

## 6) CI/CD Agent
Pipeline updates include:
- Build and test gates for frontend/backend
- Static analysis and security scan steps
- Migration checks and deployment stages
- Rollback strategy and release notes

## 7) Release Gate
Release only when:
- Acceptance criteria passed
- QA sign-off complete
- Security findings triaged
- CI pipeline green
