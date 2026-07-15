# OctoAcme Project Management Documentation

## Overview

OctoAcme follows a structured, customer-focused approach to project management that emphasizes iterative delivery, clear ownership, data-informed decisions, and psychological safety. Our process guides teams through five core lifecycle phases: initiation, planning, execution, release, and retrospective.

### Project Management Framework

**Core Lifecycle & Framework**
OctoAcme follows a structured five-phase project lifecycle: initiation, planning, execution, release, and retrospective. The organization prioritizes customer value through iterative delivery of small, testable increments while maintaining clear ownership and accountability. Each project has a dedicated Project Manager who coordinates delivery and a Product Manager who defines outcomes and measures success. Projects begin with a lightweight One-pager that confirms business need, identifies stakeholders, and establishes measurable success criteria before moving into detailed planning. This decision-gate approach ensures only validated initiatives proceed to resource-intensive planning phases.

**Roles, Responsibilities & Communication Cadence**
Three core personas drive project execution: Developers implement features and maintain quality through testing and code review; Product Managers define what to build and prioritize the backlog based on customer and business value; and Project Managers orchestrate schedules, risks, and communications. The team operates on a regular communication rhythm including daily standups (15 minutes), twice-weekly delivery standups, weekly syncs between PM and Product Manager, and monthly stakeholder updates. This cadence ensures alignment while minimizing overhead, with ad-hoc escalations triggered when blockers arise at team, product lead, or sponsor levels.

**Execution & Quality Assurance**
OctoAcme maintains high delivery standards through structured workflows: work flows through a project board with columns for Backlog, Ready, In Progress, In Review, QA, and Done. Pull requests must be small (≤400 lines where possible), include issue links and acceptance criteria, and pass automated testing and security scanning before requiring at least one approval. Quality is enforced through unit tests, integration tests, end-to-end smoke tests for critical flows, and manual QA when needed. Teams track velocity and burndown metrics, monitor success indicators via dashboards, and document risks continuously—updating a Risk Register weekly that captures impact, probability, mitigation plans, and owners to ensure proactive issue management.

**Continuous Learning & Improvement**
After each sprint, release, or milestone, OctoAcme conducts structured retrospectives (45–75 minutes) to capture what went well, identify improvements, and generate prioritized action items with clear owners and timelines. Release and deployment are standardized with pre-release checklists, staging verification, post-deploy validation, and documented rollback plans. This emphasis on blameless incident analysis, captured learnings, and iterative process refinement—combined with a culture of psychological safety—enables OctoAcme teams to reduce single-person dependencies, accelerate onboarding, and execute consistently across projects.

---

## Key Principles

- 🎯 **Customer-first** — Prioritize customer value and usability
- 🔄 **Iterative delivery** — Deliver small, testable increments
- 👤 **Clear ownership** — Each project has a named PM and Product Lead
- 📊 **Data-informed decisions** — Measure impact and iterate based on evidence
- 🛡️ **Psychological safety** — Encourage feedback and learning

---

## Quick Navigation

### Getting Started

New to OctoAcme project management? Start here:

- **[Project Management Overview](octoacme-project-management-overview.md)** — Understand our principles, roles, key artifacts, and lifecycle
- **[Roles & Personas](octoacme-roles-and-personas.md)** — Learn about Project Managers, Product Managers, Developers, and stakeholder roles

### Project Lifecycle

#### 1. Initiation

- **[Project Initiation Guide](octoacme-project-initiation.md)** — Validate business need, align stakeholders, create a one-pager, and secure go/no-go approval

#### 2. Planning

- **[Project Planning](octoacme-project-planning.md)** — Break work into shippable increments, estimate scope, identify dependencies, and create a release plan

#### 3. Execution

- **[Execution & Tracking](octoacme-execution-and-tracking.md)** — Manage day-to-day delivery, track progress, maintain quality standards, and escalate blockers

#### 4. Release

- **[Release & Deployment Guide](octoacme-release-and-deployment.md)** — Standardize deployment processes, prepare release notes, and manage rollbacks

#### 5. Retrospective

- **[Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)** — Capture learnings, convert them into actionable improvements, and measure impact

### Cross-cutting Concerns

- **[Risk Management & Communication](octoacme-risks-and-communication.md)** — Maintain a risk register, escalate issues, and keep stakeholders informed

---

## Finding the Right Document

| I need to... | Read this doc |
|---|---|
| Understand OctoAcme's approach and get oriented | [Project Management Overview](octoacme-project-management-overview.md) |
| Define roles and responsibilities | [Roles & Personas](octoacme-roles-and-personas.md) |
| Kick off a new project or initiative | [Project Initiation Guide](octoacme-project-initiation.md) |
| Create a backlog and release plan | [Project Planning](octoacme-project-planning.md) |
| Track progress and manage delivery | [Execution & Tracking](octoacme-execution-and-tracking.md) |
| Manage risks and escalations | [Risk Management & Communication](octoacme-risks-and-communication.md) |
| Prepare for and execute a release | [Release & Deployment Guide](octoacme-release-and-deployment.md) |
| Capture learnings and improve | [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) |

---

## Document Overview

### Foundation Documents

**[Project Management Overview](octoacme-project-management-overview.md)**
High-level introduction to OctoAcme's approach, core roles (PM, PdM, Developers, QA, Stakeholders), key artifacts, and the five-phase lifecycle.

**[Roles & Personas](octoacme-roles-and-personas.md)**
Detailed definitions of typical roles and responsibilities, including Developers, Product Managers, and Project Managers, with their goals and communication patterns.

### Lifecycle Phase Documents

**[Project Initiation Guide](octoacme-project-initiation.md)**
Initial validation steps: confirm business need, identify stakeholders, define success criteria, and make a go/no-go decision before planning. Includes the One-pager template and initiation checklist.

**[Project Planning](octoacme-project-planning.md)**
Turn approved initiatives into actionable plans: break work into shippable increments, estimate scope, identify dependencies, and create release plans. Includes backlog item template and sprint planning guidance.

**[Execution & Tracking](octoacme-execution-and-tracking.md)**
Day-to-day delivery management: team rhythm (standups, syncs, demos), workflow practices, quality standards, reporting metrics, blocker escalation, and execution checklist.

**[Risk Management & Communication](octoacme-risks-and-communication.md)**
Identify, assess, and monitor risks using a Risk Register. Maintain stakeholder communication through regular updates, incident communications, and clear escalation paths.

**[Release & Deployment Guide](octoacme-release-and-deployment.md)**
Standardize releases: define release types, pre-release requirements, deployment checklists, rollback procedures, and release notes. Includes post-deploy verification and incident playbook.

**[Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)**
Capture learnings after sprints, releases, or milestones. Structure retrospectives, track improvements, and build a continuous improvement culture with measurable impact.

---

## Using These Docs with Copilot Spaces

This documentation is designed to be centralized, searchable, and version-controlled. By storing process documentation in this repository:

- **New team members** can quickly discover all project management guidance in one place
- **All team members** have equal access to processes, decisions, and rationale
- **Processes remain current** through collaborative refinement and version control
- **Onboarding accelerates** by reducing single-person dependency risk
- **Consistency improves** through standardized, documented workflows

When setting up a Copilot Space for a project, add this folder as context to enable AI-assisted guidance on OctoAcme processes tailored to your specific project.

---

## Contributing to This Documentation

Help us keep OctoAcme processes current and relevant:

1. Use these docs as context for your project work
2. Notice gaps, unclear guidance, or outdated practices? [Create an issue](../issues/new) with the `documentation` label
3. Propose updates through pull requests—reference the issue and ensure changes align with OctoAcme principles
4. Capture retrospective learnings and convert them into process improvements
5. Review and refine based on team feedback

---

**Last Updated:** July 2026  
**Maintained by:** OctoAcme Team
