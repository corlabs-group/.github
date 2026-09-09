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

Use the `epic` label.

Epics may span multiple Sprints and do not have Story Points or Iterations.

### Issue

An Issue represents a **concrete unit of work** that can be completed within a Sprint.

Use one of these labels when applicable:

* `enhancement` — new or improved product behavior.
* `bug` — existing behavior that works incorrectly.
* `documentation` — documentation changes.
* `chore` — maintenance or internal technical work.
* `infrastructure` — infrastructure or operational work.

An Issue may belong to an Epic, but not every Issue needs one.

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
