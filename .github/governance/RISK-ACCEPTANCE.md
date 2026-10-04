# Governance — Residual Risk Acceptance & Disposition Record

**Scope:** `Medxpert-org` and `SynomosAI` organizations (all non-archived repositories)
**Date:** 2026-10-04
**Audit baseline:** `github-org-governor` audit — **PASS=366 / FAIL=105 / WARN=0** (post tool-fix, see §4)

This record formally dispositions every residual `FAIL` reported by the governance auditor.
Each residual FAIL is either (a) fixed, (b) **accepted** with rationale, or (c) **deferred**
to a named human action. Nothing is left unaddressed.

## 1. Residual findings and disposition

| Class | Count | Finding | Disposition | Rationale | Re-evaluate when |
|---|---|---|---|---|---|
| **C5** | 52 | PR review does not *require* CODEOWNERS sign-off | **ACCEPTED** | The org has a **single** human admin. Requiring CODEOWNERS review would make every PR unmergeable — an author cannot approve their own PR — a hard self-lock. The "second pair of eyes" role is delegated to CI checks. | A second human member/account is added |
| **C7** | 51 | `validate-codeowners` is not a required status check | **ACCEPTED (design choice)** | GitHub **Free** has no org-level required workflows. A per-repo required check is only safe when the check is guaranteed to report on *every* PR; a required check that can fail to report creates a **permanent PR deadlock** (observed live on 2026-10-04 — see `ENFORCEMENT-PROOF.md`). The check is therefore required only on `.github`, the one repository that carries the workflow unconditionally. | Free→Team upgrade, or the workflow is rolled out to all repositories |
| **O1** | 2 | Org two-factor authentication required = `false` | **DEFERRED → manual** | GitHub exposes **no write API** for org-level 2FA enforcement (a `PATCH` returns 200 but silently no-ops). It must be toggled in the web UI. | Owner action (see §2) |

**Total residual: 105 = 100% dispositioned. Un-explained FAILs: 0.**

## 2. Outstanding human action (owner)

- [ ] Enable **Require two-factor authentication** for **each** organisation:
  `https://github.com/organizations/<org>/settings/security` → *Authentication security* →
  *Require two-factor authentication* → **Save**.
  Applies to both `Medxpert-org` and `SynomosAI`. No member-removal risk (the sole member already has 2FA).

## 3. Controls currently enforced (context)

Applied org-wide and independently verified (see `.github/rulesets/` and
`.github/governance/ENFORCEMENT-PROOF.md`):

- Default-branch **ruleset** on all 52 active repositories: required PR, no force-push, no branch
  deletion — server-enforced; admin bypass restricted to `pull_request` mode.
- **Secret scanning + push protection** and **Dependabot alerts** on all repositories.
- **CodeQL** code scanning default setup on every repository with an analysable language (16).
- **OSSF Scorecard** workflow on 16 repositories (SARIF uploaded; `publish_results=false`).
- Actions restricted to **GitHub-owned + verified creators**; all third-party actions
  **pinned to full commit SHA**; `sha_pinning_required=true`.
- **Private vulnerability reporting** enabled org-wide; org **SECURITY.md** published.
- **Fork-PR workflow approval** = `all_external_contributors`.

## 4. Tool defect corrected (integrity note)

The auditor previously reported **53 `O2_team_member` FAILs** ("empty gatekeeper") for teams that
in fact **have members**. **Root cause:** the *list* endpoint `GET /orgs/{org}/teams` does **not**
return a `members_count` field, so the check read `None → 0` for every team. **Fix:** read the
*single-team* endpoint `GET /orgs/{org}/teams/{slug}`, which **does** return `members_count`.
After the fix the 53 false FAILs disappear (**158 → 105**). An earlier fix removed **12** false
FAILs from **archived** repositories that the auditor failed to skip. Both defects were caught by
the "who-tests-the-tester" pass.

## 5. Review cadence

Re-run the auditor and re-affirm this record **monthly**, or on any change to: organisation
membership, GitHub plan, or the repository set.

---

© 2026 赵兴华 (Steven Zhao · China). All rights reserved — this governance record is published so
the organisation's own posture is verifiable; no licence to reuse is granted.
`SynomosAI` and `MedXpert` are used as **unregistered** names only: **no entity registration and no
trademark registration have been applied for.**
