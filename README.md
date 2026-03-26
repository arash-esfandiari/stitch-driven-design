# Stitch-Driven Design

A Claude Code skill for designing frontend pages by generating visual mockups first, validating with the user, then translating to production code. Never build visual UI from text descriptions alone — always have a validated reference image.

## How It Works

1. **Explore** the current page/component state
2. **Create** a Stitch project with your brand's design system
3. **Generate** mockup screens with descriptive prompts
4. **Validate** mockups with the user before writing any code
5. **Export** reference files (Vite app, screenshots, HTML)
6. **Translate** Stitch output to production code, section by section

## Prerequisites

### Required

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and configured
- [Google Stitch MCP](https://stitch.withgoogle.com) — used to generate mockup screens and design systems

### Optional

- [21st.dev MCP](https://21st.dev) — for component inspiration and patterns (React + Tailwind snippets)
- [ui-ux-pro-max](https://github.com/uxui-pro-max/ui-ux-pro-max) skill — for generating design systems with style, color, and typography recommendations before creating Stitch projects

## Installation

Copy the skill into your Claude Code skills directory:

```bash
# Clone the repo
git clone https://github.com/arashesfandiari/stitch-driven-design.git

# Copy the skill file
mkdir -p ~/.claude/skills/stitch-driven-design
cp stitch-driven-design/SKILL.md ~/.claude/skills/stitch-driven-design/SKILL.md
```

Or copy manually:

```bash
mkdir -p ~/.claude/skills/stitch-driven-design
curl -o ~/.claude/skills/stitch-driven-design/SKILL.md \
  https://raw.githubusercontent.com/arashesfandiari/stitch-driven-design/main/SKILL.md
```

## Usage

Once installed, the skill activates automatically in Claude Code when you use trigger phrases like:

- "Design a new landing page"
- "Redesign the dashboard"
- "Make it look like this mockup"
- "Visual overhaul of the settings page"
- "UI refresh for the profile section"

Claude Code will follow the Stitch-driven workflow: generate mockups, get your approval, then translate to code.

## When to Use

- Designing a new page or major section
- Redesigning an existing page to match a new visual direction
- Building components that need to look polished and branded

## When NOT to Use

- Bug fixes or logic changes with no visual impact
- Adding a single small element to an existing design
- Backend-only work

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute.

## License

[MIT](LICENSE)
