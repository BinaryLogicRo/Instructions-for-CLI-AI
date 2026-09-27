# Global instructions for CLI AI

This repository distributes restrictive global instruction files for Codex CLI and Claude Code. Install them once, then start either CLI from the folder where you actually want to work. Each file contains the full policy so it works independently.

## Install globally

From this repository's root, copy the instructions to each CLI's user-level directory:

```sh
mkdir -p "$HOME/.codex" "$HOME/.claude"
cp -i AGENTS.md "$HOME/.codex/AGENTS.md"
cp -i CLAUDE.md "$HOME/.claude/CLAUDE.md"
```

`cp -i` asks before replacing an existing file. If you use `CODEX_HOME` or `CLAUDE_CONFIG_DIR`, copy into those directories instead. Leave this repository after installation and start a new `codex` or `claude` session from **any folder**. Ask the agent to summarize the instructions it loaded to verify the setup. [Codex instructions](https://learn.chatgpt.com/docs/agent-configuration/agents-md) · [Claude Code instructions](https://code.claude.com/docs/en/memory)

A folder trust prompt may still appear; it controls trust in that workspace. Instruction files guide agent behavior. For a stronger boundary, start Codex with `codex --sandbox read-only --ask-for-approval on-request`, or start Claude Code with `claude --permission-mode plan` for read-only work. Claude Code's `default` permission mode prompts for file edits; choose one-time approval when you want to authorize a specific edit. [Codex permissions](https://learn.chatgpt.com/docs/agent-approvals-security) · [Claude Code permissions](https://code.claude.com/docs/en/permissions)
