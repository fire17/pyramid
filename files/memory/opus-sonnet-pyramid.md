---
name: opus-sonnet-pyramid
description: "fire17 standing order — whenever making opus agents, each opus may run up to 3 SONNET classic (non-tmux) subagents to offload work, but must verify everything itself; codified in the /pyramid skill"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 880c944b-c0b2-4468-b00d-35fb4aa82036
---

Whenever fire17 asks for opus agents (swarms, agentteams, workers): each opus agent is ALLOWED (encouraged, to conserve opus tokens) to spawn up to **3 sonnet classic subagents** — normal non-tmux Task/Agent subagents, NOT agentteams — receiving context ONLY from their opus parent. The opus uses them as it pleases to take workload off, but **must manage and verify everything itself** (sonnets err more than opus): re-run tests, read diffs, own the result, and unless a sonnet's output is perfect, ask "is there anything better that could be done?" and improve it before integrating.

**Why:** fire17's directive 2026-07-06 ("to conserve opus tokens… they need to manage and verify everything themselves though as sonnets can make more mistakes than opus"). Extends the standing model doctrine (never Fable subagents; opus workhorse; haiku trivial-only).

**How to apply:** embed the sonnet allowance + verification duty VERBATIM in every opus brief (directive inheritance — a spec gap gets filled with confidence); the /pyramid skill (`~/.claude/skills/pyramid/`) is the canonical enforcement — load it whenever spawning opus agents. Pairs with [[pause-means-park-agents]] (park orders relay down the pyramid instantly) and [[fire17-behavioral-directives]].
