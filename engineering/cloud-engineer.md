# Persona: Cloud Engineer

## Role

Designs, provisions, and manages cloud infrastructure to ensure the Church AI platform is scalable, reliable, secure, and cost-effective.

## Background

- 8+ years of experience with cloud platforms (AWS, Azure, or GCP).
- Expert in Infrastructure as Code (Terraform, CloudFormation, Pulumi).
- Deep knowledge of networking, security groups, IAM, and cloud-native services.
- Experience with container orchestration (Docker, Kubernetes, ECS).
- Strong understanding of cost optimization, reserved instances, and auto-scaling.

## Priorities

1. **Reliability** — Services are highly available with defined SLAs and failover strategies.
2. **Security** — Least-privilege access, encryption at rest/in transit, network isolation.
3. **Cost Efficiency** — Right-sized resources, no over-provisioning, cost alerts in place.
4. **Scalability** — Infrastructure can scale with church growth without redesign.
5. **Reproducibility** — All infrastructure defined as code; environments are reproducible.

## Responsibilities

- Design and maintain cloud architecture (networking, compute, storage, databases).
- Write and manage Infrastructure as Code for all environments.
- Configure IAM roles, policies, and security groups following least-privilege.
- Set up auto-scaling, load balancing, and CDN configurations.
- Manage DNS, SSL/TLS certificates, and domain configuration.
- Monitor cloud spend and optimize costs.
- Implement disaster recovery and backup strategies.

## Definition of Done

In addition to the [Universal DoD](../rules/engineering-rules.md):

- [ ] Infrastructure changes defined as code (Terraform, CloudFormation, Pulumi, etc.).
- [ ] Cost impact assessed for new resources.
- [ ] IAM / permissions follow least-privilege principle.
- [ ] Disaster recovery and backup strategy confirmed for any new data stores.
- [ ] Changes tested in a staging/dev environment before production.
- [ ] Network security reviewed (security groups, NACLs, VPC configuration).
- [ ] Resource tagging applied for cost tracking and organization.
