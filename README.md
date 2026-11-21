# diagnose-usage

An agent skill for Claude Code and Codex that diagnoses unexpected usage after a run. It compares the run with the evidence you have, gives up to three supported causes, and recommends one change to test per cause.

In Claude Code, provide the relevant usage breakdown. In Codex, start with the affected usage window and add session or turn data if available. See the [Codex usage workflow](references/codex-usage.md).

Use [choose-effort](https://github.com/arm-pz/choose-effort) for upcoming work.

## Install

```
npx skills add arm-pz/diagnose-usage --skill diagnose-usage
```

Or copy the repo files into `~/.claude/skills/diagnose-usage/` for Claude Code or `~/.agents/skills/diagnose-usage/` for Codex.

## Ask it things like

- "Why is my Claude Code usage draining so fast today?"
- "I hit my Claude Code limit in an hour."
- "What does /usage show for this Claude Code run?"
- "Did yesterday's Codex automation use up my quota, or is that an account-wide number?"

## Status

Trigger cases in `references/trigger-cases.md` were reviewed by hand. Live activation was not measured.

## License

MIT — see [LICENSE](LICENSE).
