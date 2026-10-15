# Writing & Docs Kit

Write READMEs, technical docs, changelogs, PR descriptions and ADRs with an agent, strip AI-sounding prose, and draw diagrams that earn their place in the docs.

A setup for AI coding agents, made by [Kitloom](https://kitloom.site). One source, generated for every major agent: Claude Code, OpenAI Codex, Cursor, Google Antigravity, Gemini CLI, GitHub Copilot, Windsurf (Devin), opencode and Aider.

## Install

1. Download this repository as a ZIP, or use the **Check and download** button on its Kitloom page, which checks it first.
2. Read the files. Nothing here runs on its own: the kit has no hooks and no install scripts.
3. Copy the folders and files you want into the root of your project. `AGENTS.md` is the shared instructions file; edit it to fit your project.

## What is inside

### Skills

- `humanizer` — Rewrite a draft that reads machine-generated so it keeps its meaning but sounds like a person.
- `writing-for-agents` — Writing or editing AGENTS.md, CLAUDE.md or skills that another agent will read.
- `pr` — Drafting a pull request body that a reviewer can understand in one read.
- `changelog-automation` — Producing a changelog or release notes in Keep a Changelog format from commits and PRs.
- `documentation-and-adrs` — Recording an architecture decision or documenting a changed public API.
- `diagram-design` — A doc needs an architecture, flow, sequence or state diagram.
- `openapi-spec-generation` — Documenting an HTTP API as an OpenAPI 3.1 spec.
- `hads` — Structuring reference docs so both humans and AI models can scan them cheaply.
- `neat-freak` — After a change, reconcile README, docs and agent rule files with what the code actually does.

### Commands

Invoke by name (for example `/write-readme`).

- `write-readme` — Draft or rewrite the project README from what the repository actually contains.
- `de-slop` — Edit a file or selection to remove AI-sounding prose without changing its meaning.
- `draft-changelog` — Build a changelog entry or release notes from the commits since the last tag.

### Sub-agents

- `docs-fact-checker` — Delegate to verify that every command, path, flag and link in a doc is real and current.
- `prose-editor` — Delegate to copy-edit a draft for clarity, structure and AI-sounding phrasing, returning suggested edits.

### Scoped rules

- `markdown-prose` — Style rules for any Markdown file: plain, specific, no AI filler.
- `docs-accuracy` — Every claim in a doc must be checked against the code, commands and files in the repository.
- `no-invented-facts` — Never invent versions, benchmarks, links, features or quotes while writing.

## Where each agent finds it

| Agent | Instructions | Skills and commands | Rules | Sub-agents |
|---|---|---|---|---|
| Claude Code | `CLAUDE.md` (imports `AGENTS.md`) | `.claude/skills/` | `.claude/rules/` | `.claude/agents/` |
| OpenAI Codex | `AGENTS.md` | `.agents/skills/` | listed in `AGENTS.md` | `.codex/agents/` |
| Cursor | `AGENTS.md` | `.agents/skills/`, `.claude/skills/` | `.cursor/rules/` | `.claude/agents/` |
| Google Antigravity | `AGENTS.md` | `.agents/skills/` | `.agents/rules/` | `.agents/agents/` |
| Gemini CLI | `AGENTS.md` via `.gemini/settings.json` | `.agents/skills/`, `.gemini/commands/` | listed in `AGENTS.md` | `.gemini/agents/` |
| GitHub Copilot | `AGENTS.md` | `.agents/skills/`, `.github/prompts/` | `.github/instructions/` | `.claude/agents/` |
| Windsurf (Devin) | `AGENTS.md` | `.agents/skills/`, `.windsurf/workflows/` | `.windsurf/rules/` | — |
| opencode | `AGENTS.md` | `.agents/skills/`, `.opencode/commands/` | listed in `AGENTS.md` | `.opencode/agents/` |
| Aider | `AGENTS.md` via `.aider.conf.yml` | — | — | — |

Skills are stored twice (`.agents/skills/` and `.claude/skills/`) because Claude Code reads only its own folder. Agents that read both may list a skill twice; delete the copy you do not need.

## Credits

The skills come from these open-source repositories, each under its own licence. Their licence and a notice are kept beside every copied skill.

| Skill | Source | Licence |
|---|---|---|
| `humanizer` | [blader/humanizer](https://github.com/blader/humanizer) at `225a6f3` | MIT |
| `writing-for-agents` | [mattpocock/skills](https://github.com/mattpocock/skills) at `49dd158` | MIT |
| `pr` | [mattpocock/skills](https://github.com/mattpocock/skills) at `49dd158` | MIT |
| `changelog-automation` | [wshobson/agents](https://github.com/wshobson/agents) at `46891e7` | MIT |
| `documentation-and-adrs` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) at `aeac41d` | MIT |
| `diagram-design` | [cathrynlavery/diagram-design](https://github.com/cathrynlavery/diagram-design) at `11b08ea` | MIT |
| `openapi-spec-generation` | [wshobson/agents](https://github.com/wshobson/agents) at `46891e7` | MIT |
| `hads` | [wshobson/agents](https://github.com/wshobson/agents) at `46891e7` | MIT |
| `neat-freak` | [KKKKhazix/khazix-skills](https://github.com/KKKKhazix/khazix-skills) at `322346d` | MIT |

Everything else in this repository (instructions, rules, commands, sub-agents) is by Kitloom under the MIT licence.

## Use at your own risk

Read every file before you use it. Agent instructions can make an agent run commands on your machine. This kit was checked with Kitloom's pre-download check, which looks for warning signs but cannot prove anything is safe.
