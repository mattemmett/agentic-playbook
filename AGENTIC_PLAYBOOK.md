# AGENTIC_PLAYBOOK.md

## 1. Purpose and Scope

This playbook describes a practical, evolving approach to **agentic software development**.

In this context, *agentic development* refers to systems where software agents are given the ability to reason, act, and operate across non-trivial boundaries—often involving tools, workflows, and real-world side effects. These systems introduce new leverage, but also new classes of risk and complexity.

The purpose of this playbook is to:
- make assumptions explicit,
- separate durable principles from transient tooling,
- and provide a coherent way to design, evaluate, and evolve agentic systems over time.

This playbook is intentionally **project-agnostic**. It is not a framework, a reference implementation, or a tutorial. It does not prescribe vendors, models, or platforms. Instead, it defines a set of concepts, patterns, and constraints that can be applied across many contexts and organizations.

Non-goals of this playbook include:
- optimizing individual prompts or model outputs,
- providing end-user automation recipes,
- or documenting one-off experiments without context or follow-through.

Where implementation details matter, they are treated as **instantiations of ideas**, not the ideas themselves.

---

## 2. Core Principles

The following principles underpin everything in this playbook. They are intended to remain stable even as tools, models, and workflows evolve.

### Explicit Over Implicit
Agentic systems must be built on explicit assumptions, boundaries, and contracts. Implicit context, inferred behavior, and “the agent will figure it out” are primary sources of failure.

### Separation of Thinking, Decision, and Execution
Reasoning, decision-making, and execution should be treated as distinct phases, even when they are tightly coupled. Conflating these concerns increases risk and reduces observability.

### Stable Execution Surfaces
Agents should act through stable, well-defined execution surfaces (e.g., task runners, scripts, APIs), not by inventing commands or procedures ad hoc. Stability here enables safety, auditability, and reuse.

### Humans Retain Intent and Accountability
Agents can reason and act, but humans retain responsibility for intent, goals, and risk acceptance. Autonomy is a design choice, not a default.

### Evolution Is Designed, Not Accidental
Agentic systems will evolve. The question is whether that evolution is intentional and traceable, or implicit and chaotic. This playbook assumes evolution is part of the system and designs for it explicitly.

---

## 3. The Agentic Development Model

This playbook treats agentic development as a **systems discipline**, not a feature or productivity trick.

At a high level, an agentic system consists of:
- **Agents** — entities capable of reasoning and proposing or taking action,
- **Context** — structured information that constrains and informs reasoning,
- **Workflows** — explicit sequences that govern how reasoning becomes action,
- **Tools** — bounded execution mechanisms with real side effects,
- **Humans** — who define intent, accept risk, and evaluate outcomes.

A critical distinction in this model is between **reasoning authority** and **execution authority**. Agents may reason broadly, but execution authority is deliberately constrained. This asymmetry is intentional: it preserves leverage while limiting blast radius.

The model also assumes that:
- agents operate within systems, not in isolation,
- correctness is contextual, not absolute,
- and failures are often systemic rather than local.

Rather than optimizing for maximum autonomy, this playbook optimizes for **composability, safety, and clarity**. Agentic capability is treated as something to be earned through design, not assumed by default.

---

## 4. Context Engineering

Context engineering is the practice of **intentionally structuring, curating, and supplying information** to agentic systems so that reasoning occurs within known, bounded constraints.

In agentic development, context is not an implementation detail. It is a primary design surface. The quality, structure, and explicitness of context often matter more than the sophistication of the underlying model.

This playbook treats context as something that must be:
- explicit rather than inferred,
- structured rather than incidental,
- and designed rather than accumulated.

---

### 4.1 Types of Context

Not all context serves the same purpose. Conflating different kinds of context is a common source of failure in agentic systems.

This playbook distinguishes between several conceptual categories:

- **Rules and Constraints**  
  Normative boundaries that define what an agent is allowed to do. These include permissions, prohibitions, safety constraints, and execution limits.

- **Knowledge**  
  Relatively stable information about the system, domain, or organization. Examples include architecture descriptions, data models, conventions, and reference material.

- **Memory**  
  Evolving, project- or system-specific information that reflects decisions, state, or history. Memory captures what has changed or been learned over time.

- **Workflow Context**  
  Task-specific structure that governs how reasoning progresses toward action. This includes step sequencing, validation stages, and required approvals.

Treating these categories explicitly enables clearer reasoning, safer execution, and easier evolution.

---

### 4.2 Static vs. Evolving Context

Some context should change rarely. Other context must change frequently.

Static context includes:
- architectural principles,
- domain definitions,
- stable interfaces,
- and long-lived conventions.

Evolving context includes:
- recent decisions,
- ongoing experiments,
- active refactors,
- and temporary constraints.

Blurring this distinction leads to either rigidity (when change is resisted) or instability (when everything is mutable). Effective context engineering makes this distinction explicit and reflects it in how information is stored and supplied to agents.

---

### 4.3 Why Explicit Context Matters

Agentic systems are extremely good at filling in gaps. This is both their strength and their risk.

When context is implicit, agents will:
- infer missing constraints,
- generalize from incomplete examples,
- and optimize toward plausible but incorrect assumptions.

This playbook assumes that **implicit context is a liability**.

Explicit context:
- reduces hallucinated behavior,
- improves reproducibility,
- enables auditability,
- and makes failures diagnosable rather than mysterious.

If an assumption matters, it belongs in context—not in the agent’s imagination.

---

### 4.4 Context as a First-Class Artifact

In this model, context is not embedded casually inside prompts or code. It is treated as a **first-class artifact** with its own lifecycle.

Well-designed context artifacts:
- have a clear purpose,
- declare their scope,
- are referenced rather than duplicated,
- and evolve intentionally over time.

This separation allows:
- workflows to remain stable,
- agents to reason consistently,
- and humans to understand what information informed a given action.

---

### 4.5 Common Context Failures

Several failure modes recur across agentic systems:

- **Context Creep**  
  Gradual accumulation of unrelated or outdated information that degrades reasoning quality.

- **Implicit Contracts**  
  Assumptions that exist only in human heads or past conversations.

- **Overloaded Prompts**  
  Treating prompts as the sole container for rules, knowledge, and workflow.

- **Context Inference as Design**  
  Relying on the agent to “figure out” system structure or constraints.

These failures are systemic, not model-specific. They are addressed through design discipline, not better prompts.

---

### 4.6 Context Engineering as an Ongoing Practice

Context engineering is not a one-time setup. It is an ongoing practice that must evolve alongside systems, teams, and understanding.

As agentic systems grow:
- context must be pruned,
- assumptions must be revisited,
- and artifacts must be reclassified.

This playbook treats context engineering as a continuous responsibility—one that is essential to maintaining safe, reliable, and intelligible agentic systems over time.