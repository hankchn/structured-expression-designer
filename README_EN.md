# structured-expression-designer

Turn complex, fragmented, or information-dense content into clear, editable, and reusable visual structures.

<p align="center">
  <a href="./README.md">简体中文</a> | <strong>English</strong>
</p>

![Structured Expression Goodcase Gallery](./assets/structured-expression-goodcase-wall.svg)

## What It Is

`structured-expression-designer` is a Codex Skill for structured visual communication.

Instead of applying a diagram template immediately, it first identifies the underlying relationship in the content, such as sequence, hierarchy, comparison, time, causality, composition, network, or data trend. It then recommends two or three meaningfully different directions. After a direction is selected, the Skill produces an editable visual or source format.

Typical use cases include:

- Business processes and PRDs
- Meeting notes and research notes
- Knowledge systems and learning paths
- Data analysis and metric diagnosis
- Competitive analysis and market landscapes
- Strategy planning and roadmaps
- Capability models and presentation materials

## Core Capabilities

- **Identify information relationships**: Extract entities, relationships, hierarchy, time, data, and conclusions from raw content.
- **Recommend visual directions**: Propose two or three options based on the core question, audience, and context.
- **Explain tradeoffs**: State what each option emphasizes and what it may sacrifice.
- **Build a unified content model**: Create a structured intermediate layer before rendering.
- **Protect factual boundaries**: Separate facts, inferences, hypotheses, and placeholders.
- **Support editable outputs**: Produce Mermaid, draw.io XML, PPTX, SVG, or Markdown when the available tools support them.
- **Run visual QA**: Check reading order, density, text overflow, data definitions, and file validity.

## Diagram Library

| Category | Included templates |
|---|---|
| Sequence and state | Primary flow, swimlane flow, page / state transition |
| Data and diagnosis | Metric driver tree, funnel diagnosis, cohort / segment heatmap |
| Comparison and relationships | Capability matrix, positioning map, market / ecosystem map |
| Strategy and panorama | Strategic roadmap, capability / iceberg model, panorama information map |
| General structures | Hierarchy / taxonomy tree, timeline / evolution, causal chain / issue tree, trend / distribution chart |

## Workflow

```text
Raw content
   ↓
Define the core question, audience, and context
   ↓
Build a unified content model
   ↓
Identify the primary information relationship
   ↓
Recommend 2-3 visual directions
   ↓
User selects a direction or accepts the best option
   ↓
Generate an editable output
   ↓
Render and run QA
```

## Installation

```bash
git clone https://github.com/hankchn/structured-expression-designer.git
mkdir -p ~/.codex/skills/structured-expression-designer
cp -R structured-expression-designer/{SKILL.md,agents,assets,references} \
  ~/.codex/skills/structured-expression-designer/
```

Start a new Codex session after installation so the Skill can be loaded.

## Usage

Explicit invocation:

```text
Use $structured-expression-designer to analyze the content below.
Recommend 2-3 suitable visual structures and explain their tradeoffs:

<paste content>
```

Direct generation:

```text
Use $structured-expression-designer to turn this business process into
an editable diagram. Prioritize clear ownership boundaries between
engineering, operations, and customer support.
```

Data analysis:

```text
Use $structured-expression-designer to analyze this conversion dataset.
First decide whether a funnel, metric tree, or trend chart is most suitable,
then create a presentation-ready plan.
```

## Output Principles

| Format | Best for |
|---|---|
| Mermaid | Flows, states, sequences, trees, and rapid iteration |
| draw.io XML | Swimlanes, architecture, complex processes, and relationship maps |
| PPTX | Formal presentations, strategy, competitive analysis, and roadmaps |
| SVG | Document illustrations, one-page information graphics, and polished previews |
| Markdown | Content models, matrices, data tables, and review drafts |

The Skill only promises a file when the current tools can actually create and validate that file. Otherwise, it clearly delivers copyable source code, a page structure, or a generation specification.

## Repository Structure

```text
structured-expression-designer/
├── README.md
├── README_EN.md
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── structured-expression-goodcase-wall.svg
└── references/
    ├── content-model.md
    ├── goodcases.md
    ├── output-specs.md
    ├── selection-guide.md
    ├── templates.md
    └── visual-qa.md
```

## Design Principles

- Identify the information relationship before the business scenario.
- Make each visual answer one core question.
- Recommended directions must differ in emphasis, not merely color or orientation.
- Never fabricate scores, coordinates, funnel values, or causal claims.
- Split complex content instead of forcing everything into tiny text.
- Use a restrained consulting-style visual language focused on clarity and editability.

## Goodcases

High-quality examples are welcome. Before a case is added to the Skill, it should explain:

- What problem it solves
- Which information structure it uses
- What should be reused
- What should not be copied
- Which template and output format it belongs to

The Skill captures reusable structure and design principles. It does not reproduce complete copyrighted designs pixel by pixel.

## Contributors

- [hankchn](https://github.com/hankchn) — Project direction, requirements, and maintenance
- [Codex](https://github.com/codex) — Structure design, documentation, and implementation support
