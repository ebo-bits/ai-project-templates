# Stage 2: Work

<!-- Path Configuration - Update these paths if directory structure changes -->
<!-- BASE_DIR = . (current working directory) -->
<!-- AI_DIR = .ai -->
<!-- PHASE1_DIR = .ai/phase1-plan -->
<!-- PHASE2_DIR = .ai/phase2-work -->
<!-- COMMANDS_DIR = .claude/commands/wildbot/steps -->
<!--
Usage in this file:
- Feature discussions: {PHASE1_DIR}/05-feature-discussions/
- Feature work: {PHASE2_DIR}/features/
- Command references: {COMMANDS_DIR}/*.md
-->

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
You will know what features are in the plan by looking at the contents of `{PHASE1_DIR}/02-feature-recommendations.md`.
Inside that document a Feature will be identified by a number and a brief name, e.g. "Feature 1.: Project Setup"
You will know if a PRP exists for a feature if there is a corresponding folder in `{PHASE2_DIR}/features/feature-<feature-number>-<feature-name>`.
You will know if a PR has been completed, which will only occur after the feature has been implemented, if there is a PR in github for the feature.
You will track feature progress based on existence of PRP and PR.

## Process

For each feature, in order, we need to:

### Step 1. Create a PRP

The `<path-to-feature-discussion>` is `{PHASE1_DIR}/05-feature-discussions/<phase-number>-<feature-number>-<feature-name>.md`.

If there is not an existing `{PHASE2_DIR}/features/feature-<feature-number>-<feature-name>` folder, then run the claude command: `/2.1-prp-from-feature <path-to-feature-discussion>` (defined in `{COMMANDS_DIR}/2.1-prp-from-feature.md`).

### Step 2. Execute the PRP

The `<path-to-prp>` is `{PHASE2_DIR}/features/feature-<feature-number>-<feature-name>/description.md`.

If there is not an existing PR for the feature, then run the claude command: `/2.2-prp-base-execute <path-to-prp>` (defined in `{COMMANDS_DIR}/2.2-prp-base-execute.md`).

Once the feature is implemented, then proceed to step 3.

### Step 3. Create a PR

When you have completed your feature, you should create a PR.
```bash
# Set a timer/reminder to commit regularly
git add -A
git commit -m "feature <feature-number>: <feature-name>"
```