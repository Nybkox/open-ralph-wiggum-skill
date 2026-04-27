---
name: ralph
description: "Run Open Ralph Wiggum — an autonomous agentic loop that repeatedly sends a prompt to an AI coding agent until the task is complete. Use this skill whenever the user wants to run ralph, start an agentic loop, run a prompt in a loop, or delegate a task to ralph/ralph-wiggum. Also triggers when the user says 'ralph this', 'loop on this', or wants to run a task autonomously with repeated iterations."
---

# Open Ralph Wiggum

Run [`ralph`](https://github.com/Th0rgal/open-ralph-wiggum) — an autonomous loop that sends the same prompt to an AI agent repeatedly until it signals completion.

## Usage

Build the command from user input, then run it via Bash. The three knobs:

| Knob | Flag | Default |
|---|---|---|
| Agent | `--agent <name>` | `opencode` |
| Model | `--model <id>` | agent default |
| Mode | `--allow-all` / `--no-allow-all` | yolo (`--allow-all`) |

Agents: `opencode`, `claude-code`, `codex`, `copilot`.

## Constructing the command

```
ralph "<prompt>" --agent <agent> --model <model> [--no-allow-all] [--max-iterations N]
```

- If user says "yolo" or doesn't mention mode → omit flag (yolo is default).
- If user says "no yolo", "safe", "supervised" → add `--no-allow-all`.
- If user specifies max iterations → add `--max-iterations N`.
- If user provides a file path as prompt source → use `--prompt-file <path>` instead of inline prompt.
- Pass any extra flags the user mentions verbatim after `--`.

## Before running

1. Confirm the assembled command with the user before executing.
2. Run in background (`run_in_background: true`) — ralph loops are long-running.

## Reference

Full docs & flags: https://github.com/Th0rgal/open-ralph-wiggum/blob/master/README.md
