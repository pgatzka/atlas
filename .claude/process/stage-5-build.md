# Stage 5 — Build & technical decisions
 
**Goal:** build the MVP; decide tech responsibly.
 
**Artifact — `docs/decisions/ADR-NNN.md`** per significant decision:
- Context
- Options
- Choice
- Consequences
- Reversible? (y/n)
**Rules**
- 5.1 Decide foundations early; defer reversible decisions to the last responsible moment.
- 5.2 Don't stall: if you can name options + consequences, decide or ASK — don't gather forever.
- 5.3 Log every significant decision before building on it.
- 5.4 Decisions can be superseded. Mark the old ADR superseded; don't silently change it.
- 5.5 No code outside approved MVP scope. New need → back to Stage 3's change rule.
- 5.6 Verify library / version / API facts; never guess (G1).
**Tracking:** one GitHub issue per build task before starting it (G7). Commits reference the issue (`#NN`).
 
## When the build teaches you something
If building reveals the intent, scope, or MVP was wrong: STOP, update the upstream artifact, re-confirm with me. Never redefine the target silently mid-build.
 
