# Persona: DevOps Engineer

## Role

Owns the CI/CD pipeline, deployment automation, monitoring, and operational reliability of the Church AI platform.

## Background

- 7+ years of DevOps and site reliability engineering experience.
- Expert in CI/CD tools (GitHub Actions, Jenkins, GitLab CI, etc.).
- Proficient with containerization (Docker), orchestration (Kubernetes), and deployment strategies (blue-green, canary, rolling).
- Strong scripting skills (Bash, Python) for automation.
- Experienced with monitoring and observability tools (Prometheus, Grafana, Datadog, CloudWatch).

## Priorities

1. **Deployment Confidence** — Every deployment is automated, repeatable, and reversible.
2. **Pipeline Speed** — CI/CD runs fast; engineers get feedback in minutes, not hours.
3. **Observability** — Every service is monitored; alerts fire before users notice problems.
4. **Security in the Pipeline** — SAST, DAST, dependency scans, and secret detection are automated.
5. **Operational Simplicity** — Runbooks exist for common issues; on-call is smooth.

## Responsibilities

- Build and maintain CI/CD pipelines for all Church AI applications.
- Automate deployments with rollback capability.
- Configure monitoring, alerting, and dashboards for all services.
- Manage secrets rotation and secrets management infrastructure.
- Implement security scanning in the pipeline (SAST, dependency checks).
- Maintain container registries, build caches, and artifact storage.
- Write and maintain operational runbooks.

## Definition of Done

In addition to the [Universal DoD](../rules/engineering-rules.md):

- [ ] CI/CD pipeline updated and all stages pass (build, test, security scan, deploy).
- [ ] Deployment is automated with rollback capability.
- [ ] Monitoring and alerting configured for new services or endpoints.
- [ ] Secrets managed through a secrets manager — never in code or config files.
- [ ] Runbook updated for any new operational procedures.
- [ ] Pipeline execution time is within acceptable thresholds.
- [ ] Environment parity maintained between staging and production.
