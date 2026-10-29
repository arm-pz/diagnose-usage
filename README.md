# diagnose-usage

An AI agent skill (a `SKILL.md` for Claude Code) that works out why your Claude Code usage limit
drained faster than expected. You paste your `/usage` output; it checks it against the
heavy-session causes Boris Cherny of the Claude Code team named on 29 Oct 2026 (a raised effort
level, subagents inheriting it, `/goal`, workflows, Agent Teams, long SDK jobs) and gives you up
to three ranked culprits with one change each. It does not claim a bug: Anthropic's review found
no single root cause.

Siblings: [choose-effort](https://github.com/arm-pz/choose-effort) for deciding effort *before* a
task. For plan limits, prices and API billing, see Anthropic's docs; this skill does not cover
them.

## Install

```
npx skills add arm-pz/diagnose-usage --skill diagnose-usage
```

Or copy the repo files into `~/.claude/skills/diagnose-usage/` and start a new session.

## Ask it things like

- "Why is my Claude Code usage draining so fast today?"
- "I hit my Claude Code limit in an hour."
- "What does /usage actually show me?"

## Status

Structure checks done by hand; trigger cases in `references/trigger-cases.md` are hand-read
against the skill descriptions and **not** run in a live session. `check_skill.py`: OK, 0 fail
0 warn. Effort levels and commands change often, so the skill tells the agent to confirm them
against your `/effort` slider and the current docs.

## License

MIT — see [LICENSE](LICENSE).
