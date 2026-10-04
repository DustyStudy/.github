# Contributing

Lightweight process; these are solo-maintained projects. If the repository
has its own `CONTRIBUTING.md`, follow that instead.

## Before opening a pull request

- Open an issue first for anything larger than a small fix, so the approach
  can be agreed before you write it.
- Run the checks the repository's CI runs (see `.github/workflows/`), and add
  or update tests for behaviour you change.
- Terraform: `terraform fmt -recursive` and `terraform validate`.
- Add a line to `CHANGELOG.md` under "Unreleased" for user-visible changes,
  where the repository keeps one.

## Guidelines

- No secrets, account IDs or real findings in source, tests, docs or issues.
- Never hardcode `arn:aws:`; take the partition from the provider so the
  code also works in GovCloud.
- Pin GitHub Actions to full commit SHAs and install tools from hash-pinned
  requirement files.
- Keep the README's claims aligned with what the tests demonstrate.

Pull requests are squash-merged and must pass every required check.
