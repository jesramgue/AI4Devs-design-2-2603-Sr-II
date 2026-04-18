---
name: user-stories
description: 'Create and refine user stories for product discovery and delivery planning. Use when writing backlog items, splitting epics, defining acceptance criteria, and preparing stories for sprint planning.'
argument-hint: 'Feature, epic, or problem statement to turn into user stories'
---

# User Stories

Generate clear, testable user stories that teams can implement with minimal ambiguity.

## When to Use
- Turn ideas or requirements into actionable backlog items.
- Split an epic into independently deliverable stories.
- Add acceptance criteria before sprint planning.
- Improve story quality before engineering handoff.

## Inputs to Collect
1. Business objective: what outcome matters and why.
2. Target user/persona: who gets value.
3. Context and constraints: platform, policy, compliance, deadlines.
4. Scope boundaries: what is in and out for this iteration.
5. Dependencies: systems, teams, or data needed.

If key inputs are missing, ask focused clarifying questions before writing stories.

## Procedure
1. Define the story goal.
2. Identify the actor, need, and intended value.
3. Draft the story in this template:
   As a <user/persona>, I want <capability>, so that <outcome/value>.
4. Add acceptance criteria as observable behaviors.
5. Add non-functional criteria only when materially relevant.
6. Add explicit out-of-scope notes to prevent scope creep.
7. Validate story quality with the completion checks below.
8. If too large, split the story using vertical slicing.

## Decision Points
- Is the user unclear?
  Ask for persona or infer a temporary one and mark assumption.
- Is the value vague?
  Rewrite the "so that" clause in measurable terms.
- Is the story too big for one iteration?
  Split by user journey step, business rule, or platform variant.
- Are acceptance criteria implementation-specific?
  Rephrase as behavior and outcomes, not technical tasks.

## Splitting Rules (Branching Logic)
- If story spans multiple workflows: split by workflow.
- If story has multiple permissions/roles: split by role.
- If story includes create/read/update/delete together: split by operation.
- If story mixes happy path and complex edge cases: keep happy path first, move edge cases to follow-up stories.

## Acceptance Criteria Pattern
Use concise Given/When/Then format when possible.

Example:
- Given a signed-in user with editor access
- When they publish a draft article
- Then the article becomes visible on the public site within 5 seconds

## Completion Checks (Definition of Ready)
A story is ready when all checks pass:
- Clear actor, action, and value are present.
- Acceptance criteria are testable and unambiguous.
- Scope fits one iteration for one team.
- Dependencies and assumptions are explicit.
- Out-of-scope is stated.
- Priority and success signal are defined.

## Output Format
Return stories in this structure:
1. Story title
2. Story statement (As a / I want / so that)
3. Acceptance criteria
4. Complexity estimate (S/M/L)
5. INVEST evaluation (brief notes on each criterion)
6. Assumptions
7. Out of scope
8. Dependencies
9. Suggested split (if needed)


## Quality Bar
- Prefer user outcomes over implementation details.
- Prefer concrete verbs over abstract terms like "manage".
- Keep each criterion independently verifiable.
- Avoid combining unrelated capabilities in one story.
- Keep it simply structured for easy understanding and estimation.

## INVEST Criteria: the Checklist for High-Quality User Stories
An essential framework to evaluate whether a User Story is well defined is INVEST, an acronym created by Bill Wake in 2003 that every professional agile team uses as a checklist during backlog refinement.

### I — Independent
Each story should be able to be developed and delivered without depending on other stories. This allows flexibility in prioritization and sprint planning. If two stories are tightly coupled, consider combining or rewriting them.

### N — Negotiable
The story is not a rigid contract, but an invitation to conversation. Implementation details are negotiated between the Product Owner and the team during refinement. This connects directly with Ron Jeffries’ 3 Cs: Card (the written story), Conversation (team dialogue), and Confirmation (acceptance criteria).

### V — Valuable
Each story must deliver clear value to the end user or the business. If you cannot explain why it matters, it probably should not be in the sprint. The value should be external and visible to the user, not an internal technical benefit.

### E — Estimable
The team should be able to estimate the effort with reasonable confidence. If a story is too vague to estimate, it needs more conversation or decomposition. Note: Bill Wake has mentioned that if he were to revisit INVEST today, he would replace the "E" with "External" (visible external value), as estimation is the most overused criterion.

### S — Small
It should be small enough to be completed within a sprint (ideally 3–4 days of total work). Large stories (disguised epics) should be split into vertical slices that cut across all layers of the architecture—like slicing a cake through all layers rather than just the top layer.

### T — Testable
It must be possible to define clear acceptance criteria that allow verification of whether the story has been completed correctly. If you cannot write acceptance criteria immediately, the story needs more refinement.

## Full example with BDD acceptance criteria

Title: Smart course search with suggestions

User Story:

As an e-learning platform student,
I want to search for courses by keyword and receive relevant suggestions as I type,
so that I can quickly find the course I need without browsing the entire catalog.

Acceptance Criteria (BDD format):

Given I am on the homepage, when I type at least 3 characters in the search bar, then course suggestions appear in real time (maximum 500ms).

Given I see the search results, when I click on a course, then I navigate to the course detail page.

Given I search for a term that matches no course, when results are displayed, then I see a “No results” message with suggested courses by category.

Additional Notes:

The search should support title, description, and instructor fields.

Consider integration with a search service such as Algolia or Elasticsearch.

Accessibility: the component must be keyboard navigable.

Related User Stories:

US-045: Filter courses by category
US-052: Course detail page

INVEST Evaluation:

Independent: Does not depend on other stories to function.
Negotiable: Implementation (Algolia vs Elasticsearch) is negotiable.
Valuable: Directly improves user discovery experience.
Estimable: Clear scope, team can estimate confidently.
Small: Completable within a sprint.
Testable: Clear and measurable acceptance criteria (500ms, navigation, messaging).