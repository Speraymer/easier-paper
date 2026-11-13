# Rigor Protocol

Use this protocol for long explanations, generated artifacts, method analysis, evidence review, figures, or reproduction work. It sets decision standards; it does not override the user's current goal.

## Modes

| Mode | Minimum completion | Do not |
| --- | --- | --- |
| Scan | Problem, gap, method, one result, limitation, next section | Present a scan as deep reading |
| Full reading | Main-line map followed by coverage of substantive mechanisms, side conditions, evidence, and limitations | Treat an opening map or only the headline modules as a completed reading |
| Review | Claim–evidence matrix, alternatives, concrete evidence request | Substitute generic criticism for analysis |
| Research transfer | Transferable assumptions, methods, evidence, and non-transfer conditions | Call an idea directly reusable without qualification |

Within either Scan or Full reading, **Deep mode** requires an explicit chain from inputs to representations, operations, outputs, objectives/equations, and evidence. Include assumptions, units or tensor/variable shape where relevant, training or inference stages, ablations, metrics, and failure conditions. Do not substitute a code walkthrough for this chain; inspect implementation internally when it determines the interpretation of a reported result, and include code only on explicit user request.

With an abstract, low-resolution image, or incomplete PDF, complete only the supportable portion and state the limitation first.

## Paper-type routing

- **Systems/engineering/robotics:** inputs, sensors/data, state representation, interfaces, optimization/control loop, latency, resources, failure modes.
- **Machine learning:** task, data splits, preprocessing, train/validation/test isolation, baselines, metrics, ablations, leakage, generalization boundary.
- **Theory:** definitions, assumptions, propositions/theorems, proof strategy, conditions, counterexamples; intuition is not proof.
- **Experimental science:** sample, variables, controls, measurement, statistics, repetitions, error, and the evidence chain.
- **Clinical/observational studies:** population, eligibility, exposure/intervention, outcome, confounding, effect size, confidence interval; correlation is not causation.
- **Reviews/meta-analyses:** scope, search and inclusion logic, evidence type, heterogeneity, author position, and field consensus.

Maintain a minimal evidence ledger for each important item: claim, direct evidence, source location, support strength, and what it does not establish. Never estimate exact values from low-resolution curves, treat a proxy as a direct measure, present simulation as experimental validation, equate statistical significance with practical importance, or call missing evidence evidence of absence.

## Methods, artifacts, and learning loop

Explain methods in the paper's order: goal, objects/assumptions, mechanism, connections, inputs/outputs, training/inference, cost, and applicability. In full reading, also cover conditional branches and smaller components that change how the method works or how evidence should be interpreted; link them to the main path. Keep only essential equations, explaining variables, units/conditions, objectives, weights, and constraints. For a figure, state its question before panels, axes, units, controls, trends, errors, and sample size; then separate what it supports from what it cannot support. For a local request, inspect the figure or formula, caption, and directly relevant method text first; broaden source inspection only when a required definition, assumption, or evidence link is absent. Do not broaden the user-facing explanation merely because more source context was read.

For generated HTML/PDF, ensure readable layout, source locations, distinction between source/redrawn material, and successful rendering. For editable figures, use editable text, shapes, and connectors and check direction, overlap, alignment, print legibility, and opening. For scientific computing, inspect sources/units, run a minimum verification, and protect source data. If a full reading is unfinished, identify the next uncovered architecture, mechanism, or evidence unit; options may change the order, not end the reading early.

<!-- 中文注释：完整阅读先给主线，再讲全有实质作用的机制、边角条件、证据与局限；深度模式额外系统追踪公式和实验控制，默认不讲代码。局部问题先检查目标、图注和相关方法段，只补必要前提。 -->
