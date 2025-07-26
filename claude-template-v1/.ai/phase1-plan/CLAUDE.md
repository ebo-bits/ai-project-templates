# Stage 1: Plan

This is the first stage of any project. 

It *must* be completed prior to moving to stage 2.

## Problem

Large software projects require a significant amount of planning and preparation. This stage is designed to ensure that the project is well-defined, the team is aligned, and the necessary groundwork is in place before development begins.

This avoids building the wrong thing, or building the right thing in the wrong way. This saves time and maximizes probability of success -- getting solutions to customers and improving people's lives.

In AI first development, clear guidance (or effective context) is pre-emminent. Too much or too little context is a common pitfall. Process here is to provide A. the right context - focusing on the salient aspects that enable test-driven development, and B. the right amount of context - enough to enable the AI to build the right thing, but not so much as to overwhelm the model and prevent it from building anything useful.

## Goals / Exit Criteria

### Goals
- bring clarity to the problem statement and the solution - scenarios, requirements, etc.
- define the features that need to be built and a roadmap
- make key technology decisions
- prepare onboarding guidance for developers
- prepare feature design discussions for success
- tighten, refine, and align the plan before we head to execution

### Exit Criteria
- [ ] We have initial direction: `01-initial-description.md`
- [ ] We have defined features for a junior developer team and have a roadmap describing phases: `02-feature-recommendations.md`
- [ ] We have done a preliminary analysis of approaches for the project as a whole, made key tech decisions: `03-technology-decisions/{decision-name}.md`
- [ ] We have provided effective guidance for developer on-boarding: `04-onboarding-materials/{document-name}.md`
- [ ] We have prepared a set of feature design discussions, providing each feature team with a rich set of context to start their work: `05-feature-discussions/{phase-number}-{feature-number}-{feature-name}.md}`
- [ ] We have reviewed and refined the plan: `06-plan-improvements.md`

### Definition of done
It is complete if the following are true:
- Condition 1: there exists a non-empty file `.ai/phase1-plan/01-initial-description.md`
- Condition 2: there exists a non-empty file `.ai/phase1-plan/02-feature-recommendations.md`
- Condition 3: there exists a non-empty directory with non-empty technology decision files: `.ai/phase1-plan/03-technology-decisions/{decision-name}.md`
- Condition 4: there exists a non-empty directory with non-empty on-boarding files: `.ai/phase1-plan/04-onboarding-materials/{document-name}.md`
- Condition 5: for each feature recommended in the `02-feature-recommendations.md` file, there exists a non-empty file in the `.ai/phase1-plan/04-features/{phase-number}-{feature-number}-{feature-name}.md` file
    - feature numbers are 1-indexed and are priority ordered across phases / globally for project
- Condition 6: there exists a non-empty file `.ai/phase1-plan/06-plan-improvements.md`

## Process

### Step 1. Get Started

If condition 1 is not met, then run the claude command: `/mgc.1.1-get-started` (defined in `.claude/commands/mgc.1.1-get-started.md`).

### Step 2. Recommend Features and Produce Roadmap

If condition 2 is not met, then run the claude command: `/mgc.1.2-feature-team-sizing` (defined in `.claude/commands/mgc.1.2-feature-team-sizing.md`)

### Step 3. Make Important Technology Decisions

If condition 3 is not met, then run the claude command: `/mgc.1.3-make-technology-decisions` (defined in `.claude/commands/mgc.1.3-make-technology-decisions.md`).

### Step 4. Prepare Onboarding Guidance For Developers

If condition 4 is not met, then run the claude command: `/mgc.1.4-prepare-onboarding-materials` (defined in `.claude/commands/mgc.1.4-prepare-onboarding-materials.md`).

### Step 5. Plan Feature Discussions

If condition 5 is not met, then run the claude command: `/mgc.1.5-plan-feature-discussions` (defined in `.claude/commands/mgc.1.5-plan-feature-discussions.md`).

### Step 6. Set Up Feature Design Discussions For Success

If condition 6 is not met, then run the claude command: `/mgc.1.6-finalize-plan` (defined in `.claude/commands/mgc.1.6-finalize-plan.md`).