# nrstack

The agent skills I use every day. Say the two words; no slash needed.

## Skills

| Skill | Say | What it does |
|---|---|---|
| `design-options` | "design options", "mock it" | Shows a UI change as one picture in the thread: options, a before and after, or the end state. |
| `dumb-down` | "dumb down", "plain intl" | Restates the last message in half the words, in plain English, with every decision kept and numbered. |
| `run-retro` | "run retro" | Finds what cost the session time and the environment fix for each: at most five, most costly first. Changes nothing until you pick. |

Each skill is hill-climbed against real sessions and graded blind: `design-options` scores 7.5/10 against 6.8 for the skill it replaced, `dumb-down` 7.5 against 5.7, and `run-retro` 6.9 against 6.6.

## Install

```bash
npx skills add noelrohi/nrstack
```

Or copy them by hand:

```bash
git clone https://github.com/noelrohi/nrstack
cp -R nrstack/skills/* ~/.claude/skills/   # Claude Code
cp -R nrstack/skills/* ~/.codex/skills/    # Codex
```

`design-options` uses T3 Code's `html_preview` and `html_render` when they are available, and writes an HTML file otherwise.

## License

[MIT](LICENSE)
