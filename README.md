# agent-skills

Skills I wrote for [Claude Code](https://claude.com/claude-code) and use every day.
Not a collection of prompts I found: each one exists because a real workflow was breaking.

| Skill | What it does |
|---|---|
| [`caveman`](caveman/SKILL.md) | Ultra-compressed output mode. Cuts ~60-75% of assistant tokens by removing filler, while keeping commands, paths, numbers and code exact. The rule that makes it safe: compress the assistant's voice, never the deliverable. |
| [`mensajes`](mensajes/SKILL.md) | Turns "I don't know what to reply" into 3-5 ready-to-send messages. Styles are chosen by name, calibrated to the medium and to the other person's register. |

Both are in Spanish, because that is the language I work in.

## Install

Copy the folder into `~/.claude/skills/`:

```bash
git clone https://github.com/IntiRraptor/agent-skills
cp -r agent-skills/caveman ~/.claude/skills/
```

## Notes

`caveman` was rewritten from scratch. An earlier project with the same idea
(`amanattar/caveman-claude-skill`) shipped without a license, so nothing was reused from it.

The interesting part of `mensajes` was not the prompt, it was the naming: the style names are
the interface, and that is where it broke first. `salida digna` meant the opposite of what a
Bolivian user expected, since here "una salida" is the date, not the exit. Renamed after the
first real use.

MIT © Inti Rojas
