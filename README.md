# 🔺 pyramid

**A hierarchical agent-orchestration doctrine for Claude Code — one conductor, opus lanes, verified sonnet helpers.**

```
        FABLE (main)      — conducts, judges, integrates. Never bulk-works.
       /   |   \
   OPUS  OPUS  OPUS…      — the workhorses: build / review / validate lanes.
   /|\    |     /|\
  S S S   S    S S S      — ≤3 SONNET classic subagents per opus, opus-verified.
```

`/pyramid` (alias `/pyr`) is a Claude Code **skill** that encodes a battle-tested way to run
multi-agent work from a top-tier main session:

- **Tier 0 — the conductor**: the main session orchestrates and stays available; it never
  bulk-works, never spawns subagents on its own (expensive) model, and verifies every
  lane's output independently, by sampling.
- **Tier 1 — opus lanes**: disjoint-scoped worker agents with engineering-grade briefs —
  outcome spec, boundary contract, escalation clause ("stuck → say so and STOP"), report
  format with `file:line` evidence.
- **Tier 2 — sonnet helpers**: each opus may offload to **up to 3** classic subagents,
  briefed only with what their opus hands them. The opus re-runs their tests, reads their
  diffs, and asks *"is there anything better that could be done?"* unless the result is
  perfect — cheap throughput, supervised.
- **Park protocol**: a pause order parks the whole pyramid instantly (stop work, stay
  resident, zero burn, context intact) — agents are killed only when explicitly asked.
- **Directive inheritance**: every tier embeds the next tier's rules **verbatim** in its
  briefs (paste-ready boilerplates included) — because a model fills spec gaps with
  confidence, not common sense.

## Install

```bash
git clone https://github.com/fire17/pyramid ~/tmp-pyramid
cp -R ~/tmp-pyramid/skills/pyramid ~/.claude/skills/pyramid
mkdir -p ~/.claude/skills/pyr && ln -s ../pyramid/SKILL.md ~/.claude/skills/pyr/SKILL.md
rm -rf ~/tmp-pyramid
```

Then type `/pyramid` (or `/pyr`) in Claude Code before spawning agent waves.

## What's in this repo

- `skills/pyramid/SKILL.md` — the skill (the product).
- `skills/workflow-model-guard/` — the companion pre-spawn model guard it references.
- `files/memory/` — the two standing-directive memory notes the skill was distilled from.
- `CONTINUE.md` + `.save_and_ship/` — snapshot provenance (this repo doubles as the
  project's checkpoint; the originating session transcript is retained privately).

## Why

Born 2026-07-06 from a real session: five parallel review lanes + four build lanes shipped
a scored, evidence-backed engineering audit and its fixes in one sitting — then a pause
order taught the park-don't-kill rule, and token economics taught the sonnet tier. The
skill exists so none of that has to be re-explained to any future session.

## License

MIT © fire17
