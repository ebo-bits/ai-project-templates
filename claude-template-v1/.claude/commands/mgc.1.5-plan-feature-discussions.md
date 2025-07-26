# Plan Feature Discussion

## Goal

To generate prompts that can be useful for making details plans for each feature.

## Process
- Review initial project description: `.ai/phase01-plan/01-initial-description.md`
- Review feature recommendations: `.ai/phase01-plan/02-feature-recommendations.md`
- Review technology decisions: `.ai/phase01-plan/03-technology-decisions`
- Review onboarding materials: `.ai/phase01-plan/04-onboarding-materials`
- For each feature, produce a prompt that can be used to generate a detailed document suitable for a junior developer that will cover:
    - Purpose: Why we are building this?
    - Scenarios: Who is using it and their core usage scenarios? These scenarios must describe clearly the users involved and what they are doing and what they expect to happen. These can be as simple as: "I CAN..." statements.
    - Capabilities: Core requirements and features?
    - Key Technical Decisions: Identify the most important technical decisions and document them. These can include design, architecture, technology decisions, etc. Clarify what is in scope and out of scope for this work.
    - Technical Design: Describe the core technical architecture. Identify the core components and their responsibilities and dependencies
    - Codebase layout: Clearly communicate the folder structure, include pertinent README.md files
    - Key Interfaces: Follow industrial strength enterprise coding practices and identify clear separation of concerns and contracts between key components
    - Resources: Describe all core services, resources, infrastructure sufficiently for a junior developer
    - Milestones: Provide a staged workback plan with clear swimlanes and milestones
    - Developers: Identify how many developers and what each developers focus is. Clearly identify which developers will work regularly with which other developers.
    - Work Items: Identify major work items and sub work-items

## Output
- Write each prompt in a markdown file: `.ai/phase1-plan/05-feature-discussions/{phase-number}-{feature-number}-{feature-name}.md}`

## Tips
- The generated prompts should all have clear references to the knowledge base as appropriate.
- each file should be clearly named using hyphens to separate words
