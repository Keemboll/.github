# Security Policy

Keemboll maintains open-source BI tooling. Many of our projects are instructions, templates and scripts that coding agents or developers run on real analytics projects, so we take security reports seriously — including reports about what a skill might cause an agent to do.

This policy applies to **every repository in the Keemboll organization** unless a repository publishes its own `SECURITY.md`.

## Supported versions

Security fixes are provided for the **latest release** of each project. Older versions are not patched; please upgrade first and check whether the issue persists.

| Project | Supported |
|---|---|
| [keemboll-bi](https://github.com/Keemboll/keemboll-bi) | Latest release (`v2.x`) |

## Reporting a vulnerability

**Please do not open a public issue, discussion or pull request for a security problem.**

Report it privately, by either:

1. **GitHub private vulnerability reporting** (preferred): open the affected repository, go to the **Security** tab, then **Report a vulnerability**.
2. **Email**: `lgeobatpo98@gmail.com` with the subject `[Keemboll security] <repository> — <short summary>`.

Please include:
- the repository, version or commit, and the file(s) involved
- a description of the issue and its impact
- steps to reproduce, or a proof of concept
- any suggested fix

Do not include real tenant IDs, tokens, customer data or other secrets in your report. Redact them.

## What to expect

- **Acknowledgement** within 5 working days.
- **Assessment** — we confirm whether the report is a vulnerability and how severe it is, and keep you informed.
- **Fix and release** — we aim to publish a fix within 30 days for confirmed issues, sooner for critical ones, and we tell you before the advisory goes public.
- **Credit** — we credit reporters in the advisory and release notes unless you prefer to stay anonymous.

These are good-faith targets from a small team of maintainers, not contractual guarantees.

## In scope

Examples of what we want to hear about:

- **Scripts** (`install.py`, `build_dist.py`, `lean.py`, `validate.py`, CI helpers) that could overwrite or delete files outside their target, run arbitrary commands, or leak data.
- **Skill or agent instructions** that could lead an agent to perform destructive or unsafe actions by default — for example deleting data, widening access or security roles, publishing content, or handling credentials — without an explicit confirmation step.
- **Secrets or private data** committed to a repository, including tenant or workspace identifiers, tokens and real e-mail addresses.
- **CI/CD workflows** with unsafe permissions, injection risks or unpinned third-party actions.
- **Supply-chain issues** in a project's dependencies or release artifacts.

## Out of scope

- Vulnerabilities in third-party products themselves (Power BI, Microsoft Fabric, Claude Code, Codex, Cursor, etc.) — report those to their vendors.
- Incorrect or outdated BI advice that has no security impact — open a regular issue instead.
- Issues that require a malicious maintainer or an already-compromised machine.
- Reports from automated scanners without a demonstrated impact.

## Safe harbor

If you act in good faith — you test only against your own data and environments, avoid harming others, do not access or keep data that is not yours, and give us reasonable time to respond before disclosure — we will not pursue action against you.

## Disclosure

We prefer coordinated disclosure: we publish a GitHub security advisory once a fix is available, and we ask that you wait until then before discussing the issue publicly.

Thank you for helping keep Keemboll and its users safe.
