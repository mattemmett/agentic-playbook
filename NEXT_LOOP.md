# Next Loop: Article Intake, Evaluation, and Adoption

This file captures the **next operational loop** for applying the Agentic Playbook to real-world research, tools, and frameworks.

It exists to bridge doctrine and practice without forcing premature conclusions.

---

## Goal

Systematically evaluate new articles, frameworks, and vendor approaches to agentic development and AI-assisted engineering, with the intent to:

- test claims through controlled experiments,
- assess alignment with existing doctrine,
- decide what to adopt, reject, or modify,
- and produce concrete, reusable implementations where justified.

This work supports both ongoing research and real-world organizational adoption.

---

## High-Level Workflow

```
Read
 ↓
Intake Note
 ↓
Experiment (if warranted)
 ↓
Decision (ADR, if commitment is made)
 ↓
Template (if adoption is justified)
```

Not all items progress through every stage. Most stop early by design.

---

## Step 1: Intake Articles and Research

For each article or framework reviewed:

- Create a single note under `notes/`
- Keep the intake lightweight and honest

Suggested structure:

- Key claims (max 3)
- Operational implications
- Tensions with the playbook
- One-sentence test idea

Most articles should stop here.

---

## Step 2: Run Experiments Where Behavior Matters

Promote an article to an experiment when:

- it proposes a new workflow, context model, or execution pattern
- claims cannot be evaluated purely through reasoning
- behavior and outcomes matter more than explanation

Use `templates/EXPERIMENT_TEMPLATE.md`.

Focus on:
- observable behavior
- reproducibility
- failure modes
- impact on developer productivity and correctness

---

## Step 3: Record Decisions Explicitly

Write an ADR only when:

- a real commitment is made
- a boundary or constraint is adopted
- an approach is explicitly accepted or rejected

ADRs prevent thrash and institutional amnesia.

Use `templates/ADR_TEMPLATE.md`.

---

## Step 4: Package Successful Approaches

When an approach proves effective and stable:

- produce a concrete, vendor-specific template
- document how it maps back to the playbook
- clearly label scope and assumptions

Templates are opinionated and intentionally constrained.

---

## How to Decide: Doctrine vs Template

- **Doctrine** changes rarely and only for new invariants
- **Templates** encode concrete implementations
- **Experiments** test claims
- **Notes** absorb uncertainty

Tool-specific mechanics belong in templates, not the playbook.

---

## Adoption Lens (Organizational Reality)

When evaluating approaches, consider:

- Does this produce measurable improvement?
- Does it reduce implicit context or increase it?
- Does it constrain execution safely?
- Can it be explained and taught?
- Can skeptics be shown results, not promises?

Belief is not required. Evidence is.

---

## Immediate Next Actions (When Time Allows)

- Create `notes/READING_QUEUE.md`
- List currently open articles and sources
- Start with the GitHub Copilot agentic workflows article
- Decide whether it warrants an experiment

No urgency. No pressure.

This loop is designed to run continuously.
