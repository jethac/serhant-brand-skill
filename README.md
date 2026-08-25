# serhant-brand-skill

Agent skill that runs Ryan Serhant's *Brand It Like Serhant* (Hachette Go, 2024) as a workflow. One `SKILL.md` tree for **Claude Code**, **Codex**, and **Grok**.

## Install

Clone once, then put the directory on each tool's skill path. Codex **skips symlinks** — copy for Codex, junction or copy for the others.

```powershell
git clone <this-repo-url> serhant-brand-skill
```

| Tool | User skill path | Notes |
|---|---|---|
| Claude Code | `~/.claude/skills/serhant-brand-skill` | Also `.claude/skills/` in a repo |
| Codex | `~/.codex/skills/serhant-brand-skill` | Real directory, not a symlink. Also `.agents/skills/` in a repo, or `~/.agents/skills/` |
| Grok | `~/.grok/skills/serhant-brand-skill` | Also `.grok/skills/` in a repo |

PowerShell (Windows), from the clone:

```powershell
$src = (Resolve-Path .\serhant-brand-skill).Path
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills","$env:USERPROFILE\.codex\skills","$env:USERPROFILE\.grok\skills" | Out-Null
New-Item -ItemType Junction -Force -Path "$env:USERPROFILE\.claude\skills\serhant-brand-skill" -Target $src
New-Item -ItemType Junction -Force -Path "$env:USERPROFILE\.grok\skills\serhant-brand-skill" -Target $src
Copy-Item -Recurse -Force $src "$env:USERPROFILE\.codex\skills\serhant-brand-skill"
```

macOS / Linux:

```bash
src="$(pwd)/serhant-brand-skill"
mkdir -p ~/.claude/skills ~/.codex/skills ~/.grok/skills
ln -sfn "$src" ~/.claude/skills/serhant-brand-skill
ln -sfn "$src" ~/.grok/skills/serhant-brand-skill
rm -rf ~/.codex/skills/serhant-brand-skill
cp -R "$src" ~/.codex/skills/serhant-brand-skill
```

Restart the tool after install. Invoke `/serhant-brand-skill` (Claude, Grok) or `$serhant-brand-skill` (Codex).

## Layout

| File | Owns |
|---|---|
| `SKILL.md` | Procedure |
| `references/serhant.md` | Book frameworks |
| `references/subject.example.md` | Empty profile template |

Optional: copy the example to `references/subject.md` for a local foundation the skill will load. That path is gitignored.

## Attribution

Frameworks from Serhant (2024). This is an operating procedure, not a reproduction of the book.
