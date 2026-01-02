# Experiment: <Short, Descriptive Title>

**Status:** Proposed | Running | Completed | Abandoned  
**Date Started:** YYYY-MM-DD  
**Owner:** <Person or role>

---

## Hypothesis

State the hypothesis being tested.

This should be a falsifiable statement, not a goal or aspiration.

Example:
> Providing agents with an explicit execution surface will reduce unsafe or invented command behavior compared to free-form execution.

---

## Motivation

Explain why this experiment is worth running.

Include:
- what uncertainty this experiment is intended to reduce,
- why existing evidence is insufficient,
- and how the outcome could influence future decisions.

---

## Scope and Constraints

Define the boundaries of the experiment.

Include:
- systems or components involved,
- permissions or capabilities granted,
- data sources used,
- and anything explicitly out of scope.

If the experiment cannot fail safely within these constraints, it should not proceed.

---

## Experimental Setup

Describe how the experiment will be conducted.

Include:
- configuration details,
- relevant context supplied to agents,
- execution surfaces or workflows used,
- and any instrumentation or observation mechanisms.

This section should be specific enough to allow reproduction.

---

## Success and Failure Criteria

Define how outcomes will be evaluated.

Include:
- what constitutes success,
- what constitutes failure,
- and what ambiguous or mixed results would mean.

Avoid vague criteria such as “felt better” or “seemed to work.”

---

## Observations and Results

Record what actually happened.

Include:
- observed behaviors,
- unexpected outcomes,
- notable failures or edge cases,
- and any deviations from the planned setup.

This section should be descriptive, not interpretive.

---

## Analysis

Interpret the results.

Address:
- whether the hypothesis was supported or refuted,
- what factors may have influenced the outcome,
- and limitations of the experiment.

This is where insight is extracted from observation.

---

## Decision and Next Steps

State the outcome of the experiment.

Examples:
- Promote to practice
- Iterate with changes
- Abandon approach
- Gather additional evidence

If promotion is recommended, reference the ADR that will capture the decision.

---

## Related Artifacts

Link to:
- relevant ADRs,
- playbook sections,
- templates,
- or prior experiments.

This helps situate the experiment within the broader system.