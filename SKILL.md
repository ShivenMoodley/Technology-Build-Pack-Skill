---
name: generate-technology-build-pack
description: Turn a completed product discovery, brain-sparring session, concept discussion, or supplied product notes into a coordinated development-ready documentation pack in professional Word format. Use when Codex must create or update a PRD, technical design document (TDD), application flow, UX/UI design brief, backend/database schema, engineering implementation plan, or the full set for handoff to product, design, engineering, data, security, compliance, QA, or delivery teams.
---

# Generate Technology Build Pack

Create an implementation-ready documentation pack whose documents agree on scope, terminology, identifiers, workflows, requirements, architecture, data, and delivery sequencing.

## Required companion workflow

Read and follow the complete `documents` skill before creating any Word files. Use its required DOCX design preset, creation, render, inspection, accessibility, and delivery workflow. Save final user-facing files persistently as required by the active environment.

## Establish the evidence base

Treat the current conversation, user-provided files, approved decisions, and explicitly stated assumptions as the source record.

Before drafting:

1. Extract the product vision, users, problem, value proposition, scope, constraints, jurisdictions, platforms, integrations, security needs, commercial model, delivery expectations, and unresolved decisions.
2. Separate confirmed facts from reasonable assumptions and unresolved questions.
3. Ask only questions whose answers would materially change architecture, scope, compliance, user journeys, or delivery. If the user asks to proceed without clarification, use conservative assumptions and record them.
4. Never invent research findings, customer validation, regulatory approval, integration capability, performance results, or committed delivery dates.
5. Create a canonical glossary and requirement-ID system before authoring.

Read [document-system.md](references/document-system.md) for ownership boundaries, required sections, cross-document mappings, diagrams, and acceptance gates.

## Select the deliverables

Create only the documents requested. When the user requests the complete pack, produce six separate DOCX files:

1. Product Requirements Document
2. Technical Design Document
3. Application Flow Specification
4. Product Design Brief
5. Backend and Database Schema
6. Engineering Delivery Plan

Also create a concise pack index DOCX when producing four or more documents. The index must describe the document set, intended readers, document ownership, version, status, dependency order, glossary, and traceability key. Do not merge the six documents unless the user explicitly asks for one consolidated file.

## Maintain one source of truth

Use these identifiers consistently:

- `BR-###` for business requirements
- `FR-###` for functional requirements
- `NFR-###` for non-functional requirements
- `US-###` for user stories
- `AC-###` for acceptance criteria
- `FLOW-###` for user or system flows
- `API-###` for interfaces
- `DATA-###` for entities or data requirements
- `SEC-###` for security controls
- `OBS-###` for observability requirements
- `TEST-###` for test scenarios
- `EPIC-###` and `TASK-###` for delivery work
- `ADR-###` for architecture decisions
- `RISK-###` for risks

Do not create duplicate IDs. Ensure downstream documents reference the originating requirement or flow. Use the same names for roles, states, services, events, entities, and integrations everywhere.

## Author in dependency order

Draft in this order even if delivery order differs:

1. Pack index and glossary
2. PRD
3. Application flow
4. Design brief
5. Technical design
6. Backend/database schema
7. Engineering plan

Reconcile all documents after drafting. A late architecture or schema decision must be reflected in the relevant flows, requirements, acceptance criteria, and plan.

## Writing standard

Write for professional team use:

- Use full sentences for explanations, decisions, assumptions, and rationale.
- Use direct, specific language and active voice.
- Avoid generic openings, inflated claims, repetitive summaries, rhetorical filler, and formulaic contrast structures.
- Define specialist terms at first use.
- Use lists for discrete requirements, steps, checks, and enumerations, not as a substitute for explanation.
- Use tables only for genuinely comparable structured information.
- State an owner or responsible discipline for decisions and actions where useful.
- Distinguish `Must`, `Should`, `May`, `Out of scope`, `Assumption`, `Decision`, and `Open question`.
- Make every requirement testable and implementation-relevant.

## Word document standard

Apply the following user requirements in addition to the `documents` skill:

- Use Arial throughout.
- Use 10-point body text.
- Use a restrained professional heading hierarchy with numbered Heading 1, Heading 2, and Heading 3 styles.
- Include a title page or polished opening block, document control, version history, owner, contributors, approval status, confidentiality classification, and table of contents.
- Use page numbers, document title/version in the footer, figure and table captions, and repeating table headers.
- Keep visual treatments restrained and consistent across the pack.
- Use landscape pages only for wide schemas, matrices, or plans that cannot remain readable in portrait.
- Add alternative text to meaningful diagrams and images.

## Diagram standard

Create diagrams only when they improve operational understanding. Use native Word shapes when practical or generate clean vector/raster figures from structured diagram definitions. Never use screenshots of code or raw Mermaid text as the delivered diagram.

Use:

- a system context or container diagram for architecture;
- swimlanes for cross-role flows;
- sequence diagrams for time-ordered service interactions;
- state diagrams for lifecycle-heavy entities;
- entity-relationship diagrams for database structure;
- deployment diagrams when infrastructure topology matters;
- dependency or milestone diagrams when sequencing is complex.

Every diagram must have a figure number, descriptive title, legend where needed, readable labels, accompanying explanation, and explicit links to relevant requirement or flow IDs.

## Quality gates

Before finalizing:

1. Run the completeness gates in [document-system.md](references/document-system.md).
2. Build a traceability matrix linking business requirements through functional requirements, flows, design components, APIs/data, acceptance criteria, tests, and engineering work.
3. Verify that every in-scope capability appears in the PRD, at least one flow, the design/technical treatment, acceptance criteria, and the engineering plan.
4. Verify that all external integrations specify direction, authentication, core payloads, failure handling, rate or timeout considerations, and ownership.
5. Verify that sensitive data has classification, lawful or stated purpose, access control, encryption, retention, deletion, audit, backup, and recovery treatment where applicable.
6. Verify that non-functional requirements contain measurable targets or clearly labeled targets to be confirmed.
7. Verify that the engineering plan includes dependencies, estimates or sizing method, environments, migration, testing, release, rollback, observability, documentation, and definition of done.
8. Remove contradictions, placeholders presented as facts, orphan requirements, unexplained acronyms, and duplicated prose.
9. Render every DOCX to PNG and visually inspect every page. Correct clipping, overflow, broken tables, poor page breaks, unreadable diagrams, excessive whitespace, and inconsistent styling. Re-render after fixes.

## Final handoff

Provide the requested DOCX files and a short handoff note that states:

- what was produced;
- which assumptions or open decisions remain;
- whether the documents passed cross-document and visual QA;
- the recommended review order.

Do not claim that the pack is implementation-ready when material product, regulatory, security, integration, or architecture decisions remain unresolved. In that case, describe it as a review-ready baseline and identify the blocking decisions.
