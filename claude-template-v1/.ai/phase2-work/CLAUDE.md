# Stage 2: Work

This is the execution phase of the project. 

This stage my only begin when the planning stage is completed.

## Problem

Take outputs of planning stage and turn them into working software.

For each feature, we need to:
- create a PRP
- implement the PRP
- complete a PR for the feature

## Goals / Exit Criteria

### Goals
The goals are to complete all the features in the plan.
Completion consists of 3 steps:
1. create a PRP
2. implement the PRP
3. complete a PR for the feature

### Exit Criteria
The exit criteria is to have completed all the features in the plan.
You can exit the stage when all the features in the plan have been completed.
You will know what features are in the plan by looking at the contents of `.ai/phase1-plan/02-feature-recommendations.md`.
Inside that document a Feature will be identified by a number and a brief name, e.g. "Feature 1.: Project Setup"
You will know if a PRP exists for a feature if there is a corresponding folder in `.ai/phase2-work/features/feature-<feature-number>-<feature-name>`.
You will know if a PR has been completed, which will only occur after the feature has been implemented, if there is a PR in github for the feature.
You will track feature progress based on existence of PRP and PR.

## Process

For each feature, in order, we need to:

### Step 1. Create a PRP

The `<path-to-feature-discussion>` is `.ai/phase1-plan/05-feature-discussions/<phase-number>-<feature-number>-<feature-name>.md`.

If there is not an existing `.ai/phase2-work/features/feature-<feature-number>-<feature-name>` folder, then run the claude command: `/mgc.2.1-create-prp-from-feature <path-to-feature-discussion>` (defined in `.claude/commands/mgc.2.1-create-prp-from-feature.md`).

### Step 2. Execute the PRP

The `<path-to-prp>` is `.ai/phase2-work/features/feature-<feature-number>-<feature-name>/description.md`.

If there is not an existing PR for the feature, then run the claude command: `/mgc.2.2-execute-prp <path-to-prp>` (defined in `.claude/commands/mgc.2.2-execute-prp.md`).

Once the feature is implemented, then proceed to step 3.

### Step 3. Create a PR

When you have completed your feature, you should create a PR.
```bash
# Set a timer/reminder to commit regularly
git add -A
git commit -m "feature <feature-number>: <feature-name>"
```