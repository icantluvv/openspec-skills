# openspec-skills

A collection of AI agent skills for working with [OpenSpec](https://openspec.dev) — a structured change management workflow for software projects.

---

## What is this?

This repo contains skills that extend AI agents (Claude Code, Cursor, Windsurf, and others) with OpenSpec-aware commands. Each skill teaches the agent how to interact with the `openspec` CLI to plan, implement, and archive changes in a structured, spec-driven way.

---

## Skills

### `/openspec-propose`
Create a new change with all artifacts generated in one step: proposal, design, tasks, and a behavioral test plan. Start here when you have an idea and want to move fast.

### `/openspec-apply-change`
Implement tasks from an OpenSpec change. Works through tasks one by one, keeps the test plan in sync, and pauses on ambiguity rather than guessing.

### `/openspec-archive-change`
Finalize and archive a completed change. Checks artifact and task completion, optionally syncs delta specs to main specs, then moves the change to the archive.

### `/openspec-explore`
A thinking-partner mode for exploring ideas before committing to a change. Reads the codebase, draws ASCII diagrams, surfaces risks and unknowns. Never writes code — that's what `/openspec-apply-change` is for.

### `/search-specs`
QA-oriented search over structured requirements in `/spec`. Finds business rules, permissions, edge cases, and acceptance criteria without dumping entire documents.

---

## Requirements

- [OpenSpec CLI](https://openspec.dev) must be installed and available as `openspec`
- An AI agent with skills/rules support (Claude Code, Cursor, Windsurf, etc.)

---

## Structure

```
openspec-propose/        → /openspec-propose skill
openspec-apply-change/   → /openspec-apply-change skill
openspec-archive-change/ → /openspec-archive-change skill
openspec-explore/        → /openspec-explore skill
search-specs/            → /search-specs skill
```

Each directory contains a `SKILL.md` that defines the skill's behavior, steps, and guardrails.
