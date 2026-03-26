# Contributing to Stitch-Driven Design

Thanks for your interest in contributing! This skill helps developers design frontend pages using a mockup-first workflow with Google Stitch and Claude Code.

## Getting Started

1. Fork and clone the repo
2. Install the skill locally:

```bash
mkdir -p ~/.claude/skills/stitch-driven-design
cp SKILL.md ~/.claude/skills/stitch-driven-design/SKILL.md
```

3. Test your changes by using the skill in Claude Code with a real design task

## Making Changes

The core of this project is `SKILL.md` — a structured guide that Claude Code follows during design tasks.

### What to change

- **Workflow improvements** — better step ordering, missing steps, clearer instructions
- **Tailwind-to-CSS translations** — additional mappings in the translation table
- **Common mistakes** — new pitfalls you've encountered and their fixes
- **Tool integrations** — better ways to combine with other skills or MCP servers
- **Prompt tips** — techniques that produce better Stitch mockups

### What NOT to change

- Don't add features unrelated to the mockup-first design workflow
- Don't remove the core validation steps (user must approve mockups before implementation)
- Don't add dependencies on paid or proprietary tools beyond what's already listed

## Submitting a PR

1. Create a branch from `main`
2. Make your changes to `SKILL.md`
3. Test the skill end-to-end with a design task in Claude Code
4. Open a PR with:
   - **What** you changed
   - **Why** it improves the workflow
   - **How** you tested it (describe the design task you used)

## Reporting Issues

Use the GitHub issue templates for:

- **Bug reports** — the skill produced incorrect output or a broken workflow
- **Feature requests** — ideas for improving the design workflow

## Code of Conduct

Be respectful and constructive. We're all here to make frontend design workflows better.
