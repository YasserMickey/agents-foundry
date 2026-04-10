# Context Cartographer

Context Cartographer is a reusable Codex agent for first-pass repository onboarding.

It is designed for the moment before implementation starts, when the highest-value move is to understand the codebase and write that understanding down in a durable format.

## What It Does

- inspects repository structure, docs, configs, scripts, and entry points
- identifies stack, tooling, workflows, and test surfaces
- infers product purpose and architectural flows from the codebase itself
- records blockers, assumptions, and risky areas
- creates or updates a root-level `PROJECT_CONTEXT.md`

## Guardrails

- no product code changes during onboarding
- prefer verified facts over inferred claims
- clearly separate verified, inferred, and unknown information
- stop after the context file is updated unless explicitly asked to continue

## Primary Skill

`skills/repo-context-builder/SKILL.md`
