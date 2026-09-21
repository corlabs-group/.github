# Corlabs Workflow

This document defines the common development workflow for Corlabs projects.

The goal is simple:

**ChatGPT helps define → GitHub organizes → OpenCode implements → Code is the source of truth.**

---

## Work Structure

### Epic

An Epic represents a **finite product goal** that requires multiple Issues.

Examples:

* `Enable Online Reservations`
* `Enable Club Following`
* `Improve User Onboarding`

Use the `Epic` Issue Type.

Epics may span multiple Sprints and are not Sprint-sized units of work.

### Issue

An Issue represents a **concrete unit of work** tracked in GitHub.

Every Issue must use the appropriate **Issue Type**:

* `Feature` — new or improved product behavior.
* `Bug` — existing behavior that works incorrectly.
* `Task` — concrete technical, operational, maintenance, documentation, or infrastructure work.
* `Spike` — time-boxed investigation used to reduce uncertainty or inform a decision.
* `Epic` — a larger, finite goal that groups related work and may span multiple Sprints.

`Feature`, `Bug`, and `Task` should normally represent work that can be completed within one Sprint.

A `Spike` should have a clear question, scope, and expected outcome rather than implementation as its primary goal.

An `Epic` is not a Sprint-sized unit of work. It may contain related Issues, but not every Issue needs to belong to an Epic.

---

## Workflow

```text
Idea / Problem
      ↓
   ChatGPT
      ↓
   Backlog
      ↓
  Refinement
      ↓
    Ready
      ↓
Sprint Planning
      ↓
Current Sprint
      ↓
In Progress
      ↓
  In Review
      ↓
    Done
```

### Backlog

Create an Issue when something is worth tracking.

It does not need to be fully defined yet.

### Ready

Move an Issue to `Ready` when it has:

* Clear goal
* Acceptance Criteria
* Priority
* Story Points (`1 / 2 / 3 / 5 / 8`)
* Parent Epic and Milestone, when applicable

**Ready = it can be implemented now.**

### Current Sprint

During Sprint Planning:

1. Define the Sprint Goal.
2. Select `Ready` Issues that contribute to it.
3. Assign them to the current Iteration.

During development:

`Ready → In Progress → In Review → Done`

Work on **one Issue at a time** whenever possible.

---

## Planning Model

`Milestone` = release or delivery goal
`Area` = permanent product capability
`Epic` = finite product goal
`Iteration` = Sprint / when work happens
`Issue` = executable unit of work

Example:

```text
Milestone: MVP

Area: Reservations

Epic: Enable Online Reservations
├── Issue: Add reservation form
├── Issue: Validate availability
├── Issue: Create reservation endpoint
└── Issue: Send reservation confirmation
```

---

## Tools

### ChatGPT

Think, research, make decisions, and define work.

Not every idea needs to become an Issue.

### GitHub

The persistent system for planning and tracking work:

**Roadmap → Epics → Backlog → Sprint → Pull Requests**

### OpenCode

Takes an Issue, inspects the current codebase, plans the implementation, and implements the change.

### Code and Migrations

The current code and migrations are the **source of truth for what is actually implemented**.

---

## Rules

1. **One thing at a time.**
2. **New idea → Backlog.**
3. **Ready = ready to implement.**
4. **Epic = finite goal.**
5. **Iteration = when we work on it.**
6. **Milestone = which release it belongs to.**
7. **Done = actually finished.**
8. **Keep it simple.**

---

## Development Flow

```text
ChatGPT defines
      ↓
GitHub organizes
      ↓
OpenCode implements
      ↓
Pull Request
      ↓
Merge
      ↓
Done
```
