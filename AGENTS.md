# AGENTS.md

This file provides guidance to AI Agents (Claude, GitHub Copilot, etc.) when working with code in this repository.

## Project Overview

Dioxus UI Skill is an AI-powered design intelligence toolkit providing searchable databases of UI styles, color palettes, font pairings, chart types, and UX guidelines for Dioxus Components.

## Search Command

```bash
python3 src/dioxus-skill/scripts/search.py "<query>" --domain <domain> [-n <max_results>]
```

**Stack search:**
```bash
python3 src/dioxus-skill/scripts/search.py "<query>" --stack <stack>
```
Available stacks: `dioxus` (default), `html-tailwind`, `shadcn`.

## Architecture

```
src/dioxus-skill/                # Source of Truth
├── data/                         # Canonical CSV databases
│   ├── products.csv, styles.csv, ...
│   └── stacks/                   # Stack-specific guidelines
│       └── dioxus.csv            # Dioxus Components guidelines
├── scripts/
│   ├── search.py                 # CLI entry point
│   ├── core.py                   # Search engine configuration
│   └── design_system.py          # Design system generation
```

## Sync Rules

When modifying files:

1. **Data & Scripts** - Edit in `src/dioxus-skill/`:
   - `data/stacks/dioxus.csv` for Dioxus rules.
   - `scripts/*.py` for logic.

## Prerequisites

Python 3.x (no external dependencies required)
