# Simple PRD: ATS (Applicant Tracking System)

## 1. Product Summary

ATS is a modern recruiting platform for companies that want to replace fragmented hiring tools with one system for job posting, candidate tracking, screening, interviews, and offer management.

The product's main differentiator is explainable AI. Instead of giving black-box recommendations, the platform shows why a candidate was matched, flagged, or advanced.

## 2. Problem Statement

Recruiting teams often use multiple disconnected tools for applicant tracking, assessments, interviews, messaging, and reporting. This creates four main problems:

- Recruiters waste time switching between tools.
- Hiring decisions are slower and harder to track.
- AI recommendations lack transparency and increase trust concerns.
- Compliance, auditability, and bias monitoring are difficult across disconnected systems.

## 3. Goal

Build a unified ATS that helps recruiting teams hire faster, with better visibility and stronger confidence in decision-making.

## 4. Target Users

- Recruiters managing high application volume.
- Hiring managers reviewing candidates and interview feedback.
- Interview panel members submitting structured evaluations.
- HR and leadership teams monitoring hiring funnel performance.
- Candidates applying, scheduling interviews, and tracking status.

## 5. Product Objectives

- Reduce recruiter tool switching by centralizing the hiring workflow.
- Improve hiring speed from job opening to offer.
- Provide explainable AI recommendations for screening and matching.
- Support fairer and more auditable hiring decisions.
- Simplify implementation compared to legacy ATS platforms.

## 6. Success Metrics

- Reduce average time-to-hire by 15 days versus customer baseline.
- Reduce recruiter tool switching by 60% or more.
- Reach recruiter NPS above 50.
- Improve offer acceptance rate.
- Increase adoption of AI-assisted workflows and dashboards.

## 7. Scope for MVP

### In Scope

#### 1. Job and Requisition Management
- Create, edit, publish, and close job openings.
- Use job templates for repeatable hiring workflows.
- Support approval flow before publishing when required.

#### 2. Multichannel Job Posting
- Publish jobs to careers page and selected external channels.
- Track source performance and application volume.

#### 3. Candidate and Application Management
- Create candidate profiles from resumes.
- Deduplicate applicants.
- Move candidates across hiring stages.
- Store history of actions, notes, and status updates.

#### 4. AI-Assisted Screening
- Score candidates against job requirements.
- Show match confidence and explanation.
- Flag potential concerns based on missing criteria.

#### 5. Assessment and Interview Workflow
- Send assessments.
- Schedule interviews with calendar support.
- Capture structured interview feedback.
- Summarize interview insights with AI support.

#### 6. Messaging and Candidate Portal
- Send candidate communications using templates.
- Allow candidates to view status, respond to requests, and manage interview scheduling.

#### 7. Offer and Onboarding Handoff
- Generate offers.
- Track acceptance or rejection.
- Trigger onboarding handoff to HRIS when hired.

#### 8. Reporting and Governance
- Funnel reporting by stage.
- Time-to-fill and source reporting.
- Audit log for major decisions and AI overrides.

### Out of Scope for MVP

- Deep marketplace ecosystem with dozens of integrations.
- Highly customized enterprise workflow engines.
- Advanced predictive workforce planning.
- Full BI-grade analytics beyond core recruiting dashboards.
- Fully automated hiring decisions without human review.

## 8. Key User Stories

### Recruiter
- As a recruiter, I want to create and publish a job quickly so that I can start receiving applications without using multiple tools.
- As a recruiter, I want AI-assisted screening with clear explanations so that I can prioritize strong candidates faster.
- As a recruiter, I want one place to manage communication, assessments, interviews, and offers so that I can move candidates through the funnel efficiently.

### Hiring Manager
- As a hiring manager, I want to review shortlisted candidates and structured interview feedback so that I can make faster and more consistent decisions.

### Candidate
- As a candidate, I want to track my application status and interview steps so that I know what happens next.

### HR/Leadership
- As a business leader, I want funnel and hiring performance metrics so that I can understand team efficiency and hiring quality.

## 9. Functional Requirements

### Job Management
- The system must support job creation, editing, approval, publishing, and closure.
- The system must allow reusable job templates.

### Candidate Pipeline
- The system must create and update candidate records.
- The system must support multiple hiring stages.
- The system must record candidate activity history.

### AI Support
- The system must generate candidate match scores.
- The system must explain why a recommendation was made.
- The system must allow humans to override AI suggestions and log the reason.

### Assessments and Interviews
- The system must send and track assessments.
- The system must support interview scheduling.
- The system must collect structured feedback from interviewers.

### Communications
- The system must send templated messages.
- The system must maintain a unified communication timeline per candidate.

### Reporting
- The system must show hiring funnel metrics.
- The system must track source effectiveness and time-to-fill.

## 10. Non-Functional Requirements

- Security: Role-based access and auditability are required.
- Privacy: Candidate data handling must support GDPR-style compliance needs.
- Explainability: AI outputs must include evidence or reasoning.
- Reliability: Core recruiting workflows must be available and traceable.
- Usability: Recruiters should be able to complete core workflows with minimal training.

## 11. Risks

- AI recommendations may lose trust if explanations are weak or inconsistent.
- Integration dependencies may slow implementation.
- Enterprise buyers may require deeper customization than the MVP supports.
- Bias monitoring features may be expected to be more mature than an MVP can deliver.

## 12. Open Questions

- Which external integrations are essential for the first release?
- How much AI explainability detail should be shown to recruiters by default?
- What level of customization is needed for approval workflows per customer?
- Which reporting views matter most in the first 90 days after launch?

## 13. Recommended MVP Narrative

The MVP should focus on one complete hiring flow:

1. Create and publish a job.
2. Receive and deduplicate applications.
3. Rank candidates with explainable AI.
4. Run assessments and interviews.
5. Make a decision and generate an offer.
6. Track funnel performance and audit decisions.

This keeps the first release focused on delivering the core value proposition: faster, more transparent, and more unified hiring.