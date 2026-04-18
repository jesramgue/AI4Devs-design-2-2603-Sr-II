Prompts - LTI Jesus Ramirez Guerrero
# Environment
 IDE: Visual Studio Code using GitHub Copilot using GPT-5.4 - Thinking Effort Medium 

# 1. Simplify PRD
I felt that the result of the previous design session was not simple enough for the AI ​​to focus on the real goal (user stories and ticket splitting), with the intention of making agents more productive (better results), so I decided to simplify the LTI-JRG.md documentation a bit.

## Prompt
As a Senior Product Manager generate a simpler Product Requirements Document (PRD) out of the LTI-JRG.md. The expected structure is similar to: 
- Title
- Product Summary
- Problem Statement
- Goal
- Target Users / Personas
- Product Objectives
- Success Metrics
- Scope for MVP (list of items)
- Out of Scope for MVP (list of items)
- Key User Stories
- Functional Requirements
- Non-Functional Requirements
- Risks
- Open Questions

Save the result in a Markdown file "LTI-JRG/LTI-JRG-PRD.md"

# 2. User Stories Generation
Before writing the next prompt I thought it was a good idea if I detailed to the AI what the user-stories skills looks like, to define what I really expect from him so I wrote the skill called user-stories with indeed some of the content and examples from our documentation.
Check [LTI-JRG/user-stories-skill.md](./user-stories-skill.md)

## Prompt
Act as a senior Product Owner with experience in Agile methodologies and user stories generation skills.

Based on the project PRD, generate 5 User Stories.

After generating the stories, suggest a prioritization order for the MVP and justify your decision.

Write the output into a Markdown file "LTI-JRG/UserStories-JRG.md"

# 3. User Story Mapping
I considered the backlog a bit flat, losing the complete user journey. For that and to facilitate the discussion with the team about what the MVP truly is I considered to create a the User Story Mapping to visualise better the dependencies and gaps in functionality.

For that I created a user-story-mapping-skill.md with what I expect the agent to produce and the structure. I considered in the first version to use Mermaid to check if it was powerful and easy to maintain enough.
Check [LTI-JRG/user-stories-mapping-skill.md](./user-stories-mapping-skill.md)

## Prompt
Create a User Story Map for that use the user stories created, and indicate which ones would go in the MVP versus version 2
User the new Skill created LTI-JRG/user-stories-mapping-skill.md

Add the output in "LTI-JRG/UserStories-JRG.md" after the last header

# 4. Ticket Split
As I want the ticket in a particular structure, with the intention to reuse it, I created another skill to detail and define how I want the tickets to be splitted and the expected outputs. 
Check [LTI-JRG/ticket-split-skill.md](./ticket-split-skill.md)

## Prompt
Convert the User Story "US-01: Create and Publish a Job Opening" into small, testable and implementation-ready tickets using the new skill ticket-split.

Add the result to "LTI-JRG/UserStories-JRG.md" after the last header