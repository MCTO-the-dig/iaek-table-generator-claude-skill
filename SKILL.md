---
name: iaek-table-generator
description: Generates the IAEK impact table HTML for Digitising Events Platform Tools & Tech articles. Use this skill whenever Adam asks to create an IAEK table, impact table, or platform impact analysis for a tool or platform. Triggers on phrases like "create the IAEK table", "generate the impact table", "build the IAEK table for [tool]", or any request for a platform impact analysis. Always use this skill for IAEK table generation — do not attempt to write IAEK tables without it.
---

# Digitising Events — IAEK Table Generator

Produces the Platform Impact Analysis HTML table for insertion into Digitising Events Platform Tools & Tech articles. Output is a single HTML table, nothing else.

## Inputs Required

- **Platform or tool name** — used in the caption
- **Use case description** — what the tool does in a DE or events workflow context
- **IAEK framework fit** — which one or two IAEK categories apply (see Framework Options below)
- **CVI impact** — the primary value created (what becomes possible)
- **CVO outcome** — the operational transformation (what changes in practice)
- **Strategic value** — the competitive or scalability advantage

If any input is missing, ask for it before generating. Do not invent content.

---

## Framework Options

Select one or two that best fit the tool. Always use the full label and letter exactly as shown.

| Label | Letter | When to Use |
|-------|--------|-------------|
| Information Exchange | I | Information delivery and content distribution |
| Audience Engagement | A | Community building and interaction facilitation |
| Experience Enhancement | E | Personalised and improved user experiences |
| Knowledge Gain/Transfer | K | Experiences that significantly accelerate learning or enable deeper understanding |

---

## Output

Return **only the HTML table** — no preamble, no explanation, no markdown wrapper.

```html
<table class="impact-table" role="table" aria-label="Platform Impact Analysis">
  <caption style="caption-side: top; font-size: 1.1rem; font-weight: 600; margin-bottom: 1rem; color: #374151;">
    Platform Impact Analysis: [PLATFORM NAME]
  </caption>
  <thead>
    <tr>
      <th scope="col">Assessment Category</th>
      <th scope="col">Analysis & Impact</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="category-cell">Use Case</td>
      <td class="content-cell">[USE CASE DESCRIPTION WITH <span class="highlight">KEY FEATURE</span> HIGHLIGHTED]</td>
    </tr>
    <tr>
      <td class="category-cell">IAEK Framework Fit</td>
      <td class="content-cell"><strong>[Primary Framework] ([Letter])</strong> - [Description]<br><strong>[Secondary Framework] ([Letter])</strong> - [Description]</td>
    </tr>
    <tr>
      <td class="category-cell">Primary CVI Impact</td>
      <td class="content-cell">Enables <span class="highlight">[KEY VALUE CREATION]</span> with [supporting details and workflow benefits].</td>
    </tr>
    <tr>
      <td class="category-cell">CVO Outcome</td>
      <td class="content-cell">[Operational transformation description] whilst <span class="highlight">[KEY EFFICIENCY GAIN]</span> and [additional operational benefits].</td>
    </tr>
    <tr>
      <td class="category-cell">Strategic Value</td>
      <td class="content-cell">Transforms [problem area] from [current state] into [improved state], enabling <span class="highlight">[STRATEGIC ADVANTAGE]</span> without [typical scaling constraints].</td>
    </tr>
  </tbody>
</table>
```

---

## Constraints

- Return **only the HTML table** — no surrounding text, no explanation
- Use exact class names: `impact-table`, `category-cell`, `content-cell`
- Include all accessibility attributes: `role`, `aria-label`, `scope`
- Format IAEK Framework Fit rows with `<strong>` tags and `<br>` separator between entries
- Use `<span class="highlight">` for one or two key terms per cell — do not over-highlight
- If only one IAEK category applies, use a single `<strong>` line with no `<br>`
- British English throughout
