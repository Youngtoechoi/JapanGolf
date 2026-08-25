# caveman (vendored)

`SKILL.md` here is a verbatim copy of the upstream Caveman skill.

- Source: https://github.com/JuliusBrussee/caveman
- Path upstream: `skills/caveman/SKILL.md`
- Commit: `81536f57b3303b7de7f5bc5b564cc344f9112d68` (2026-08-25)
- License: MIT (upstream `LICENSING.md` classifies all of `skills/` as MIT).
  Copy of the notice is in `LICENSE` next to this file.

## Why vendored instead of installed as a plugin

Upstream ships a full Claude Code plugin (`claude plugin install caveman@caveman`)
that adds SessionStart/UserPromptSubmit hooks, a statusline badge, token-savings
stats, and companion skills. None of that is here — this is the prompt-only core,
which is self-contained and needs no hooks.

Trade-off: no auto-activation on session start, no `/caveman-stats`, no statusline
badge. Type `/caveman` once per session instead.

## Full plugin install

To get the hooks and companion skills on your own machine:

```
claude plugin marketplace add JuliusBrussee/caveman
claude plugin install caveman@caveman
```

If you do that, delete this vendored copy so the two don't both define `caveman`.

## Updating the vendored copy

Re-copy `skills/caveman/SKILL.md` from upstream and update the commit hash above.
Do not hand-edit `SKILL.md` — local edits make the next update a merge.
