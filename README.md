# fable-skills

Installable [Claude Code skills](https://code.claude.com/docs/en/skills) that make any Claude model — Opus 4.8 in particular — operate with the judgment, planning, verification, and reasoning habits of **Claude Fable 5**, Anthropic's Mythos-class model.

## What's in here

| Skill | What it does |
|---|---|
| [`fable-mode`](skills/fable-mode/SKILL.md) | The full operating discipline: when to act vs. ask, scouting before editing, hypothesis-driven debugging, demonstrated-not-assumed verification, and faithful outcome reporting. |

The skill is a set of working habits, not a persona. It changes *how* the model works — what it checks before destructive commands, what counts as "done", how it labels confidence — not how it sounds.

## Activation

Say any of these in a session where the skill is installed:

- `fable mode` / `fable mode on`
- `fable it`
- `think like fable` / `act like fable`
- `mythos mode`

It also triggers implicitly on high-stakes, multi-step work (debugging stubborn failures, cross-file refactors, migrations, production changes), and deactivates with `fable mode off`.

## Installation

### Claude Code — personal (all projects)

Copy the skill folder into your user skills directory:

**Windows (PowerShell)**
```powershell
.\install.ps1
```

**macOS / Linux**
```bash
./install.sh
```

Or manually: copy `skills/fable-mode/` to `~/.claude/skills/fable-mode/`.

### Claude Code — per project

Copy `skills/fable-mode/` into `<your-project>/.claude/skills/fable-mode/`.

### Claude.ai / Claude Desktop

Zip the `skills/fable-mode/` folder (the zip must contain `SKILL.md` at the top level of the skill folder), rename it `fable-mode.skill`, and upload it via **Settings → Capabilities → Skills**.

## Verifying it's installed

Start a new Claude Code session and type `fable mode`. The model should acknowledge with a short "Fable mode on." and visibly change how it works — leading answers with outcomes, verifying changes by running them, and labeling claims as confirmed vs. inferred.

## License

MIT — see [LICENSE](LICENSE).
