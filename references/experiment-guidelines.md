# Experiment Guidelines

Use these rules when planning, running, extending, or diagnosing publication-oriented computational, laboratory, prototype, hardware, or field experiments across engineering disciplines. Apply only the parts relevant to the study type.

## Match the design to the study

Identify the research question, response variables, controllable factors, controls or comparators, operating range, and evidence needed for the claim before expanding the experiment.

- For computational and numerical studies, check the implemented equations or method, initial and boundary conditions, solver settings, and only the convergence, discretization, or mesh sensitivity needed for the claim.
- For laboratory and bench studies, check the apparatus, materials or specimens, control condition, factor levels, instrument range and resolution, calibration when material, and environmental conditions that affect the response.
- For prototype, hardware, and field studies, check interfaces, timing, operating envelope, reference measurements, relevant environmental variation, and necessary safety controls.
- For mixed hardware-software studies, verify that firmware, software, configuration, clocks, units, and physical interfaces correspond to the intended test condition.

Do not turn these examples into a universal checklist. Select the design elements that can materially affect the current conclusion and follow normal conventions for the field.

## Select validation by claim

Use three proportional levels:

1. **Operability:** confirm the relevant code, model, apparatus, or procedure runs and produces usable data without an obvious failure.
2. **Experimental sanity:** confirm the intended method or treatment, control, sample or specimen, conditions, units, instrumentation, factors, responses, and data reduction relevant to the request.
3. **Claim-critical validity:** check conditions that could change the conclusion. Examples include fair comparisons, material calibration, measurement uncertainty, repeatability, conservation or dimensional sanity, and numerical convergence. Do not add all of them when they are irrelevant.

Use targeted checks first. Broaden only when the changed component has wider impact. Do not rerun every model, specimen, operating point, replicate, method, output, or full test suite for a localized plotting, analysis, or configuration change.

## Handle blockers

Treat an issue as a hard blocker only when the next run would be unusable, unsafe, or misleading: missing materials or corrupt data, failed apparatus or code, wrong method, treatment, specimen, or control, materially wrong conditions, invalid metrics or measurements, consequential invalid values, unit or coordinate errors, leakage, or an unfair comparison.

Treat audit completeness and unrelated engineering quality as soft unless the user or project makes them part of the task.

## Record reproducibility information

Retain the information needed to understand and repeat the study: relevant configuration or model version, materials and specimen preparation, apparatus or instrument settings, calibration when material, initial and boundary conditions, operating conditions, factor levels, controls or comparators, meaningful repeats or random seeds, response definitions, analysis method, and results. Reuse existing configuration files, lab records, tables, logs, or data formats. Do not construct a parallel provenance system.

Preserve existing infrastructure and formats. Keep a current manifest compatible if the repository already uses one; do not delete it or create another manifest without need.

## Use repeats and randomness normally

Distinguish independent experimental replicates, repeated measurements on the same sample, and stochastic computational runs. Use the type and number that the research question and field convention require; do not treat them as interchangeable.

Run requested random seeds directly and aggregate the requested metrics. Do not create seed hashes, lineage, registries, immutable records, integrity stages, or a seed audit.

Use enough repeats or seeds to support the claim and match field convention. Do not increase the count by reflex when a result is weak. For scarce, destructive, or expensive specimens, use an efficient design and state the resulting limitation rather than pretending the evidence is broader.

## Choose statistics from the question

Add a statistical method or uncertainty analysis when the user requests it, the design requires it, comparable publications normally require it, or omission would leave the claim unsupported. Use error bars and uncertainty terms that correspond to their stated source—such as replicate variability, standard error, confidence interval, instrument uncertainty, or propagated measurement uncertainty. Do not infer significance from descriptive improvement, and do not automatically apply multiple-comparison correction because several groups exist.

## Choose controls, comparators, and ablations

Use the field's appropriate comparison: control or reference condition, standard method, analytical solution, accepted numerical model, commercial instrument, prior design, or canonical baseline. Ensure fair inputs, operating conditions, resource budgets, sample handling, and response definitions. Do not build a benchmark framework just to add one comparator.

Require each component-removal, mechanism-isolation, or ablation test to answer a claim-relevant question. Avoid all component permutations and factorial designs unless the research question demands them.

## Control parameter and robustness experiments

Choose the smallest informative range that covers the stated operating region or hypothesis. Do not automatically cross every load, geometry, material, environment, controller, algorithm, and replicate. Use formal design-of-experiments methods when they efficiently answer the actual multivariable question, not as mandatory ceremony.

When a reviewer requests robustness analysis, identify the specific robustness concern and test that dimension. Do not convert it into a comprehensive audit of the paper.

## Diagnose weak or negative results

Never fabricate, cherry-pick, remove unfavorable seeds, overwrite results, hide failures, or invent significance. Examine, in order:

1. Whether the implementation, apparatus, measurement, or response calculation is wrong.
2. Whether the test conditions can expose the proposed physical or computational mechanism.
3. Whether materials, specimens, parameters, and comparison conditions are fair.
4. Whether the method, model, device, process, or design needs revision.
5. Whether the research question or claim should narrow.

Prefer a scientifically informative negative or bounded result over a cosmetically stronger but unsupported claim. Do not make additional statistics or a large robustness matrix the automatic first response.

## Allocate research resources

Prioritize core novelty, mechanism or method effectiveness, essential controls and comparisons, sensitivity or component studies, applicability range, efficiency, and writing before supplementary robustness and engineering audit. Stop adding work once the requested claim has adequate, conventional support.
