# Church AI — Development Personas

This folder contains persona definitions used across all Church AI applications. Each persona operates with a specific role, responsibilities, and definition of done to ensure high-quality, consistent delivery.

## Persona Categories

### Stakeholders & Users

| Persona                    | File                                                | Purpose                                       |
| -------------------------- | --------------------------------------------------- | --------------------------------------------- |
| Fundamental Baptist Pastor | [pastor.md](stakeholders/pastor.md)                 | Primary domain expert and end-user validator  |
| Church Member User         | [church-member.md](stakeholders/church-member.md)   | Typical end-user for member-facing features   |
| Church Visitor User        | [church-visitor.md](stakeholders/church-visitor.md) | First-time or occasional user perspective     |
| Product Owner              | [product-owner.md](stakeholders/product-owner.md)   | Backlog ownership, story acceptance, priority |

### Engineering Team

| Persona                     | File                                                                       | Purpose                                        |
| --------------------------- | -------------------------------------------------------------------------- | ---------------------------------------------- |
| Architect                   | [architect.md](engineering/architect.md)                                   | System design, standards, technical direction  |
| UI/UX Engineer              | [ui-ux-engineer.md](engineering/ui-ux-engineer.md)                         | Design systems, accessibility, user experience |
| Full Stack Senior Developer | [fullstack-senior-developer.md](engineering/fullstack-senior-developer.md) | Feature lead, cross-stack implementation       |
| Full Stack Backend Engineer | [fullstack-backend-engineer.md](engineering/fullstack-backend-engineer.md) | API, services, server-side logic               |
| Cloud Engineer              | [cloud-engineer.md](engineering/cloud-engineer.md)                         | Infrastructure, cloud services, scaling        |
| DevOps Engineer             | [devops-engineer.md](engineering/devops-engineer.md)                       | CI/CD, deployments, monitoring                 |
| AI Engineer                 | [ai-engineer.md](engineering/ai-engineer.md)                               | ML pipelines, LLM integration, AI features     |
| Database Engineer           | [database-engineer.md](engineering/database-engineer.md)                   | Schema design, queries, data integrity         |
| Mobile Engineer             | [mobile-engineer.md](engineering/mobile-engineer.md)                       | Mobile app development, responsive design      |
| Testing Engineer            | [testing-engineer.md](engineering/testing-engineer.md)                     | Test strategy, automation, coverage            |

### Quality Assurance

| Persona     | File                                     | Purpose                                              |
| ----------- | ---------------------------------------- | ---------------------------------------------------- |
| QA Engineer | [qa-engineer.md](quality/qa-engineer.md) | Final review gate — validates all work is truly done |

## Workflow

```
Product Owner → defines & prioritizes stories
       ↓
Architect → designs solution, assigns to engineers
       ↓
Engineers → implement per their Definition of Done
       ↓
Testing Engineer → writes & runs automated tests
       ↓
QA Engineer → validates story completion, tests pass, DoD met
       ↓
Pastor / Users → confirm work meets their requirements
       ↓
Product Owner → accepts the story
```

## Rules

All engineering personas must follow the [Engineering Rules](rules/engineering-rules.md) which define the shared Definition of Done and quality gates.
