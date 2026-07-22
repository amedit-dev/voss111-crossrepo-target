# voss111-crossrepo-target

Write-target repo for the **R-VOSS-111** cross-authority (CVSS Scope:Changed)
proof — see `amedit-dev/mydos`, `vercel/reports/submitted/R-VOSS-111_cross_repo_proof/`
for the full setup and the `fire_cross_repo_proof.sh` script.

This repo has no other purpose. If `PROOF.md` exists here, it means a command
injected via `repository_dispatch` on `amedit-dev/voss111-actions-injection-poc`
(fired using a credential scoped only to `Contents:write` on that *other*
repo) used a separately-scoped `CROSS_REPO_PAT` — exfiltrated from that job's
own environment — to write to *this* repo. That's the different-security-authority
pivot needed to justify CVSS Scope:Changed on the underlying script-injection
finding.
