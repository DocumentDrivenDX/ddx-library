# DDx Library

Templates, patterns, prompts, and configurations for AI-assisted development.

## HELIX Workflow

The HELIX workflow — the primary methodology in this library — has moved to its
own repository: **[helix](https://github.com/easel/helix)**

Install HELIX directly:

```bash
cd ~/Projects/helix
scripts/install-local-skills.sh
```

## Remaining Contents

This library retains generic DDx assets that are not HELIX-specific:

- **commands/** — Claude Code slash commands (`/ddx:prd`, `/ddx:code-review`, etc.)
- **agents/** — Specialized Claude Code agents (architect, code-reviewer, test-engineer, qa-analyst)
- **personas/** — AI persona definitions
- **prompts/** — Standalone AI prompts
- **templates/** — Project templates
- **patterns/** — Reusable code patterns
- **mcp-servers/** — MCP server registry
- **environments/** — Environment configurations
- **tools/** — Tool definitions

## License

MIT
