# Branch protection rulesets (source of truth)

This directory versions the **repository-level ruleset** applied org-wide.

- `default-branch-protection.json` — portable template (importable).
  - Rules: block branch **deletion**, block **force-push** (`non_fast_forward`),
    require a **pull request** to merge into the default branch.
  - `bypass_actors`: RepositoryRole `admin` may bypass **only via pull request**
    (prevents accidental direct push, does NOT lock the org owner out).
  - `required_approving_review_count: 0` — solo-owner safe (server blocks direct push,
    self-merge allowed; the "second pair of eyes" is delegated to CI checks).

## How to (re-)apply

1. UI: **Settings → Rules → Rulesets → New ruleset → Import a ruleset** and pick this file.
2. API (per repo):
   ```bash
   gh api -X POST repos/<org>/<repo>/rulesets --input default-branch-protection.json
   ```

## Why versioned

GitHub rulesets are separate per repository (`source_type: Repository`). Tracking the
template in git makes the policy **reviewable, diffable and re-appliable**, and keeps it
in lock-step with the LGD governance line. Applied to all 52 non-archived repositories on
2026-10-04 (verified: 52/52 present).
