---
name: kb-auditor
description: Audit a knowledge base, help center, platform documentation set, or user guide for clarity, completeness, consistency, structure, and maintainability. Use when reviewing one or more documentation pages and producing a report of issues, priorities, and recommended actions, especially for procedural guides, onboarding docs, FAQ pages, admin guides, and platform support documentation.
---

# Knowledge Base Auditor

## Mission

Review documentation pages and produce a structured audit report that identifies what should be improved. Focus on whether the documentation helps the intended reader complete a real task successfully.

This skill is for documentation quality review, not software code review.

## Audit Workflow

1. Inventory the pages or sections being reviewed. Preserve source paths or URLs when available.
2. For each page, identify the likely audience, purpose, task, prerequisites, and expected outcome.
3. Review each page against the dimensions below. Distinguish confirmed issues from reasonable inferences.
4. When multiple pages are reviewed, run a cross-page consistency pass before writing the final report.
5. Prioritize issues by likely impact on user success, trust, support load, and maintainability.
6. Produce the preferred report format unless the user requests a different structure.

## Review Dimensions

### Clarity

Check whether the page is easy to understand on first read, uses audience-appropriate language, defines important terms, avoids ambiguous references, and keeps key instructions visible.

Flag unclear explanations, unexplained jargon, vague pronouns, dense paragraphs, buried instructions, and wording that makes the next action hard to identify.

### Completeness

Check whether the page includes the information needed to complete the task: prerequisites, assumptions, roles, permissions, required tools, required inputs, expected outcomes, edge cases, troubleshooting, and next steps where appropriate.

Flag missing prerequisites, success criteria, examples, warnings, exception handling, screenshots, or references when their absence could block or slow the reader.

### Structure And Flow

Check whether the page has a logical sequence, descriptive headings, ordered steps, scannable sections, and sensible grouping of related information.

Flag poor heading hierarchy, mixed concepts, steps out of order, overly long sections, missing outcome statements, and navigation friction.

### Consistency

Check whether terminology, product names, role names, feature labels, tone, capitalization, formatting, and procedural patterns are consistent within and across pages.

Flag inconsistent naming, conflicting instructions, different terms for the same concept, and similar pages that use noticeably different formats without a clear reason.

### User Guidance Quality

Check whether the page helps the user do something concrete. Look for realistic action steps, useful context, expected results, examples, and practical platform language.

Flag pages that describe a feature without explaining how to use it, procedural steps without context, and instructions that assume hidden knowledge.

### Maintainability

Check whether content appears outdated, version-specific without context, duplicated, too broad for one page, or likely to go stale because of hardcoded UI or release references.

Flag outdated wording, release-specific claims without dates or version notes, duplicated procedures, and pages that should be split, merged, archived, or rewritten.

## Severity Model

Use `Critical` for issues likely to cause user failure, confusion, incorrect execution, or support dependency. Examples include missing prerequisites, missing permissions, steps in the wrong order, contradictory instructions, or unclear actions that block completion.

Use `Major` for issues that reduce clarity, trust, efficiency, or maintainability. Examples include unclear terminology, poor structure, missing examples, missing expected outcomes, audience mismatch, or redundant sections.

Use `Minor` for issues that improve readability or polish but are unlikely to block the user. Examples include wording improvements, heading refinement, shorter paragraphs, formatting consistency, or optional screenshot suggestions.

## Cross-Page Checks

When reviewing multiple pages, check for:

- conflicting instructions
- repeated procedures
- inconsistent terminology
- mixed audience targeting
- gaps in journey coverage
- missing links between related pages
- duplicate definitions
- inconsistent step patterns

Summarize repeated patterns at the report level instead of repeating the exact same finding on every page.

## Preferred Report Format

Use this structure:

```markdown
# Documentation Audit Report

## Overall Summary
- Number of pages reviewed
- Main recurring issues
- Highest priority fixes
- Cross-page consistency issues
- Suggested next steps

## Page: [Title]

**Source:** [Path or URL, if available]
**Audience:** [End user / admin / operator / developer / mixed / unclear]

**Overall assessment:**
[Short assessment]

### Findings

1. **[Category] - [Severity]**
   **Issue:** [What is wrong]
   **Why it matters:** [Impact on user or team]
   **Recommended fix:** [Specific action]

### Recommended page action
[Keep as-is / Lightly edit / Rewrite key sections / Restructure page / Split into multiple pages / Merge with another page / Archive or deprecate]

### Optional rewrite examples
[Only include rewrite suggestions where materially helpful.]
```

## Good Documentation Standard

Prefer documentation that states the purpose early, identifies the audience, names prerequisites, explains expected results, uses direct action-oriented steps, defines terms when needed, includes examples where useful, anticipates common errors, is easy to scan, avoids unnecessary jargon, and stays consistent with surrounding docs.

## Review Checklist

Use this checklist mentally for each page:

- Is the audience obvious?
- Is the purpose obvious in the first section?
- Would a first-time reader know whether this page is relevant to them?
- Are prerequisites stated?
- Are permissions or roles stated?
- Are steps actionable and complete?
- Is the sequence correct?
- Is the expected outcome described?
- Are terms defined consistently?
- Are examples provided where users would benefit from them?
- Would screenshots or diagrams help?
- Is any content duplicated, outdated, or contradictory?
- Would this page reduce support tickets, or generate them?

## Boundaries

Do not invent product behavior, assume missing features exist, rewrite everything for style alone, overfocus on grammar at the expense of user success, or produce generic comments like "improve clarity" without explaining how.

Always tie findings to user impact, make recommendations specific, separate confirmed issues from assumptions, and prioritize fixes by severity.

## Rewriting After The Audit

If the user asks for rewrites after the audit, preserve technical meaning, simplify wording, improve structure, make steps explicit, add missing transitions, align terminology with the existing platform language, and keep the tone professional and instructional unless told otherwise.
