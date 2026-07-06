# Pyramid — hierarchical agent-orchestration doctrine skill
**Snapshot 2026-07-06 by session 880c944b (Tokenomics MEGA WORK session). Fresh-space briefing.**

## What this is
`/pyramid` (alias `/pyr`) — fire17's standing doctrine for how a Fable main session runs
agent hierarchies: **Fable conducts → opus lanes work (agentteam/tmux swarms or Agent-tool
teammates) → each opus may offload to ≤3 SONNET classic (non-tmux) subagents it must
verify entirely**. Includes the park-on-pause protocol (park immediately, never kill unless
told), the never-Fable model guard + banner, directive-inheritance law with paste-ready
opus/sonnet brief boilerplates, tmux swarm + fleet hygiene, and the engineering-principles
brief ingredients. Born from fire17's 2026-07-06 directive after a session where this exact
workflow (5 opus review lanes + 4 opus build lanes, evidence-backed briefs, park order)
worked well — minus two corrections now baked in: pause means PARK not kill, and the new
sonnet offload tier.

## Current state (honest)
- Skill LIVE at `~/.claude/skills/pyramid/SKILL.md`; alias dir `~/.claude/skills/pyr/`
  (SKILL.md → symlink `../pyramid/SKILL.md`). Registration live-verified in-session (both
  appeared in the available-skills list). Ghost-text/argument-hint not visually verified
  in a composer yet.
- Consistency sweep: `~/.claude/skills/workflow-model-guard/SKILL.md` gained a sonnet
  tier row pointing to /pyramid.
- Vault-synced (living library): `~/Creations/Skills/{pyramid,pyr,workflow-model-guard}`
  (✔ synced, provenance recorded). THIS directory is the frozen point-in-time snapshot.
- Not yet exercised on a real mission since creation — the doctrine it encodes WAS
  exercised this session; the skill file itself is untested as a trigger.

## Original locations of everything copied here
- `conversation/880c944b-….jsonl` ← `~/.claude/projects/-Users-magic-Tokenomics/` (SACRED
  verbatim, point-in-time; session continued after the copy). `cship-880c944b….json` ←
  `~/.cship/live/`.
- `skills/pyramid/`, `skills/workflow-model-guard/` ← `~/.claude/skills/…` (pyr's SKILL.md
  is a symlink live; stored here as a plain copy-note file).
- `files/memory/{opus-sonnet-pyramid,pause-means-park-agents}.md` ←
  `~/.claude/projects/-Users-magic-Tokenomics/memory/`.
- NOT copied (their own durable homes): the Tokenomics repo work this session
  (`/Users/magic/Tokenomics`, its own git; see `.deify/review-2026-07-06/` +
  `.deify/PAUSE-CHECKPOINT-2026-07-06.md` there), subagent transcripts (same
  `~/.claude/projects/-Users-magic-Tokenomics/` bucket), secrets (none involved).

## How to resume
- `claude --resume 880c944b-c0b2-4468-b00d-35fb4aa82036` from `/Users/magic/Tokenomics`,
  or read `conversation/` here. The paused Tokenomics v1-rc mission resumes via
  `/Users/magic/Tokenomics/.deify/PAUSE-CHECKPOINT-2026-07-06.md` §4.

## Next steps
1. Trigger-test /pyramid on a real spawn wave; tune the description if it undertriggers.
2. Consider folding the fire17-behavioral-directives memory pointer into the skill's §5.
3. On any skill edit: re-run `python3 ~/Creations/Skills/sync_skill.py ~/.claude/skills/pyramid --note "…"` (vault law).
