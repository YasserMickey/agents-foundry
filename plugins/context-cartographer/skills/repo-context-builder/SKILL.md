---
name: repo-context-builder
description: Explore an existing repository, infer how it works from the codebase itself, and create or update a root-level PROJECT_CONTEXT.md for future engineers or AI sessions. Use when the user wants onboarding context before implementation, review, or planning work begins.
---

# Repo Context Builder

## Mission

Your first job is to understand the repository well enough to leave behind a practical onboarding document that future work can rely on.

This skill is for existing projects, not greenfield builds. Treat the codebase as the primary source of truth and avoid asking the user to explain the system unless a blocker genuinely cannot be discovered locally.

## Core Outcome

Create or update a root-level `PROJECT_CONTEXT.md` that gives a future engineer or AI enough context to start meaningful work quickly.

## Operating Rules

- inspect before you infer
- prefer verified evidence from the repo over assumptions
- label uncertain conclusions clearly
- do not modify product code, configs, or infrastructure unless the user explicitly asks
- do not broaden the task into implementation work
- after updating `PROJECT_CONTEXT.md`, pause for the next instruction unless the user asked for more

When useful, distinguish findings as:

- `Verified`: directly confirmed from files, commands, or executable config
- `Inferred`: a strong but unconfirmed conclusion drawn from repo evidence
- `Unknown`: not discoverable from current access

## Investigation Phases

### 1. Repository Surface Scan

Inspect:

- repository structure
- top-level docs
- config files
- scripts
- entry points
- package manifests
- deployment or environment files when present

### 2. Tooling and Workflow Mapping

Identify, where possible:

- language and framework choices
- runtime and package manager
- build system
- lint and formatting setup
- test setup
- local development workflow
- CI or deployment hints

Do not guess commands when they cannot be confirmed. If a command is only implied, mark it as inferred.

### 3. Product and Architecture Inference

Infer what the project appears to do by reading:

- routes and controllers
- UI structure
- service boundaries
- schemas and models
- integration code
- background jobs or workers
- domain naming and conventions

Map the major modules and explain how the important pieces connect.

### 4. Operational Constraints

Surface blockers and prerequisites such as:

- environment variables
- databases
- credentials
- external APIs
- local services
- queues, caches, or storage systems
- monorepo workspace dependencies

### 5. Risk and Maintainability Pass

Identify:

- fragile or high-coupling areas
- outdated or contradictory docs
- likely technical debt
- areas that seem difficult to test
- places where future contributors may make incorrect assumptions

## Required Output File

Write findings into `PROJECT_CONTEXT.md`.

Keep the file concise, practical, and evidence-based. Optimize for fast onboarding, not exhaustive narration.

Include these sections:

- Project Summary
- Quick Start
- What The Project Appears To Do
- Tech Stack And Tooling
- Repository Structure
- Key Entry Points
- Main Architectural Flows
- Run / Build / Test / Lint Commands
- Environment Variables And External Dependencies
- Conventions And Patterns
- Risks / Fragile Areas / Technical Debt
- Unknowns / Assumptions
- Suggested Next Investigation Steps

If the repository is a monorepo or multi-service system, document each app or service separately where that improves clarity.

## Writing Guidance

- keep the strongest facts near the top
- use short, durable language
- make unknowns obvious
- avoid speculative implementation advice unless it helps future onboarding
- prefer commands and paths exactly as found in the repo
- if enough information exists, keep `Quick Start` actionable

## Response Back To The User

After updating `PROJECT_CONTEXT.md`, give a short summary covering:

- what the project appears to be
- the most important confirmed tooling details
- any blockers or unknowns that prevent full verification

Then wait for the next instruction.
