## install with 

```shell
ln -s ~/.agents/AGENTS.md ~/.claude/CLAUDE.md
ln -s ~/.agents/AGENTS.md ~/.pi/agent/AGENTS.md
ln -s ~/.agents/AGENTS.md ~/.codex/AGENTS.md
ln -s ~/.agents/AGENTS.md ~/.config/opencode/AGENTS.md


for dest in ~/.claude/skills ~/.codex/skills ~/.pi/agent/skills ~/.config/opencode/skills; do
  mkdir -p "$dest"
  for s in ~/.agents/skills/*/; do ln -sfn "${s%/}" "$dest/$(basename "$s")"; done
done
```

## Update the skills

```shell
npx skills@latest update
```

Run the skills loop again after an update to link new skills.
