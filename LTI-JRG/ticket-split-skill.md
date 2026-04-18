---
name: ticket-split
description: 'Split PRDs, epics, and user stories into implementation-ready tickets with MVP vs next Versions release slicing. Use when planning delivery scope, dependency order, and sprint-ready backlog items.'
argument-hint: 'PRD path, User Stories, epic, or story set to split into tickets'
---

# Ticket Split

Convert high-level product requirements into small, testable tickets and a clear MVP versus next Versions.

## When to Use
- You need to split an epic or large story into sprint-sized tickets.
- You need to decide what belongs to MVP versus next Versions.
- You need to expose dependency order before planning.
- You need backlog items with acceptance criteria and release assignment.

## Workflow Extracted From This Project
1. Start from a simplified PRD with clear in-scope and out-of-scope boundaries.
2. Create user stories with testable acceptance criteria.
3. Map stories into an end-to-end backbone journey.
4. Prioritize using flow dependency, business value, and risk reduction.
5. Slice stories into tickets and assign release targets (MVP or next Versions).

## Inputs to Collect
1. Product goal and release objective.
2. Source artifacts (PRD, story list, or story map).
3. Scope boundaries and constraints.
4. Team capacity and timeline assumptions.
5. Required output level (high-level or implementation-ready).

If any critical input is missing, ask concise clarifying questions before splitting.

## Procedure
1. Read the source artifact and identify the backbone flow.
2. Order candidate stories by dependency and value.
3. Mark stories as MVP candidate, next Versions candidate, or needs clarification.
4. Split large stories into vertical slices with user-visible outcomes.
5. Convert each slice into a ticket with BDD-style acceptance criteria.
6. Add size estimate (S/M/L), dependencies, and release tag.
7. Validate ticket quality using completion checks.
8. Return final execution order and MVP/next Versions rationale.

## Decision Points
- Is a story too large for one sprint?
	Split by workflow step, user role, or happy path versus edge case.
- Is a ticket technical but not user-visible?
	Reframe as an enabler ticket tied to a visible outcome.
- Is release placement unclear?
	Prefer MVP only if the ticket is required for the minimum end-to-end flow.
- Is dependency risk high?
	Pull enablers earlier and defer optional enhancements.

## Release Slicing Rules
- MVP includes only the minimum coherent end-to-end flow.
- Next Versions includes depth, optimization, and expanded integrations.
- Do not place blockers of core flow in next Versions.
- Prefer thin vertical slices over horizontal component chunks.

## Defaults
- Scope: workspace-scoped skill at `.github/skills/ticket-split/`.
- Source selection: auto-detect source artifact and ask when ambiguous.
- Output depth: implementation-ready split with about 8 to 15 tickets.
- Release model: MVP versus next Versions only.

## Output Format
Return:
1. Backbone flow (ordered activities)
2. Ticket list with IDs
3. Ticket details:
	 - Title
	 - Story - Detailed description
	 - Acceptance criteria (Given/When/Then)
   - Priority (Highest, High, Medium, Low, Lowest)
	 - Dependencies
	 - Release (MVP or next Versions)
   - Effort estimation (Estimated time in days)
   - Tags (by product features like: Backend, Frontend, Infrastructure, etc)
   - Links or References
   - Change History
4. Prioritized implementation sequence
5. Short rationale for MVP versus next Versions split

## Completion Checks
A split is ready when:
- Every ticket has explicit user or business value.
- Tickets are small enough for sprint planning.
- Acceptance criteria are testable and unambiguous.
- Dependencies and order are explicit and conflict-free.
- MVP contains a usable end-to-end experience.
- Next Versions items are enhancements, not MVP blockers.

## Quality Bar
- Keep one primary outcome per ticket.
- Use concrete verbs and measurable outcomes.
- Avoid implementation-only wording unless marked as enabler.
- Flag assumptions and unresolved risks explicitly.
