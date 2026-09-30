# AI Workflow Template

A project-agnostic four-agent AI development workflow for Claude Code, Gemini CLI, GitHub Copilot and OpenAI Codex.

> **Plugin-free variant** (GitHub plugin only, all other capabilities use native tools): [joshido/ai-template-core](https://github.com/joshido/ai-template-core)

## What's Included

| File | Purpose |
|------|---------|
| `AGENTS.md` | Single source of truth — workflow, Orchestrator role, conventions |
| `CLAUDE.md`, `GEMINI.md` | Generated copies of `AGENTS.md` — never edit by hand |
| `.claude/agents/` | Subagents: tester, developer, reviewer, tool-caller |
| `.ai/plan-template.md` | Required format for presenting implementation plans |
| `.ai/lessons-learned.md` | Short log of mistakes and how to avoid them |
| `.claude/settings.json` | Claude Code settings; its SessionStart hook turns on the git hooks |
| `scripts/sync-agent-files.sh` | Regenerates `CLAUDE.md` and `GEMINI.md` from `AGENTS.md` |
| `.githooks/pre-commit` | Runs the sync script on every commit |
| `.github/workflows/agent-files.yml` | CI check that the generated files are in sync |

## How to Use

1. Copy all files into the root of your new repository.
2. Enable the git hooks once per clone: `git config core.hooksPath .githooks`. Claude Code does this automatically at session start.
3. Replace the `<!-- CUSTOMIZE -->` section in `AGENTS.md` with a description of your project, then commit — `CLAUDE.md` and `GEMINI.md` are regenerated.
4. Add your permissions and preferences to `.claude/settings.json`.
5. Delete this README or replace it with your project README.

## Customization

- **Workflow** → edit `AGENTS.md` only. Run `scripts/sync-agent-files.sh` (or just commit) to update the copies.
- **Agent behavior** → edit the file in `.claude/agents/`.
- **Models** → agents use aliases (`opus`, `sonnet`, `haiku`) that resolve to the latest release. To pin a version, set `ANTHROPIC_DEFAULT_OPUS_MODEL`, `ANTHROPIC_DEFAULT_SONNET_MODEL` or `ANTHROPIC_DEFAULT_HAIKU_MODEL` in your environment.

## AI Tool Support

| Tool | Reads |
|------|-------|
| Claude Code | `CLAUDE.md` + `.claude/agents/` |
| Gemini CLI | `GEMINI.md` |
| GitHub Copilot | `AGENTS.md` |
| OpenAI Codex | `AGENTS.md` |

## Workflow Overview

```
Plan approved → Tester → Developer → Reviewer → commit → next task → PR
```
