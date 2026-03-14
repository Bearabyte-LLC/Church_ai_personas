# Engineering Rules — Definition of Done & Quality Gates

These rules apply to every engineering persona on the Church AI project. No story is considered complete until every applicable gate is satisfied.

---

## Universal Definition of Done (All Engineers)

Every engineer must confirm **ALL** of the following before marking work as done:

1. **Code Complete** — All acceptance criteria from the story are implemented.
2. **Self-Reviewed** — The engineer has reviewed their own code for correctness, readability, and adherence to project standards.
3. **No Regressions** — Existing tests continue to pass; no functionality has been broken.
4. **Unit Tests Written** — New or changed logic has corresponding unit tests with meaningful assertions.
5. **Integration Points Verified** — Any integration with other services, APIs, or modules has been tested end-to-end in a local or staging environment.
6. **Documentation Updated** — Relevant README files, API docs, inline comments, or architectural decision records are updated if the change affects them.
7. **Security Reviewed** — No secrets committed, no injection vulnerabilities introduced, auth/authz enforced where required.
8. **Linting & Formatting** — Code passes all linting rules and follows the project's formatting standards with no warnings.
9. **Build Succeeds** — The project builds successfully with no errors.
10.   **Branch Is Clean** — Commit history is meaningful, branch is rebased on latest main, and there are no merge conflicts.

---

## Role-Specific Definition of Done

### Architect

- Solution design documented and shared with the team before implementation begins.
- Non-functional requirements (performance, scalability, security) are addressed.
- Technology choices are justified with rationale recorded.
- Cross-service interfaces and contracts are defined.

### UI/UX Engineer

- Designs are responsive across target breakpoints (mobile, tablet, desktop).
- Accessibility standards met (WCAG 2.1 AA minimum).
- Design tokens and component library are used consistently.
- Visual regression tests pass or are updated with approval.
- User flows validated against pastor/user persona expectations.

### Full Stack Senior Developer

- All Universal DoD items met.
- Code reviewed by at least one peer (or Architect).
- Feature flag implemented if the feature is not ready for full release.
- Performance impact assessed — no unnecessary re-renders, N+1 queries, or blocking calls.
- Mentoring: any patterns introduced are documented for the team.

### Full Stack Backend Engineer

- API contracts match the agreed specification (OpenAPI/Swagger or equivalent).
- Database migrations are reversible and tested.
- Error handling returns appropriate HTTP status codes and messages.
- Rate limiting, input validation, and auth middleware applied where needed.
- Logging added for critical paths.

### Cloud Engineer

- Infrastructure changes defined as code (Terraform, CloudFormation, Pulumi, etc.).
- Cost impact assessed for new resources.
- IAM / permissions follow least-privilege principle.
- Disaster recovery and backup strategy confirmed for any new data stores.
- Changes tested in a staging/dev environment before production.

### DevOps Engineer

- CI/CD pipeline updated and all stages pass (build, test, security scan, deploy).
- Deployment is automated with rollback capability.
- Monitoring and alerting configured for new services or endpoints.
- Secrets managed through a secrets manager — never in code or config files.
- Runbook updated for any new operational procedures.

### AI Engineer

- Model inputs/outputs validated and sanitized.
- Prompt templates versioned and stored outside application code.
- Guardrails in place for LLM outputs (content filtering, hallucination checks).
- Pipeline performance benchmarked (latency, token usage, cost).
- Fallback behavior defined for when AI services are unavailable.

### Database Engineer

- Schema changes are backward-compatible or migration path is documented.
- Indexes reviewed for query performance.
- Data integrity constraints enforced at the database level.
- Backup and restore procedures verified for any new tables/collections.
- Sensitive data encrypted at rest and in transit.

### Mobile Engineer

- Tested on target devices/emulators (iOS and Android minimum set).
- Offline behavior handled gracefully.
- App permissions requested only when needed and justified.
- Push notification flows tested end-to-end.
- App size and startup performance within acceptable thresholds.

### Testing Engineer

- Test plan created covering positive, negative, edge, and boundary cases.
- Automated tests added to the CI pipeline.
- Test coverage meets or exceeds the project threshold (target: 80%+).
- Performance/load tests written for critical user paths.
- Test data management strategy defined (fixtures, factories, seeding).

---

## QA Engineer — Final Quality Gate

The QA Engineer is the last gate before stakeholder review. They verify:

1. **Story Completeness** — Every acceptance criterion is demonstrably met.
2. **DoD Compliance** — The engineer's role-specific DoD items are all satisfied.
3. **Tests Pass** — All automated tests (unit, integration, e2e) pass in CI.
4. **Manual Verification** — The feature works as expected in a staging environment through hands-on testing.
5. **Cross-Browser / Cross-Device** — Frontend changes verified on supported browsers and devices.
6. **Edge Cases** — Unusual inputs, empty states, error states, and boundary conditions are handled.
7. **Data Integrity** — Data created/modified by the feature is consistent and correct.
8. **No Regressions** — Related features still work correctly.
9. **Performance Acceptable** — No noticeable degradation in load times or responsiveness.
10.   **Ready for Stakeholder Review** — QA confirms the work is genuinely done and ready for pastor/user validation.

> **The QA Engineer must reject work that does not meet these criteria.** Work is returned to the responsible engineer with specific, actionable feedback.

---

## Stakeholder Validation Gate

After QA approval, the following stakeholders validate the work:

### Fundamental Baptist Pastor

- Confirms the feature aligns with the church's mission, values, and theological standards.
- Verifies the language, tone, and content are appropriate and doctrinally sound.
- Tests the feature from the perspective of a pastor managing a congregation.
- Signs off that the feature meets their stated requirements.

### User Personas (Church Member / Visitor)

- Confirms the feature is intuitive and easy to use.
- Verifies it solves the need it was designed for.
- Reports any confusion, friction, or unexpected behavior.

### Product Owner

- Final acceptance that the story is complete.
- Confirms alignment with the product roadmap and priorities.
- Closes the story.

---

## Workflow Summary

```
Engineer completes work → Self-review against DoD
    ↓
Testing Engineer → Automated test coverage confirmed
    ↓
QA Engineer → Full validation (story, DoD, tests, manual QA)
    ↓ (reject → back to engineer with feedback)
Pastor / Users → Stakeholder validation
    ↓ (reject → back to QA/engineer with feedback)
Product Owner → Story accepted & closed
```
