# Dioxus UI Skill

An AI skill that provides design intelligence for building Dioxus applications using [Dioxus Components](https://github.com/DioxusLabs/components) (shadcn-inspired) and Tailwind CSS.

## Features

- **Dioxus-First Guidelines**: Specialized knowledge base for Dioxus Components setup, usage, and best practices.
- **Design System Generation**: AI-powered engine to generate tailored design systems (colors, typography, styles) for your Dioxus apps.
- **Multi-Stack Context**: Includes guidelines for `shadcn` (as an upstream reference) and `html-tailwind` for styling.
- **UI/UX Intelligence**: Access to 60+ UI styles, 90+ color palettes, and UX anti-patterns.

## Supported Stacks

| Stack | Description | Usage |
|-------|-------------|-------|
| **dioxus** | Core guidelines for Dioxus Components | `--stack dioxus` |
| **shadcn** | Reference patterns from the original React library | `--stack shadcn` |
| **html-tailwind** | Utility class best practices | `--stack html-tailwind` |

## Usage

### Search Guidelines

Find specific component usage or best practices:

```bash
# Search Dioxus-specific rules
python3 src/dioxus-skill/scripts/search.py "button" --stack dioxus

# Check upstream shadcn patterns
python3 src/dioxus-skill/scripts/search.py "dialog" --stack shadcn
```

### Generate Design System

Generate a complete visual design system based on your project description:

```bash
python3 src/dioxus-skill/scripts/search.py "modern SaaS dashboard for fintech" --design-system
```

### General UI Search

Search for specific design concepts:

```bash
python3 src/dioxus-skill/scripts/search.py "glassmorphism" --domain style
python3 src/dioxus-skill/scripts/search.py "accessible colors" --domain color
```

## Directory Structure

```
src/dioxus-skill/
├── data/
│   ├── stacks/           # Stack-specific knowledge bases
│   │   ├── dioxus.csv
│   │   ├── shadcn.csv
│   │   └── html-tailwind.csv
│   └── *.csv             # General design databases (colors, styles, etc.)
└── scripts/              # Search and generation logic
```

## Credits

This skill is adapted from [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) by Next Level Builder. It reuses the search engine core and general UI/UX knowledge bases while providing a specialized dataset for the Dioxus ecosystem.
