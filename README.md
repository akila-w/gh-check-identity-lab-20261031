# gh-check-identity-lab-20261031

Disposable, public sandbox for **Stage 45B-2 — GitHub required-check identity and collision testing**.

Every file here is **synthetic**. There is no real catalogue data, no credentials, and no
production code. This repository is temporary and will be deleted once the experiment evidence
has been preserved.

## What this is

A controlled lab to test whether a pull-request-controlled GitHub Actions job that reports the
same check name as a genuine trusted job can affect a required status check.

- `.github/workflows/catalogue-publication-trusted.yml` — the **genuine trusted check**. Because
  it is triggered by `pull_request_target`, GitHub always runs the workflow definition from the
  default branch, not from the pull request. It decides pass/fail by **inspecting** synthetic
  PR-head data through the REST API, and never checks out or executes pull-request code.
- `catalogue.json` — synthetic catalogue. Its `publication_signal` field is the only input the
  trusted check reads from a PR head (`PASS` → success, anything else → failure).

No third-party Actions are used; the workflow calls only the GitHub REST API via the built-in
`GITHUB_TOKEN` with read-only `contents` permission.
