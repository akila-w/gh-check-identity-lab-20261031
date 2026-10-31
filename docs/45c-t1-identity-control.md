# Stage 45C-2 T1 identity-enforcement control (disposable)

This file belongs to a disposable sandbox pull request used to test which GitHub App
must supply the required check `catalogue-publication-trusted`.

- Repository: `akila-w/gh-check-identity-lab-20261031` (sandbox only).
- The required check is pinned to the dedicated trusted-check App (App ID 5555097).
- The root `catalogue.json` `publication_signal` is set to `PASS` only so the legacy
  synthetic GitHub Actions workflow (App ID 15368) finishes with `success`. That value is
  synthetic test data. It is not an input to the trusted publisher's verdict.
- Expected result before any trusted publication: the PR stays blocked, because a
  success from App 15368 cannot satisfy a check pinned to App 5555097.

Disposable test data. Never merge this pull request or this branch.
