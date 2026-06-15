# IAEK Table Generator — Claude Skill

A Claude skill that generates the Platform Impact Analysis HTML table for [Digitising Events](https://digitisingevents.com) Platform Tools & Tech articles.

Part of the [HITL (Human-in-the-Loop) methodology](https://digitisingevents.com) — a live experiment in AI-powered independent media operations.

---

## What It Does

Takes tool or platform context as input and returns a single, ready-to-paste HTML table assessing that tool against the IAEK framework. Output drops directly into a Webflow rich text field with no further formatting required.

---

## The IAEK Framework

IAEK is the core evaluation lens used across all Digitising Events Platform Tools & Tech content. It assesses tools against four value categories:

| Letter | Category | What It Covers |
|--------|----------|----------------|
| I | Information Exchange | Information delivery and content distribution |
| A | Audience Engagement | Community building and interaction facilitation |
| E | Experience Enhancement | Personalised and improved user experiences |
| K | Knowledge Gain/Transfer | Experiences that significantly accelerate learning or enable deeper understanding |

Each table maps a tool to one or two IAEK categories and evaluates it across five dimensions: Use Case, IAEK Framework Fit, Primary CVI Impact, CVO Outcome, and Strategic Value.

---

## Usage

Place `SKILL.md` in your Claude skills directory. The skill triggers on phrases like:

- "create the IAEK table for [tool]"
- "generate the impact table"
- "build the IAEK table"
- Any request for a platform impact analysis in a DE context

Claude will ask for any missing inputs before generating. It will not invent content.

---

## Output

A single HTML table using the following Webflow classes:

- `impact-table` — table root
- `category-cell` — left column (assessment category label)
- `content-cell` — right column (analysis and impact copy)
- `highlight` — inline span for key terms

No preamble, no explanation. Paste-ready.

---

## Part of the DE Skills Library

This skill sits alongside:

- [`de-editorial-checker`](https://github.com/themediacto/de-editorial-checker) — three-pass editorial review against DE house style
- [`article-video-script`](https://github.com/themediacto/article-video-script) — spoken-word teaser script generator for ElevenLabs TTS

---

## About Digitising Events

Digitising Events is a live experiment in building an AI-powered independent media business using the Human-in-the-Loop methodology. The skills library documents repeatable procedures that emerge from that process and makes them publicly available.

More at [digitisingevents.com](https://digitisingevents.com)
