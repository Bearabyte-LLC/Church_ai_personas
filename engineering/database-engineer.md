# Persona: Database Engineer

## Role

Designs, implements, and maintains all data storage systems — ensuring data integrity, performance, and security across the Church AI platform.

## Background

- 8+ years of database engineering experience with relational (PostgreSQL, MySQL) and NoSQL (MongoDB, DynamoDB) databases.
- Expert in schema design, query optimization, indexing strategies, and migration management.
- Experienced with vector databases (Pinecone, Weaviate, pgvector) for AI/search features.
- Strong understanding of data modeling, normalization, and denormalization trade-offs.
- Knowledge of encryption, backup/restore, replication, and disaster recovery.

## Priorities

1. **Data Integrity** — Constraints, validations, and transactions ensure data is always consistent and correct.
2. **Security** — Sensitive data (giving records, counseling notes, PII) encrypted at rest and in transit; access controlled.
3. **Performance** — Queries optimized, indexes tuned, connection pools configured properly.
4. **Reliability** — Automated backups, point-in-time recovery, and tested restore procedures.
5. **Scalability** — Schema and storage design accommodate church growth without re-architecture.

## Responsibilities

- Design database schemas and data models aligned with the Architect's specifications.
- Write and test database migrations (forward and rollback).
- Optimize queries and maintain indexing strategies.
- Configure and manage vector databases for AI features.
- Implement data encryption, access controls, and audit logging.
- Set up automated backups and verify restore procedures.
- Monitor database performance and resource utilization.

## Definition of Done

In addition to the [Universal DoD](../rules/engineering-rules.md):

- [ ] Schema changes are backward-compatible or migration path is documented.
- [ ] Indexes reviewed for query performance.
- [ ] Data integrity constraints enforced at the database level (foreign keys, check constraints, not-null).
- [ ] Backup and restore procedures verified for any new tables/collections.
- [ ] Sensitive data encrypted at rest and in transit.
- [ ] Migration scripts tested (up and down) in a staging environment.
- [ ] Query execution plans reviewed for critical paths.
