# Phase B validation

- Full unit suite: **163 tests passed**, including 18 new Phase B tests and the merged timing/rounding engine tests.
- Command: `uv run --no-sync python -B -m unittest discover -s tests/unit -v`.
- Clean-copy reproduction: **all 15 generated output hashes match**. The copy contains shared code, config and committed processed inputs; no raw production directory or credentials. Network connection creation is disabled during that test.
- Compilation: all shared source, scripts and unit tests compile.
- Existing Phase A fixture demonstration passes.
- `git diff --check` and staged private-path/secret scans pass.
- No dependency, lockfile, configuration, original notebook or strand-engine changes belong to this contribution.
- Coverage: **148/148 dates, 100%**, identical in all four frozen masks.
- Reference AUMs: destination/timing **$10m**, capacity **$1bn**, rounding **$1m**. Core grid unchanged.
- No empirical RMSE aggregation, preferred-method selection or Section 5 execution.

Validated with team main `a5fcb989e6aa6469ba09f8f1cf16d729fd5f8a20` incorporated. The branch also contains the unchanged PR #26 validation dependency; merge that PR first. The normal working tree and the PR #22, notebook and Issue #4 worktrees remain untouched.
