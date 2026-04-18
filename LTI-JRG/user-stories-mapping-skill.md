---
name: user-story-mapping
description: 'Generate user story maps and prioritized MVP backlogs from PRDs. Use when turning product requirements into workflow-aligned stories, acceptance criteria, and release slices.'
argument-hint: 'PRD file path or product scope to map into user stories'
---

# User Story Mapping

Turn a PRD into a practical story map and MVP delivery sequence.

## When To Use
- You have a PRD and need a clear end-to-end user journey.
- You need to convert broad requirements into implementable stories.
- You need to define an MVP slice with justification.
- You need acceptance criteria and prioritization for sprint planning.

## Inputs To Collect
1. Product goal and business outcome.
2. Target personas and primary actor per flow.
3. In-scope and out-of-scope boundaries.
4. MVP constraints (time, team size, technical limits).
5. Success metrics and decision criteria.
6. Requested story count.

If key inputs are missing, ask clarifying questions before mapping.

## Procedure
1. Read and summarize the PRD into a one-line product goal.
2. Identify the backbone journey (major user activities in order).
3. Break each activity into user tasks.
4. Convert tasks into user stories in this format:
   As a <persona>, I want <capability>, so that <value>.
5. Add concise Given/When/Then acceptance criteria per story.
6. Estimate complexity (S, M, or L).
7. Evaluate each story with INVEST.
8. Mark assumptions, dependencies, and out-of-scope items.
9. Propose MVP priority order and justify the sequence.
10. If a story is too large, split it into vertical slices.

## Decision Points
- Is the backbone unclear?
  Start with a single primary flow, then add secondary flows.
- Is a story too broad for one iteration?
  Split by workflow step, user role, or happy-path vs edge case.
- Is the value statement weak?
  Rewrite the "so that" clause with measurable user or business impact.
- Are acceptance criteria implementation-heavy?
  Rephrase as observable behavior and expected outcomes.
- Is prioritization contested?
  Prioritize by flow dependency, business value, and risk reduction.

## Suggested Prioritization Logic
Use this order when building an MVP map:
1. Entry point stories (start of user journey).
2. Core value realization stories (product differentiation).
3. Validation and decision stories (quality and confidence).
4. Completion and conversion stories (end-to-end closure).
5. Optimization stories (advanced analytics, automation depth, ecosystem breadth).

## Defaults
- Always include a story map backbone plus stories in the output.
- Use flow dependency + value + risk as the default prioritization method.
- If story count is not specified, ask for the desired number before generating.

## Output Format
Return the result in this structure:
1. Story map backbone (ordered activities)
2. User-requested count user stories.
3. Acceptance criteria (Given/When/Then)
4. Complexity estimate (S/M/L)
5. INVEST evaluation (brief)
6. Assumptions
7. Dependencies
8. Out of scope
9. MVP prioritization order
10. Prioritization rationale
11. Mermaid diagram

## Completion Checks
A mapped backlog is ready when all checks pass:
- Backbone activities reflect a coherent end-to-end journey.
- Every story has clear actor, value, and testable criteria.
- Story scope is small enough for sprint planning.
- Dependencies are explicit and sequencing is defensible.
- MVP order is justified with value and risk logic.

## Quality Bar
- Prefer user outcomes over internal implementation detail.
- Prefer concrete actions over vague verbs like "manage".
- Keep each criterion independently verifiable.
- Avoid mixing multiple capabilities in one story.
- Keep language simple so teams can estimate quickly.