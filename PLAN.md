# Client Delivery Lead (CDL) AI Strategy — Plan

> Source: hand-drawn strategy board "Client Delivery Lead AI Strategy" (Obsidian / Excalidraw, last edited 2026-11-01). This document transcribes that board and turns it into a build plan for the skills in this repo.

This repo is a library of reusable **Claude skills** (`.skill` bundles) that Boosted's Client Delivery Leads use to do client-delivery work faster, more consistently, and with less prompting. This plan records *why* the library exists, *what shape* a good skill takes, and *which skills* we are building toward.

---

## 1. Strategy

### What — why Boosted uses AI to enhance delivery
- **Work more efficiently** — automate the repeatable parts of delivery work.
- **Spend time on what matters** — push toil to the toolset, keep humans on judgement.
- **Provide more clarity** — consistent, well-structured outputs clients can trust.
- **Be more consistent** — the same high bar regardless of who runs the task.

### How — the operating principles for everything we build
- **Build a toolset people can actually use** — not one-off prompts, but packaged, shareable skills.
- **Consistent outputs across team members** — any CDL running a skill gets the same quality.
- **Adaptable to different projects** — a skill works across clients, not just one engagement.
- **Easy to use / adopt** — low friction; usable without prompt-engineering expertise.
- **AI-provider agnostic** — do not hard-couple to a single model or vendor; skills must be portable.

---

## 2. Building blocks

Three primitives make the strategy real:

### Skills
- Encapsulate **repeatable tasks**.
- Provide **consistency** to outputs.
- Let users **automatically pull the right context** without writing complex prompts.
- Are **transferable to any project**.

### Connectors (MCP)
- Connect the agent to **real systems and context**.
- **Integrate AI with the existing tech stack** (Notion, Granola, repos, etc.).
- **Enable agents to do tasks outside their sandbox** — act, not just answer.

### Projects
- Give **groups of people access to the same context**.
- Let **multiple users share the same agent**, so delivery knowledge compounds across a pod.

---

## 3. Skill catalog

Each category has a characteristic workflow. These are the skills the strategy board calls out, grouped and annotated with build status in this repo.

### Artifacts — *Analyze → Create*
Client-facing deliverables generated from gathered context.

| Skill | Status |
| --- | --- |
| POV (point of view) | planned |
| Exec Deck | planned |
| Problem / Solution Deck | planned |
| UAT Test Scripts | planned |
| User Guide | planned |
| DAIA | planned |
| PIA (Privacy Impact Assessment) | planned |
| Third-party Risk Assessment | planned |
| FinOps | planned |

Related skills already in repo: **`proposal-generator`**, **`discovery-brief-v2`**.

### Analysis — *Gather Context → Collaborate with User → Present*
Structured analysis artifacts, built with the client in the loop.

| Skill | Status |
| --- | --- |
| Macro / Business Analysis | planned |
| Process Maps | planned |
| User Persona Mapping | planned |
| User Flows | planned |
| Data Dictionary | **built** → `data-dictionary.skill` |
| User Feedback Analysis | planned |
| Test Case Creation | planned |

### Repeatable Tasks — *Schedule → Run (optional)*
Recurring delivery chores that can be scheduled and run with minimal input.

| Skill | Status |
| --- | --- |
| Weekly Client Updates | planned |
| Landing Page Setup | **built** → `project-landing-page.skill` |
| Landing Page Update | partial (extend `project-landing-page`) |
| Notion Project Board Updates | partial (see `granola-to-notion.skill`) |
| Standup Prep | planned |
| Sprint Planning Prep | planned |
| Pod Retros | planned |

### Metaskills (branding) — the internal / platform layer
Skills about Boosted itself, governance, and building more skills.

| Skill | Status |
| --- | --- |
| Boosted Branding | planned |
| Boosted Values | planned |
| Data Governance Review | planned |
| Skill Creation (a skill that scaffolds new skills) | planned |
| AI Skip Stop | planned |
| Archify | planned |
| Open Whisper | planned |
| Skill ReadMe Page | planned |
| Flutter (app building) | planned |
| Knowledge-work plugins | planned |
| hallmark (design) | planned |

---

## 4. Current state of the repo

Skills packaged today:

- `data-dictionary.skill` — Analysis › Data Dictionary
- `discovery-brief-v2.skill` — Analysis / Artifacts › discovery brief
- `granola-to-notion.skill` — Repeatable Tasks › meeting notes → Notion board
- `project-landing-page.skill` — Repeatable Tasks › Landing Page Setup
- `proposal-generator.skill` — Artifacts › proposal / exec deck

---

## 5. Build roadmap

Sequenced so each phase ships usable value and feeds the next.

1. **Harden what exists** — confirm the five shipped skills meet the "How" bar (consistent, adaptable, easy to adopt, provider-agnostic); add a `SKILL.md` README standard.
2. **Repeatable Tasks first** (highest frequency, clearest ROI): Weekly Client Updates, Standup Prep, Sprint Planning Prep, Pod Retros, Landing Page Update, Notion Project Board Updates.
3. **Analysis pack**: Process Maps, User Persona Mapping, User Flows, User Feedback Analysis, Test Case Creation, Macro/Business Analysis.
4. **Artifacts pack**: POV, Exec Deck, Problem/Solution Deck, UAT Test Scripts, User Guide, then the governance set (DAIA, PIA, Third-party Risk Assessment, FinOps).
5. **Metaskills / platform**: Skill Creation + Skill ReadMe Page (force-multipliers), Data Governance Review, Boosted Branding/Values, then the rest.

### Cross-cutting requirements (apply to every skill)
- Pulls its own context (MCP connectors where possible) rather than requiring long prompts.
- Produces a consistent, templated output.
- Documented with a README so any CDL can adopt it.
- Provider-agnostic; no hard dependency on a single model/vendor.
