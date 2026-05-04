# frontend-toolbox

Shared AI-tool skills for the STRV frontend team. Works with Claude Code, Codex CLI, and Cursor — distributed as plain `SKILL.md` files via the open [Agent Skills spec](https://agentskills.io/specification).

> Spike repo. Validates the distribution flow. Target end-state lives at `strvcom/frontend-toolbox`.

## Install

Pick the agent(s) you use:

```bash
# All three tools, project-local
npx skills add haidave/frontend-toolbox -a claude-code -a codex -a cursor

# Single tool, single skill, global (across all your projects)
npx skills add haidave/frontend-toolbox -a claude-code --skill frontend-design -g
```

Update later:

```bash
npx skills update
```

`npx skills` writes to `.claude/skills/`, `.cursor/skills/`, or `.codex/skills/` depending on the agent flag. By default it symlinks; pass `--copy` for file copies.

## Available skills

| Skill | What it does | Owner |
|---|---|---|
| [`frontend-design`](skills/frontend-design/SKILL.md) | Distinctive, production-grade frontend UIs that avoid generic AI aesthetics. Vendored from [anthropics/skills](https://github.com/anthropics/skills). | @haidave |

More skills land as domain owners are recruited. See [CODEOWNERS](CODEOWNERS).

## Contributing

- Each top-level dir under `skills/` has an owner in [CODEOWNERS](CODEOWNERS) who reviews PRs touching it
- New skill = new dir under `skills/<name>/` with a `SKILL.md` — see the [spec](https://agentskills.io/specification)
- Conventional Commits for the changelog

## License

Apache 2.0 — see [LICENSE](LICENSE) and [NOTICE](NOTICE).
