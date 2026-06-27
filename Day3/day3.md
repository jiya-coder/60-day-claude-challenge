# Prompt Engineering Notebook

> A reproducible, version-controlled record of prompts, model outputs, and learnings for `[topic, e.g. "Role-Based Prompting experiments"]`.
> Maintained as a living document — append new iterations rather than overwriting old ones.

## Table of contents

1. [Overview](#1-overview)
2. [Prompts](#2-prompts)
3. [Outputs](#3-outputs)
4. [Learnings](#4-learnings)
5. [Screenshots](#5-screenshots)
6. [Repro steps](#6-repro-steps)
7. [File references](#7-file-references)
8. [Versioning](#8-versioning)

---

## 1) Overview

### Purpose

`[1-3 sentences: why this notebook exists. e.g. "This notebook documents experiments testing role-based prompting strategies with Claude, to establish which persona framings produce the most reliable, expert-level outputs for technical writing tasks."]`

### Scope

- **In scope:** `[e.g. single-turn prompts, persona-based system prompts, comparison of model versions]`
- **Out of scope:** `[e.g. multi-turn agentic workflows, fine-tuning, production deployment]`

### Context

| Field | Value |
|---|---|
| Model(s) used | `[e.g. claude-sonnet-4-6, claude-opus-4-7]` |
| Interface | `[e.g. claude.ai, API, Claude Code]` |
| Related issue / ticket | `[link or ID, if applicable]` |
| Related docs | `[links to design docs, specs, prior notebooks]` |

### Goals for this round of experiments

- [ ] `[Goal 1, e.g. "Establish a baseline output with no role prompt"]`
- [ ] `[Goal 2, e.g. "Test 3 persona framings and compare specificity"]`
- [ ] `[Goal 3]`

---

## 2) Prompts

> Record prompts **exactly as sent** — including typos, formatting, and whitespace — so results are reproducible. Each prompt gets an ID referenced later in Outputs and Versioning.

### Prompt `P-001` — Baseline (no role)

**Used in version:** `v0.1.0`
**Date:** `YYYY-MM-DD`
**File:** [`prompts/P-001-baseline.txt`](./prompts/P-001-baseline.txt)

```text
[Exact prompt text goes here]
```

**Clarifications / iterations:**
- `[e.g. "Initial phrasing was ambiguous about output format — clarified to request a numbered list in P-001a"]`

---

### Prompt `P-002` — Role-based variant

**Used in version:** `v0.1.0`
**Date:** `YYYY-MM-DD`
**File:** [`prompts/P-002-role-based.txt`](./prompts/P-002-role-based.txt)

```text
[Exact prompt text goes here, e.g.:
"You are a senior [role] with [N] years of experience in [domain].
<task description>"]
```

**Clarifications / iterations:**
- `[Iteration note, e.g. "v1 used 'You are an expert in X' — too vague, model defaulted to generic tone. Revised to specify years of experience and a concrete scenario in v2."]`

---

### Prompt `P-003` — `[Next variant / follow-up prompt]`

**Used in version:** `v0.1.0`
**Date:** `YYYY-MM-DD`
**File:** [`prompts/P-003-[slug].txt`](./prompts/P-003-[slug].txt)

```text
[Exact prompt text goes here]
```

**Clarifications / iterations:**
- `[Notes]`

> Add additional `P-00N` entries as the notebook grows. Keep one prompt per file under `prompts/` so each is independently diffable in git.

---

## 3) Outputs

> Paste **representative** outputs, not every run. If outputs are long, link to the full dump in `data/` instead of pasting inline. Always pair an output with the Prompt ID and exact model/version that generated it.

### Output for `P-001` (baseline)

**Model:** `[e.g. claude-sonnet-4-6]`
**Generated:** `YYYY-MM-DD`
**Full output file:** [`data/P-001-output.md`](./data/P-001-output.md)

<details>
<summary>Representative excerpt (click to expand)</summary>

```text
[Paste representative excerpt of the model's response here]
```

</details>

**Observed characteristics:** `[e.g. "Generic, surface-level, ~80 words, no follow-up questions"]`

---

### Output for `P-002` (role-based)

**Model:** `[e.g. claude-sonnet-4-6]`
**Generated:** `YYYY-MM-DD`
**Full output file:** [`data/P-002-output.md`](./data/P-002-output.md)

<details>
<summary>Representative excerpt (click to expand)</summary>

```text
[Paste representative excerpt of the model's response here]
```

</details>

**Observed characteristics:** `[e.g. "Specific, asked clarifying diagnostic question, used domain terminology correctly"]`

---

### Side-by-side comparison

| Aspect | `P-001` (no role) | `P-002` (role-based) |
|---|---|---|
| Length | `[e.g. 80 words]` | `[e.g. 160 words]` |
| Specificity | `[low / medium / high]` | `[low / medium / high]` |
| Domain vocabulary used | `[yes/no + examples]` | `[yes/no + examples]` |
| Asked clarifying questions | `[yes/no]` | `[yes/no]` |
| Notes | `[free text]` | `[free text]` |

---

## 4) Learnings

### Key takeaways

- `[Takeaway 1, e.g. "Assigning a specific, concrete role (with years of experience / context) outperforms vague roles ('an expert') in specificity and depth."]`
- `[Takeaway 2]`
- `[Takeaway 3]`

### Pitfalls encountered

| Pitfall | Description | Mitigation |
|---|---|---|
| `[e.g. Over-broad role]` | `[e.g. "Vague role assignment ('you are an expert') produced outputs barely different from baseline."]` | `[e.g. "Add specific context: years of experience, a named scenario, or constraints."]`|
| `[e.g. Role/task mismatch]` | `[Description]` | `[Mitigation]` |
| `[Pitfall]` | `[Description]` | `[Mitigation]` |

### Improvements for next iteration

- [ ] `[e.g. "Test combining role prompts with explicit output-format constraints"]`
- [ ] `[e.g. "Run each prompt 3x to check consistency, not just a single sample"]`
- [ ] `[e.g. "Add a negative example — a role prompt that backfires — for contrast"]`

---

## 5) Screenshots

> Store image files in `images/`, named `<prompt-id>-<short-description>.png`. Always include alt text and a one-line caption. Prefer PNG for UI screenshots, and crop to the relevant region before committing.

### Screenshot: Baseline response in UI

![Claude chat interface showing a generic, unstructured response to the baseline prompt with no role assigned](./images/P-001-baseline-response.png)

*Caption: Baseline output (`P-001`) — note the generic phrasing and lack of structure.*

---

### Screenshot: Role-based response in UI

![Claude chat interface showing a structured, detailed response after a role was assigned, including a clarifying follow-up question](./images/P-002-role-response.png)

*Caption: Role-based output (`P-002`) — model adopts domain vocabulary and asks a diagnostic follow-up question.*

---

### Screenshot: `[Additional screenshot, e.g. side-by-side diff tool]`

![Placeholder alt text describing what this screenshot shows](./images/P-00N-description.png)

*Caption: `[One-line caption]`.*

> **Placeholder note:** until real screenshots are captured, this section can be left with the structure above and a `[ ] pending capture` checkbox per row so reviewers know what's outstanding.

- [ ] `P-001` baseline screenshot captured
- [ ] `P-002` role-based screenshot captured
- [ ] `[Additional screenshot]` captured

---

## 6) Repro steps

### Prerequisites

- `[e.g. Node.js >= 18 / Python >= 3.10]`
- `[e.g. An Anthropic API key with access to the model(s) listed in Overview]`
- `[e.g. git, make, or other CLI tools used by scripts in this repo]`

### Environment setup

```bash
# Clone the repo
git clone [repo-url]
cd [repo-name]

# Install dependencies
[e.g. pip install -r requirements.txt]
[e.g. npm install]

# Set environment variables
export ANTHROPIC_API_KEY="[your-key-here]"
```

### Running a prompt from this notebook

```bash
# Example: re-run prompt P-002 against the API and save output
[e.g. python scripts/run_prompt.py --prompt prompts/P-002-role-based.txt \
    --model claude-sonnet-4-6 \
    --out data/P-002-output.md]
```

### Capturing a new screenshot

```bash
# Example convention for naming and saving screenshots
# 1. Run the prompt interactively in the target UI
# 2. Save the screenshot as images/<prompt-id>-<short-description>.png
# 3. Reference it in Section 5 with alt text + caption
```

### Validating outputs match this notebook

```bash
# Optional: if outputs are deterministic-ish or you keep checksums/diffs
[e.g. diff data/P-002-output.md data/P-002-output-rerun.md]
```

> Replace all bracketed commands above with the actual scripts/tooling used in this repo. If no automation exists yet, keep this section as the documented manual procedure.

---

## 7) File references

```text
.
├── README.md                          # This notebook
├── prompts/
│   ├── P-001-baseline.txt             # Exact text of prompt P-001
│   ├── P-002-role-based.txt           # Exact text of prompt P-002
│   └── P-003-[slug].txt               # Exact text of prompt P-003
├── data/
│   ├── P-001-output.md                # Full raw output for P-001
│   ├── P-002-output.md                # Full raw output for P-002
│   └── P-00N-output.md                # Full raw output for additional prompts
├── images/
│   ├── P-001-baseline-response.png    # Screenshot referenced in Section 5
│   ├── P-002-role-response.png        # Screenshot referenced in Section 5
│   └── README.md                      # Placeholder / naming convention notes
└── scripts/                           # (optional) automation referenced in Section 6
    └── run_prompt.py
```

| Path | Description | Status |
|---|---|---|
| `prompts/P-001-baseline.txt` | `[description]` | `[ ] pending / [x] complete` |
| `prompts/P-002-role-based.txt` | `[description]` | `[ ] pending / [x] complete` |
| `data/P-001-output.md` | `[description]` | `[ ] pending / [x] complete` |
| `data/P-002-output.md` | `[description]` | `[ ] pending / [x] complete` |
| `images/P-001-baseline-response.png` | `[description]` | `[ ] pending / [x] complete` |
| `images/P-002-role-response.png` | `[description]` | `[ ] pending / [x] complete` |

---

## 8) Versioning

> One row per meaningful iteration of this notebook (new prompt round, model change, or significant learning). Use [semantic versioning](https://semver.org/)-style tags (`vMAJOR.MINOR.PATCH`) or date-based tags — pick one convention and stay consistent.

| Version | Date | Model(s) | Summary of changes | Author |
|---|---|---|---|---|
| `v0.1.0` | `YYYY-MM-DD` | `[model name]` | `[e.g. "Initial notebook scaffold + baseline prompt P-001"]` | `[name]` |
| `v0.2.0` | `YYYY-MM-DD` | `[model name]` | `[e.g. "Added role-based prompt P-002, side-by-side comparison"]` | `[name]` |
| `v0.3.0` | `YYYY-MM-DD` | `[model name]` | `[e.g. "Added screenshots, refined learnings section"]` | `[name]` |

### Changelog detail (optional, for non-trivial versions)

#### `v0.2.0` — `YYYY-MM-DD`

- Added: `[what was added]`
- Changed: `[what was changed and why]`
- Fixed: `[any corrections to earlier prompts/outputs]`

---

## Notes / open questions

- `[Anything unresolved, e.g. "Need to test whether role-based prompting holds up on adversarial/edge-case tasks"]`
- `[Open question 2]`

---

*This notebook follows a "documented experiment" convention: every prompt is traceable to an output, every output to a screenshot (where applicable), and every change to a version entry. Copy this file as a template for new experiment notebooks — keep the section structure, replace the content.*
