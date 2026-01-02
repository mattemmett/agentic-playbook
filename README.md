# Agentic Development Playbook

*Applied research and practical patterns for agentic software development.*  
*A living playbook capturing how agentic systems are evaluated, designed, and evolved as tools, terminology, and best practices change.*

---

## What This Repository Is

This repository is a **project-agnostic playbook** for agentic software development.

It captures an evolving understanding of how to design, evaluate, and operate agentic development systems in a way that is **durable, explicit, and repeatable**, despite rapid changes in tools, terminology, and best practices.

Rather than focusing on a single framework, vendor, or codebase, this repo exists to document:
- how we *think* about agentic development,
- how that thinking evolves over time,
- and how it translates into reusable patterns and artifacts that can be applied to any project.

This is not a tutorial repo. It is a **living knowledge system**.

---

## Why This Exists

Agentic development is changing quickly:
- terminology shifts (agents, workflows, context, tools, models),
- tooling evolves rapidly,
- examples and articles represent snapshots in time,
- and agents can amplify incorrect assumptions if those assumptions are not made explicit.

Without structure, understanding tends to:
- fragment across projects,
- reset every time tooling changes,
- or collapse into ad-hoc conventions that are hard to explain or defend.

This playbook exists to provide **continuity**:
- a stable place to record current best understanding,
- a clear process for incorporating new research or tools,
- and visibility into *why* certain approaches were adopted or rejected.

---

## How to Use This Repository

This repository is organized around different *types* of knowledge, each with a clear purpose.

### Current Best Understanding
- **`AGENTIC_PLAYBOOK.md`**
  - The authoritative description of the current agentic development approach.
  - Defines core concepts, boundaries, preferred patterns, and anti-patterns.
  - Changes intentionally and relatively slowly.

### Decisions and Rationale
- **`decisions/` (Architecture Decision Records)**
  - Each ADR captures *why* a specific choice was made.
  - Includes context, alternatives, and consequences.
  - Enables backtracking and reassessment when assumptions change.

### Research Intake and Evaluation
- **`intake/`**
  - Raw inputs: articles, tools, papers, links, ideas.
- **`reviews/`**
  - Structured evaluations of new research or tooling.
  - Each review assesses relevance, tradeoffs, and impact on the playbook.

### Experiments
- **`experiments/`**
  - Small, controlled tests of new ideas.
  - Each experiment defines a hypothesis, setup, results, and outcome.

### Reusable Artifacts
- **`templates/`**
  - Project-agnostic templates (e.g., Make patterns, agent workflows, context files).
  - These are intended to be copied into real projects.

### Evolution Over Time
- **`CHANGELOG.md`**
  - A high-level record of how the playbook itself has evolved.
  - Focuses on conceptual changes, not file-by-file diffs.

---

## How Understanding Evolves Here

New ideas are incorporated deliberately, not implicitly.

The general loop is:
1. **Intake** — capture new research, tools, or ideas.
2. **Review** — evaluate claims, scope, and relevance.
3. **Experiment** — test promising ideas in a controlled way.
4. **Decision** — adopt, adapt, defer, or reject.
5. **Update** — reflect changes in the playbook, decisions, templates, and changelog.

Nothing is silently rewritten. Historical context is preserved.

---

## What This Repository Is Not

This repository is **not**:
- a fixed framework you must follow rigidly,
- a vendor-specific guide,
- a collection of one-off scripts,
- or a replacement for project-level documentation.

Instead, it is a **thinking and decision system** that informs how those things are built elsewhere.

---

## Status

This is a living system.

Expect:
- iteration,
- refinement,
- and occasional rethinking as the agentic development ecosystem matures.

The goal is not to be "right forever," but to remain **coherent, explicit, and adaptable** over time.
