---
name: easier-paper
description: Guide beginners through progressively complete research-paper readings in clear Chinese, from the main story to methods, details, evidence, and limits. Use for paper-reading conversations; not for citation formatting or translation-only requests.
---

# Easier Paper

Build a defensible understanding of a paper, not a polished but shallow summary. Explain in the reader's language, retain essential English terms, and define them on first use.

## Core rules

1. Establish scope before promising depth. Treat “read/understand this paper” and “deep reading” as requests for complete paper coverage unless the user asks for a quick scan. A method diagram, figure, formula, or named module is a local request unless the user asks for a whole-paper map.
2. Build a provisional map from the abstract, introduction, overview figure, conclusion, and key experiments; then verify it against methods, figures, tables, appendices, and definitions.
3. Trace every important claim to a page, section, figure, table, equation, or appendix. Label it as a paper fact, author interpretation, background knowledge, or learning inference.
4. Preserve the reasoning chain: problem, design rationale, input-to-output transformation, supporting evidence, and conclusion boundary.
5. Make saved artifacts checkable: readable layout, source locations, correct units and metrics, clear distinction between source and redrawn figures, and openable files.

Read [Rigor Protocol](references/rigor-protocol.md) for long explanations, generated files, method analysis, evidence review, figures, or reproduction work.

## Reading scope is not explanation scope

Choose how much source material to inspect from what is needed to answer the request, independently from how much the user wants explained.

- For a whole-paper request, first explain the main line, then progressively cover every substantive mechanism and its supporting details: inputs and preprocessing, representations, intermediate operations, training or inference, assumptions, conditional paths, small but consequential components, experiments, and limitations. Tie each detail back to the main line. An opening overview is the start of the explanation, not its completion.
- Keep a coverage map while teaching. Before calling the reading complete, account for the paper's meaningful sections, figures, tables, and appendices; explain what each adds or why it does not affect the paper's claims. Do not silently omit a side mechanism because it is absent from the architecture diagram or seems too implementation-specific.

- For a local figure, formula, method, or diagram, start with the target item, its caption, and the directly referenced method paragraph.
- Expand only when a key definition, assumption, symbol, control, or evidence link is missing. Read the smallest additional passage that resolves that gap.
- For an explicitly local question, reading extra context does not require a longer answer. Explain the requested object and any prerequisite needed to understand it.
- Use a whole-paper reading only for a whole-paper question, a requested full map, or when the local item cannot be interpreted reliably without broader context.

## Reading modes

Select a mode automatically from the user's request, or honor an explicit choice. Both modes preserve the same evidence standard and beginner-friendly language.

| Mode | Default use | Focus |
| --- | --- | --- |
| **Learning mode** | Default | Complete paper coverage in manageable stages, using plain language and only the mathematics needed to understand each mechanism |
| **Deep mode** | “Deep mode”, “rigorous”, “full method”, or a request for formulas/derivation | The same coverage with systematic input–representation–operation–output traces, equations, assumptions, objectives, ablations, metrics, failure conditions, and conclusion boundaries |

Neither mode includes a code walkthrough unless the user explicitly asks for code. If implementation must be inspected to settle a paper claim, explain the finding in conceptual terms without turning the lesson into code analysis.

## Route the current request

| User signal | Route | This-turn outcome |
| --- | --- | --- |
| What is this paper about? Is it relevant? | Orientation | Topic, gap, method, main finding, reading path |
| Read it with me / Deep read it | Guided reading | Main line first, then all substantive mechanisms, evidence, conditions, and limits in natural units |
| What is X? Why do this? | Concept rescue | Plain explanation, minimal example, paper role |
| I cannot read this figure, formula, or method | Local breakdown | Purpose, inputs, outputs, logic, conclusion, limits |
| Is it reliable or innovative? | Evidence review | Claim–evidence map, alternatives, limitations |
| How does it connect to another paper or my work? | Connection | Common structure, differences, transferable ideas |

When only a paper is supplied, begin with a medium-depth paper map: research tension, prior limitation, inputs/outputs, central mechanism, experimental support with one concrete result, value, and stated limitation. Continue from that map into the remaining mechanisms and evidence; options may change the order or emphasis, but must not turn unvisited details into optional omissions.

## Explain for beginners

For each difficult point: state the everyday problem; give one brief analogy or example; map it back to the paper precisely; add only the necessary prerequisite vocabulary; and check understanding with one answerable question. An analogy is not evidence and must not conceal a material mismatch.

Read [Evidence and Explanation Boundaries](references/evidence-and-explanations.md) for claims, figures, and external material. Read [Mode Routing](references/mode-routing.md) if the request is ambiguous.

## Built-in modules

Choose modules automatically; users do not need to name a module or external skill.

| Situation | Module | Outcome |
| --- | --- | --- |
| Complex paper or many figures | Reading map | Problem, method path, mechanism, experiments, synthesis |
| Blocking formula, module, or experiment | Deep explanation | Terms, assumptions, inputs, outputs, and evidence boundary |
| Review, writing, comparison, or project planning | Academic transfer | Outline, comparison, research question, or reproduction plan |
| Code, data, statistics, plotting, or citation verification | Research workbench | Validated computation, figure, or retrieval result |
| Architecture needs more than text | Editable figure design | Diagram specification and editable-native deliverable where available |
| Reader cannot identify the obstacle | Read-aloud diagnosis | One small concept at a time and adaptive checks |
| Static media cannot show a mechanism | Dynamic mechanism demonstration | Minimal controllable animation tied to paper operations |

Read [Integrated Capabilities](references/integrated-capabilities.md) when selecting or delivering a module.

## Learning ladder and delivery gate

After the opening map, work through architecture, mechanism, evidence, and boundaries until the coverage map is complete. A response may stop at a natural teaching boundary, but name the next uncovered unit and never present the overview as the whole reading. Before finishing, ensure the reader can state why the paper exists, what it does, how its important parts work together, and what supports or limits its conclusion. Mark unavailable source material and never fabricate detail.

## Conversation learning map

Starting with the second turn of a paper-reading conversation, end every response with a compact Markdown table titled `相邻概念导航`. First state the turn's one overall learning theme in a short line, then use the table to show its immediate learning neighborhood.

- Do not add the table in the first substantive reply about a paper; build the initial map first.
- Include the 2–5 concepts most directly adjacent to the overall learning theme, chosen from prerequisites, components, causes, consequences, contrasts, or common confusions. Do not dump a broad glossary.
- Use three columns: `相关概念`, `它在本轮主题中的位置`, and `理解后能推进什么`. Do not repeat the current concept in every row or present the table as a one-to-one comparison.
- Keep the overall theme and its neighbors concrete to this paper. Mark an adjacent concept as already explained when appropriate; otherwise make the third column state the specific gap it will close.
- The table is navigation, not evidence: retain normal source locations and fact-vs-inference labels in the explanation itself.

<!-- 中文注释：整篇论文阅读先讲主线，再逐步讲全重要机制、边角但有影响的组件、条件、证据和局限；学习模式与深度模式区别在数学和分析深度，不在覆盖是否完整。默认不讲代码。明确的局部问题仍聚焦当前对象及必要前提。 -->
