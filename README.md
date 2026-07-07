# DDx Library

This repository contains the DDx (Document-Driven Development eXperience) library of templates, patterns, prompts, and configurations for AI-assisted development.

## Demo: HELIX Quickstart

Full TDD cycle — from empty repo to passing tests — driven by Claude with the HELIX workflow:

![HELIX Quickstart Demo](docs/demos/helix-quickstart/recordings/helix-quickstart.gif)

> Planning stack → Red phase → Bead-driven implementation → Green phase → Critical review → Queue triage. [Run it yourself](docs/demos/helix-quickstart/) · [asciinema](https://asciinema.org/a/12zustljbjnrygad).

## Installation

### Claude Code Plugin

Install the DDx Library plugin with the NPX marketplace installer:

```bash
npx claude-plugins install @DocumentDrivenDX/ddx-library/ddx
```

For Claude Code's native plugin flow:

```bash
# Add the repository as a marketplace
/plugin marketplace add DocumentDrivenDX/ddx-library

# Install the plugin
/plugin install ddx@ddx-library
```

This gives you:
- **Skills**: DDx operational skills for beads, workers, reviews, agents, status, and queue stewardship; plus `/ddx:helix` (TDD workflow), `/ddx:review` (critical review), `/ddx:grind` (continuous queue execution), `/ddx:execute` (single bead), `/ddx:triage` (queue health), `/ddx:handoff` (agent handoff review), `/ddx:helix-alignment-review` (drift analysis)
- **Commands**: `/ddx:prd`, `/ddx:code-review`, `/ddx:commit-hooks`, `/ddx:github-actions`, `/ddx:docs`, `/ddx:gitignore`, `/ddx:create-workflow`

## Contents

- **commands/** - Claude Code slash commands
- **skills/** - Auto-invoked Claude Code skills (HELIX workflow)
- **agents/** - Specialized agent prompts retained as library resources
- **prompts/** - AI prompts and instructions for various development tasks
- **personas/** - AI personality definitions for consistent interactions
- **workflows/** - Complete development methodologies (HELIX, etc.)
- **docs/demos/** - Reproducible demo recordings ([HELIX quickstart](docs/demos/helix-quickstart/))

## Contributing

### Local Development

Clone and install locally to test changes:

```bash
# Clone the repository
git clone https://github.com/DocumentDrivenDX/ddx-library.git
cd ddx-library

# Test as a local plugin
claude --plugin-dir .

# Or from another directory
claude --plugin-dir /path/to/ddx-library
```

### Plugin Structure

```
ddx-library/
├── .claude-plugin/
│   ├── plugin.json      # Claude Code plugin manifest
│   └── marketplace.json # Claude Code marketplace descriptor
├── package.yaml         # DDx package manifest
├── commands/            # Slash commands (/ddx:*)
├── skills/              # Auto-invoked skills
├── agents/              # Specialized agent prompt resources
└── .mcp.json            # MCP server configs
```

### Making Changes

- **commands/*.md** - Add or modify slash commands
- **skills/*/SKILL.md** - Add or modify auto-invoked skills
- **agents/*.md** - Add or modify specialized agent prompt resources
- **workflows/** - Add or modify workflow definitions
- **prompts/** - Add or modify standalone prompts

### Submitting Changes

1. Fork this repository
2. Create a branch for your changes
3. Test locally with `claude --plugin-dir .`
4. Submit a pull request

## License

This library is open source software licensed under the MIT License.

## Related Projects

- [HELIX Workflow](./workflows/helix/) - Six-phase AI-assisted development methodology
