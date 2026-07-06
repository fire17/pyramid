---
name: pause-means-park-agents
description: "fire17 standing order — \"pause the agents\" means PARK them (halt work, keep alive + resumable), NEVER TaskStop/kill unless he explicitly says close/kill"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 880c944b-c0b2-4468-b00d-35fb4aa82036
---

When fire17 says to pause/stop agents (e.g. token limits), **PARK them immediately — do not terminate them.** Park = SendMessage each active agent: "PARK NOW: stop ALL work this instant, stay resident, await resume" (no handoff-writing requirement — that spends tokens too). Idle/parked teammates burn ZERO tokens, so parking achieves the full token freeze while keeping every agent's in-context state intact for instant resume. Kill (TaskStop) ONLY when he explicitly says close/kill/clean up.

**Why:** On 2026-07-06 I TaskStop-killed the whole fleet (7 agents incl. 2 mid-build) on his "pause all agents" order. He corrected me: "next time i ask please dont close the agents but rather park them immediately ok?" Killing lost the two builders' working context, turning resume into finish-or-revert triage of half-written files; parked agents would have resumed mid-task for free.

**How to apply:** Pause order → (1) instantly SendMessage "PARK NOW, stop work, stay resident, await resume" to every ACTIVE agent; (2) leave idle agents untouched (they cost nothing); (3) write/refresh the durable checkpoint from main; (4) on resume, SendMessage "resume" to parked agents — they continue with context intact. Sequencing per his words: park FIRST, immediately; checkpoint/other safety steps after. Related: [[fire17-behavioral-directives]], [[tokenomics-project]].
