# Open Ralph Wiggum Skill

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill for running [Open Ralph Wiggum](https://github.com/Th0rgal/open-ralph-wiggum) — an autonomous agentic loop that repeatedly sends a prompt to an AI coding agent until the task is complete.

## Install

```bash
npx skills add Nybkox/open-ralph-wiggum-skill
```

## Usage

Once installed, just ask Claude to run ralph:

- "ralph this task with claude-code and sonnet"
- "loop on fixing the auth bug, no yolo"
- "run ralph with codex, max 10 iterations"

The skill lets you pick **agent** (`opencode`, `claude-code`, `codex`, `copilot`), **model**, and **mode** (yolo/no-yolo).
