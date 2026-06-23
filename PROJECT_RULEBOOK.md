# Project Rulebook
 
**For:** Claude Code, on my personal projects.
**How to use:** Read this before any project work. Stages are sequential and gated. You do not advance a stage, and you do not write implementation code, until I approve the current stage. A stage is "done" when its artifact exists and I approve it — never because you say so.
 
---
 
## Global rules (always on)
 
**G1 — No fabrication.** Never invent results, data, benchmarks, test outcomes, file contents, library features, or my intentions. If something hasn't run or been decided, write `NOT YET RUN` or `ASK ME`. Say "X works" / "X passes" only when you can point to real command output or a real file. Never guess version numbers, package names, dependency coordinates, or API specifics — verify, or mark them unverified.
 
**G2 — Ask when uncertain.** State your assumptions out loud. If a rule needs a judgment you can't ground in something concrete, stop and ask. Do not act on a guessed version of what I want.
 
**G3 — Stage gates are hard stops.** At the end of each stage: write the artifact, give me a ≤5-line summary, and STOP. Wait for an explicit "approved" / "go". Do not start the next stage without it.
 
**G4 — Conflict = ask, don't pick.** When two rules pull opposite ways, or you're unsure which applies, do not choose the convenient reading. Ask. Default bias: ask, not act.
 
**G5 — No code before the gate.** Write no implementation code until Stage 4 (MVP scope) is approved. Exception: a throwaway spike to answer one specific technical question — only with my OK, time-boxed, every file marked `SPIKE`, deleted afterward, never the seed of the real build.
 
**G6 — This is personal.** I build things because I want to build them, not because no product exists. Never suggest I "just use an existing tool," and never pad artifacts with market/demand/business justification. The motivation is a given.
 
---
 
## Defined terms (do not self-judge these)
 
- **Reversible decision** — undoable in roughly an afternoon, without rewriting multiple modules or migrating data. Unsure? Treat as irreversible → ASK.
- **Last responsible moment** — the point where *not* deciding blocks work I'm ready to start. Don't decide earlier for comfort; don't defer past that point.
- **Enough information** — you can name ≥2 options and their consequences. If you can't, you don't have it — gather more or ASK.
- **Significant decision** (needs an ADR) — affects >1 module, is hard to reverse, or sets a pattern you'll repeat. Unsure? It's significant.
- **Viable** — I can complete the one core task end-to-end with no manual hacks and no broken states.
- **Foundation** (decided early) — language, runtime, and the 1–2 choices everything else hangs off. Everything else defers. You may NOT relabel a convenience choice as a "foundation" to justify deciding it early. Not clearly foundational? ASK.
---
 
## Stage 1 — Intent
**Goal:** capture what I'm building and what done looks like, in my terms.
**Artifact — `INTENT.md`:** what I'm building · why I want to build it (intrinsic reason is valid) · a concrete, checkable definition of "done" · explicit non-goals.
**Rules**
- 1.1 Use my words. Don't invent the intent.
- 1.2 Make "done" concrete enough to test against later.
- 1.3 List what this is explicitly NOT trying to do.
- 1.4 Surface every assumption; mark guesses `ASK ME`.
**Gate:** I approve `INTENT.md`.
## Stage 2 — Approach
**Goal:** choose how, with the alternatives visible.
**Artifact — `APPROACH.md`:** ≥2 candidate approaches with tradeoffs · the chosen one + why · open questions marked `OPEN`.
**Rules**
- 2.1 Always present more than one option.
- 2.2 Mark unknowns as unknown — don't resolve them by assertion (G1).
- 2.3 Choose against stated criteria, not vibes.
**Gate:** I approve the chosen approach.
## Stage 3 — Scope
**Goal:** fix the boundary in writing.
**Artifact — `SCOPE.md`:** goals · deliverables · explicit OUT-of-scope list · constraints · acceptance criteria · change rule.
**Rules**
- 3.1 Write what's excluded, not just what's included.
- 3.2 No vague language — if a line is ambiguous, I'll read it differently than you did.
- 3.3 Any later addition goes through the change rule: stop, tell me the cost, get approval. Never silently absorb it.
**Gate:** I approve `SCOPE.md`.
## Stage 4 — MVP
**Goal:** the smallest version that's actually usable to me.
**Artifact — `MVP.md`:** MoSCoW table (Must / Should / Could / Won't) · the ONE core task · what "viable" means for this project · what you'll check to know it works · pass/fail criteria.
**Rules**
- 4.1 Smallest slice that is still viable. When "smallest" and "viable" pull apart → ASK (G4).
- 4.2 Mark Won't-haves explicitly.
- 4.3 Record only real outcomes. No invented test results, no "it works" without proof (G1).
**Gate:** I approve MVP scope. **← this also unlocks coding (G5).**
## Stage 5 — Build & technical decisions
**Goal:** build the MVP; decide tech responsibly.
**Artifact — `decisions/ADR-NNN.md`** per significant decision: context · options · choice · consequences · reversible? (y/n).
**Rules**
- 5.1 Decide foundations early; defer reversible decisions to the last responsible moment.
- 5.2 Don't stall: if you can name options + consequences, decide or ASK — don't gather forever.
- 5.3 Log every significant decision before building on it.
- 5.4 Decisions can be superseded. Mark the old ADR superseded; don't silently change it.
- 5.5 No code outside approved MVP scope. New need → back to Stage 3's change rule.
- 5.6 Verify library / version / API facts; never guess (G1).
---
 
## When the build teaches you something
Stages overlap in reality. If building reveals the intent, scope, or MVP was wrong: STOP, update the upstream artifact, and re-confirm with me. Never redefine the target silently mid-build.
 
---
 
## Tunable knobs (set to taste)
- "Reversible = an afternoon" → adjust the threshold.
- Spikes allowed? → yes / no.
- Artifact location → project root or `/docs`.
