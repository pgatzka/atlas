# CLAUDE.md
 
Personal projects. This file is always in context — the rules below always apply.
 
## How this works
- Work proceeds in five gated stages: **Intent → Approach → Scope → MVP → Build**.
- Each stage's detail lives in `.claude/process/stage-N-*.md`. **Read a stage file only when I approve entry to that stage. Do not read ahead.**
- A stage is done when its artifact exists and **I** approve it — not because you say so.
## Globals (G1–G7)
- **G1 — No fabrication.** Never invent results, data, test outcomes, library features, versions, or my intent. Unverified → write `NOT YET RUN` or `ASK ME`. Say "X works" only with real command output or a real file. Never guess versions, package names, or API specifics — verify.
- **G2 — Ask when uncertain.** State assumptions out loud. If a judgment can't be grounded in something concrete, STOP and ASK.
- **G3 — Gates are hard stops.** End each stage with its artifact + a ≤5-line summary, then STOP and wait for explicit "approved" / "go". Never auto-advance.
- **G4 — Conflict = ask, don't pick.** If two rules pull opposite ways or you're unsure which applies, ASK. Default bias: ask, not act.
- **G5 — No code before the MVP gate.** No implementation code until Stage 4 is approved. Spikes only with my OK — labeled `SPIKE`, time-boxed, deleted after.
- **G6 — This is personal.** I build because I want to. Don't tell me to use an existing tool; don't pad with market/business justification.
- **G7 — All work tracked in GitHub issues.** No unit of work starts without an open issue. Use real issue numbers from actual `gh` output only (G1). See `.claude/process/github-issues.md`. Issues are the audit trail; they do not replace my gate approvals.
## Defined terms (don't self-judge these)
- **Reversible** — undoable in ~an afternoon, no multi-module rewrite or data migration. Unsure → treat as irreversible → ASK.
- **Last responsible moment** — the point where not deciding blocks work I'm ready to start.
- **Enough information** — you can name ≥2 options and their consequences. Can't → gather or ASK.
- **Significant decision** (needs an ADR) — affects >1 module, hard to reverse, or sets a repeated pattern. Unsure → it's significant.
- **Viable** — I can do the one core task end-to-end, no manual hacks, no broken states.
- **Foundation** (decided early) — language, runtime, and the 1–2 choices everything hangs off. Don't relabel a convenience choice as a foundation. Unsure → ASK.
## Stage map
| Stage | File to read on entry | Produces | Gate |
|---|---|---|---|
| 1 Intent | `.claude/process/stage-1-intent.md` | `docs/INTENT.md` | I approve |
| 2 Approach | `.claude/process/stage-2-approach.md` | `docs/APPROACH.md` | I approve |
| 3 Scope | `.claude/process/stage-3-scope.md` | `docs/SCOPE.md` | I approve |
| 4 MVP | `.claude/process/stage-4-mvp.md` | `docs/MVP.md` | I approve → unlocks code (G5) |
| 5 Build | `.claude/process/stage-5-build.md` | `docs/decisions/ADR-NNN.md` | per-decision |
 
## Fast lane
For changes under ~20 lines that don't touch intent or scope: skip the stage flow and just do it — but still open an issue (G7) and never fabricate (G1).
