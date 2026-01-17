# ArkTechNWA Claude Code Plugins

A marketplace of MCP tools and plugins for Claude Code.

## Available Plugins

### zsh-tool
Zsh shell execution with psychological protections for AI agents.

- **NEVERHANG**: Circuit breaker prevents runaway commands
- **A.L.A.N.**: Learns command patterns, tracks success rates
- **Yield-based execution**: Long commands return control, poll for results
- **Interactive stdin**: Send input to running processes
- **PTY mode**: Real terminal emulation

## Installation

Add this marketplace to Claude Code:
```bash
# Clone into your marketplaces directory
cd ~/.claude/plugins/marketplaces
git clone https://github.com/ArkTechNWA/claude-plugins.git arktechnwa
```

Then install plugins via `/plugin install arktechnwa/zsh-tool`

## License

MIT
