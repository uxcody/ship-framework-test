# ship-framework-test

An AI product team framework for one-person teams. Gives Claude structured roles (PM, designer, engineer, reviewer) and agents that work in parallel to plan, build, and ship products.

## What this repo is
A fork of the Ship Framework used for testing and personal customization. The `template/` directory contains the framework itself — Claude commands, skills, and reference docs that get installed into a project.

## Structure
- `template/.claude/commands/` — 20 slash commands (`/ship-build`, `/ship-review`, `/ship-design`, etc.)
- `template/.claude/skills/ship/` — ship framework skills
- `template/.claude/skills/your-skills/` — placeholder for custom skills
- `template/references/` — 85 reference docs organized by platform (ios/, shared/, web/)
- `setup.sh` — installs the template into a target project
- `ship-framework.plugin` — Claude Code plugin (installable via `claude plugin add`)

## How to install the framework into a project
```bash
# Plugin method (recommended)
claude plugin add ./ship-framework.plugin

# Legacy template-copy method
bash setup.sh
```

## Key commands (once installed in a project)
- `/ship-build` — build a feature end-to-end
- `/ship-review` — multi-agent code review
- `/ship-design` — design a UI or flow
- `/ship-plan` — plan a product or feature
- `/ship-qa` — quality assurance pass
- `/ship-fix` — targeted bug fix

## Notes
- This repo does not have a build step — it's markdown templates and shell scripts
- VERSION file tracks the current release (date-based versioning, e.g. `v2026.04.14`)
- The `template/references/` structure was reorganized in v5 — references now live under `.claude/skills/ship/` in the plugin architecture
