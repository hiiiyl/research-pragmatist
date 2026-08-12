# Anti-Pattern Dictionary

Use this reference to recognize whether a proposed action advances the research question or merely adds ceremony. Reject the action by default when it matches an anti-pattern and lacks a concrete need.

## Audit creep

Do not let a normal experiment grow into `audit -> freeze -> register -> hash -> gate -> validate -> report`. Run the experiment with ordinary configuration and result records.

## Scope creep

Do not continue refactoring, documenting, testing, or adding experiments after the requested outcome is sufficiently complete. Keep unrelated modules, filenames, formats, and repository structure unchanged.

## Validation inflation

Do not add checks merely because more checking is possible. Require each check to detect a plausible error that affects the present task or claim.

## Reproducibility theater

Do not confuse abundant provenance artifacts with scientific reproducibility. Prefer preserving the materials or specimens, apparatus or model, relevant settings and conditions, repeats or seeds when meaningful, responses, analysis, and results needed to repeat and interpret the experiment.

## Defensive writing

Do not turn a paper into a response to imagined reviewers. Avoid repeated constructions such as “to rule out any concern” or “we additionally verify” unless they introduce evidence for an actual research question.

## Infrastructure inflation

Do not build registries, databases, servers, leaderboards, governance layers, CI systems, or long-lived platforms for a one-off paper experiment unless the user asks or the project already requires them.

## Abstraction inflation

Do not wrap a small research change in managers, factories, dependency injection, plugin systems, generic interfaces, or layers intended for hypothetical future use. Add an abstraction only when it reduces current complexity or duplication.

## Statistical overkill

Do not automatically add Holm, Bonferroni, FDR, bootstrap intervals, permutation tests, equivalence tests, or Bayesian analysis. Select statistics from the design and claim, not from a desire to appear rigorous.

## Experiment matrix explosion

Do not expand one requested factor into every combination of load, geometry, material, environment, operating point, model or method, and replicate. Run the smallest design that answers the stated question.

## Documentation inflation

Do not create AUDIT, EVIDENCE, GATE, VALIDATION, PROVENANCE, COMPLIANCE, or similar Markdown files by default. Update an existing useful document only when the task needs it.

## Warning escalation

Do not turn a non-impacting warning, unlocked non-core package version, missing hash, or untested irrelevant edge case into a blocker. Explain it briefly if it matters and continue.

## Reviewer-defense matrix

Do not add weak, redundant, artificial, or irrelevant controls, reference methods, or baselines solely to anticipate every possible objection. Add comparisons that answer a real research question.

## Disguised recurrence

Judge behavior, not filenames. Renaming a registry to an index, an audit to a review, or a gate to a readiness check does not make unnecessary machinery useful.
