# zsh-tool

Zsh shell execution with NEVERHANG circuit breaker and A.L.A.N. learning.

## Required: Install the MCP server

Before using this plugin, install zsh-tool:

```bash
pip install zsh-tool
```

This adds the `zsh-tool` command to your PATH, which the MCP server needs.

## Features

- **NEVERHANG**: Circuit breaker prevents runaway commands
- **A.L.A.N.**: Learns command patterns, tracks success rates
- **Yield-based execution**: Long commands return control, poll for results
- **Interactive stdin**: Send input to running processes
- **PTY mode**: Real terminal emulation
