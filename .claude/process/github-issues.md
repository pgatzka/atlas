# GitHub issue tracking
 
All work is tracked in GitHub issues (G7). Use the `gh` CLI. Use real issue numbers from actual command output only — never invent or assume a number (G1).
 
## Conventions
- One open issue before any unit of work starts.
- Reference the issue in commits: include `#NN` in the message. Use `Closes #NN` to auto-close on merge.
- Close an issue only when its work is done and verified — not when you assert it is.
- Stage approvals come from me. You may log my approval as an issue comment, but never self-close a gate.
- If there's no repo or `gh` isn't authenticated: STOP and ASK — don't skip tracking.
## Commands (PowerShell)
- Check auth: `gh auth status`
- Create: `gh issue create --title "Short title" --body "What and why"`
- List open: `gh issue list --state open`
- View one: `gh issue view 12`
- Comment: `gh issue comment 12 --body "note"`
- Close: `gh issue close 12`
## Optional (tune to taste)
- Label issues by stage: `--label stage-1` etc.
- Group a project's stages under a milestone: `--milestone "v1"`.
 
