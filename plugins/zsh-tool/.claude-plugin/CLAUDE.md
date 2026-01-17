# zsh-tool

Zsh shell execution MCP server with psychological protections for AI agents.

## Why zsh-tool?

The built-in Bash tool works for simple commands, but causes issues in zsh environments and lacks observability. zsh-tool provides:

- **NEVERHANG**: Circuit breaker prevents runaway/hanging commands from blocking everything
- **A.L.A.N.**: Learns command patterns, tracks success rates, warns about novel commands
- **Yield-based execution**: Long commands return control early, poll for results
- **Interactive stdin**: Send input to running processes via `zsh_send`
- **PTY mode**: Real terminal emulation for tools that need it

## Installation

```bash
pip install zsh-tool
```

Add to `~/.claude/mcp_servers.json`:
```json
{
  "zsh-tool": {
    "command": "zsh-tool"
  }
}
```

## Usage

Use `mcp__zsh-tool__zsh` for command execution:
- `zsh_poll` to check on long-running commands
- `zsh_send` to send stdin to running processes
- `zsh_kill` to terminate a task
- `zsh_health` to check NEVERHANG and A.L.A.N. status
- `zsh_alan_stats` for learning metrics

## When to use

Prefer zsh-tool over Bash when you need:
- Interactive stdin (answering prompts mid-execution)
- PTY mode (terminal detection, colors, curses)
- Observability on command patterns
- Protection against hanging commands
