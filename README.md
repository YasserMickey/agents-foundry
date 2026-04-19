# Agents Foundry

Agents Foundry is a growing library of reusable Codex agents for exploring codebases, accelerating onboarding, and turning repeatable prompts into shareable workflows.

## Why This Repo Exists

Instead of rewriting the same strong prompt every time, this repository packages proven workflows as installable Codex plugins and skills. Each agent is meant to be:

- practical on day one
- easy to understand and extend
- useful for both humans and future AI sessions

## Current Agents

### Context Cartographer

Maps an existing repository, infers how it works, and creates or updates `PROJECT_CONTEXT.md` without changing product code.

Location: `plugins/context-cartographer`

### KB Auditor

Audits knowledge bases, help center articles, platform manuals, and user guides for clarity, completeness, consistency, structure, and maintainability.

Location: `plugins/kb-auditor`

## Repository Layout

- `.agents/plugins/marketplace.json`: repo-local plugin marketplace for Codex
- `plugins/`: installable plugin packages
- `plugins/context-cartographer/skills/repo-context-builder/`: the first reusable onboarding skill
- `plugins/kb-auditor/skills/kb-auditor/`: documentation audit and remediation reporting skill

## Install In Codex

1. Open this repository in Codex.
2. Point Codex at the repo-local marketplace in `.agents/plugins/marketplace.json` if needed.
3. Install or enable the plugin you want to use.
4. Use the starter prompt from the plugin, or invoke its skill directly.

## Design Principles

- prefer evidence over guesses
- optimize for reusable documentation
- keep code changes out of onboarding work unless explicitly requested
- leave future sessions in a better state than they started

## Planned Next Agents

- architecture reviewer
- bug reproduction scout
- dependency and environment auditor
- test gap mapper

## Publishing Status

This repository is designed to host multiple reusable agents over time, starting with Context Cartographer.
