# Stitch-Driven Design

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that enforces a mockup-first workflow for frontend design. Instead of coding UI from text descriptions, you generate visual mockups with [Google Stitch](https://stitch.withgoogle.com), validate them with the user, then translate to production code with exact values.

## Why

AI coding tools are bad at visual design when working from text alone. They guess at layouts, colors, and spacing — producing generic-looking interfaces. This skill fixes that by making a validated visual reference the source of truth before any code is written.

## How It Works

1. **Claude reads your app** — analyzes your current codebase, design system, and user requirements
2. **Connects to Stitch & 21st.dev MCPs** — feeds your brand context (fonts, colors, layout preferences) into Google Stitch to generate mockup screens, and pulls component inspiration from 21st.dev
3. **View the mockup** — log into the [Stitch dashboard](https://stitch.withgoogle.com) in your browser to see what it generated
4. **Export the project** — download the Stitch project (the mockup) as a Vite app using AI Studio
5. **Point Claude to it** — give Claude the path to the exported files and watch the magic happen — it reads the screenshots, extracts exact values from the code, and translates everything into your project's stack

## What Stitch Gives You

When the user exports from Stitch, you get:

- **`screen.png`** — Visual target (Claude reads this as an image)
- **`src/App.tsx`** — Full React components with exact Tailwind classes
- **`src/index.css`** — Design tokens, glass panel definitions, font imports
- **`code.html`** — Flat HTML per screen (secondary reference)

Claude extracts exact hex colors, rem values, shadow definitions, blur amounts, and layout grids from the code — then maps them to your project's CSS approach.

## Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
- [Google Stitch MCP](https://stitch.withgoogle.com) — generates mockup screens and design systems

**Optional:**
- [21st.dev MCP](https://21st.dev) — component inspiration and interaction patterns
- [ui-ux-pro-max](https://github.com/uxui-pro-max/ui-ux-pro-max) — generates design system recommendations to feed into Stitch

## Installation

```bash
# Option 1: Clone and copy
git clone https://github.com/arash-esfandiari/stitch-driven-design.git
mkdir -p ~/.claude/skills/stitch-driven-design
cp stitch-driven-design/SKILL.md ~/.claude/skills/stitch-driven-design/SKILL.md

# Option 2: Direct download
mkdir -p ~/.claude/skills/stitch-driven-design
curl -o ~/.claude/skills/stitch-driven-design/SKILL.md \
  https://raw.githubusercontent.com/arash-esfandiari/stitch-driven-design/main/SKILL.md
```

## Usage

The skill activates automatically when you say things like:

- "Design a new landing page"
- "Redesign the dashboard"
- "Visual overhaul of the settings page"

Claude will follow the full workflow — generate mockups, wait for your approval, then translate to code.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
