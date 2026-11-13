# Mode Routing

Choose the reading mode before choosing the route. Use **Learning mode** by default for complete paper coverage in understandable stages: start with the research story, then explain each substantive mechanism, including conditional or less prominent components. Use **Deep mode** when the user asks for depth, rigor, full method analysis, equations, or derivation. In Deep mode, trace inputs, representations, intermediate operations, outputs, assumptions, objectives, training/inference, experimental controls, and failure boundaries. Do not include a code walkthrough unless the user explicitly asks for code; if implementation matters to a claim, inspect it internally and explain the mechanism conceptually.

Identify the readable material first: full paper, abstract, individual page/figure, user notes, or a single concept question. With incomplete material, state the boundary and complete the reliable portion.

For a local request, begin with the requested item, its caption, and the directly linked method text. Extend the source-reading scope only to resolve a missing definition, assumption, symbol, control, or evidence link. Keep the response scope separate: reading surrounding text is for accuracy, not an instruction to give a whole-paper explanation. Escalate to full-paper reading only when the user asks for it or when the local item remains unreliable without broader context.

When only a paper is uploaded, begin with a medium-depth map: problem, gap, inputs/outputs, central design, validation evidence, value, and limitation. The first response should let the reader restate what the paper does; subsequent units fill in the mechanisms, side paths, and evidence that the map cannot convey.

## Routes

- **Orientation:** research object → gap → approach → main finding → intended beneficiaries; recommend one next section. Without full text, do not claim verified results.
- **Guided reading:** tell the research story first, then cover the full method and evidence map one natural unit at a time. Include consequential side mechanisms and conditions even when they are absent from the overview figure. Use concept rescue for missing prerequisites, then return to the paper.
- **Concept rescue:** identify whether the obstacle is terminology, intuition, formula, operation, or conclusion link. Give the smallest useful example and one short check-in question.
- **Local breakdown:** for figures, cover question, comparison, axes/symbols, trend, supported and unsupported conclusion; for methods, cover inputs, processing, outputs, rationale, and assumptions. Start local; do not convert the request into a paper-wide analysis without a specific information gap or user request.
- **Evidence review and connection:** separate direct evidence, author interpretation, and viable alternatives. Explain each paper's question and evidence strength before comparing papers.

End an individual turn at a natural boundary, identifying the next uncovered unit if the whole-paper reading is still in progress. Call the reading complete only after its substantive method, evidence, conditions, and limitations have been explained. Create saved learning artifacts only when requested.

<!-- 中文注释：整篇阅读从主线进入全部有实质作用的机制、条件与证据，分轮讲完；深度模式增加公式和系统分析，不默认讲代码。局部问题仍先读目标、图注和直接相关段落，只补理解所需前提。 -->
