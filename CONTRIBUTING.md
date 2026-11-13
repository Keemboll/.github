# Contributing to Keemboll

Thanks for helping improve Keemboll! This guide applies to **every repository in the organization**. Individual projects may add their own `CONTRIBUTING.md` with project-specific rules (for example, how to add a skill to `keemboll-bi`); when they do, that file takes precedence for details and this one covers the rest.

By participating, you agree to keep discussions respectful and constructive. By contributing, you agree that your work is released under the licence of the repository you contribute to (Apache-2.0 unless stated otherwise).

## Our scope

Keemboll hosts open-source BI projects: semantic modeling, DAX / SQL / M, analytics engineering, data quality, governance, documentation and delivery tooling. If your idea fits that scope, it is welcome — even if it targets a tool or platform we do not yet cover.

## Ways to contribute

- **Report a bug** — wrong output, broken script, failing install.
- **Request or propose a feature** — describe the BI task, who needs it, and what a good result looks like.
- **Improve documentation** — clearer wording, better examples, missing prerequisites.
- **Test on real projects** — tell us what worked or failed on your own models and data. This is among the most valuable contributions we can get.
- **Propose a new project** — see below.

## Proposing a new project

Open a thread in [organization discussions](https://github.com/Keemboll/.github/discussions) with:

1. **Problem** — which BI task is painful today, and for whom
2. **Scope** — what the project will and will not do
3. **Platforms** — Power BI, Fabric, dbt, DuckDB, SQL engines, others
4. **Maintainer** — who will own it
5. **First deliverable** — the smallest useful version

A project is accepted when it is useful on its own, documented, openly licensed and has a named maintainer.

## Before you start

1. Search the repository's existing issues and pull requests to avoid duplicates.
2. For anything larger than a small fix, open an issue first so we can agree on the approach.
3. Read the repository's `README.md` and, if present, `AGENTS.md` or other project guidelines.

## Development workflow

```bash
git clone https://github.com/Keemboll/<repository>.git
cd <repository>
git checkout -b my-change

# make your changes, run the project's checks
# (see the repository README for the exact command, e.g. python scripts/validate.py)
```

Then open a pull request against `main`. CI must pass before review.

## Quality bar (all projects)

- **Correct** — code, queries and models must run and be valid. Verify on a real model or dataset whenever you can, and say when you could not.
- **Specific** — state precisely what a feature does and does not cover.
- **Safe** — no destructive operations without an explicit confirmation step; never commit credentials, tenant IDs or real customer data.
- **Documented** — update the README, examples and changelog for any user-visible change.
- **Portable** — prefer open formats and plain-text artifacts; avoid wording or code that only works with a single vendor or agent.
- **Tested** — add or update tests when the repository has them.

## Commits and pull requests

- Keep commits and pull requests focused on one change.
- Use clear commit messages. Some repositories (such as `keemboll-bi`) derive automatic version bumps from the **commit message prefix** — follow the convention in that repository, for example:

```
fix: correct time-intelligence pattern
feat: add incremental-refresh review
docs: clarify install steps
```

- Never edit generated files by hand (for example `marketplace.json` in `keemboll-bi`); CI regenerates them.

### Pull request checklist

- [ ] The project's checks pass locally
- [ ] The change is focused and explained in the PR description
- [ ] Documentation and changelog are updated if behaviour changed
- [ ] Examples are marked as tested or untested
- [ ] No secrets or private data are included

## Reporting security issues

Please do **not** open a public issue for a security problem. Use GitHub's private vulnerability reporting (repository **Security** tab → *Report a vulnerability*) or contact the maintainer directly.

## Questions

Ask in [organization discussions](https://github.com/Keemboll/.github/discussions) or open an issue with the `question` label. Thanks for contributing!
