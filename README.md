# Global instructions for CLI AI

This repository distributes restrictive global instruction files for Codex CLI and Claude Code. Install them once, then start either CLI from the folder where you actually want to work. Each file contains the full policy so it works independently.

## Install globally

Run these commands from **any directory** on Linux. They download the published files directly from this repository.

```sh
mkdir -p "$HOME/.codex" "$HOME/.claude"
curl -fL "https://raw.githubusercontent.com/BinaryLogicRo/Instructions-for-CLI-AI/main/AGENTS.md" -o "$HOME/.codex/AGENTS.md"
curl -fL "https://raw.githubusercontent.com/BinaryLogicRo/Instructions-for-CLI-AI/main/CLAUDE.md" -o "$HOME/.claude/CLAUDE.md"
```

These commands replace any existing global instruction files, so review or back up those files first.