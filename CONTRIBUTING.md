# Contributing to Myntlo

This guide applies to every Myntlo repository that does not have its own `CONTRIBUTING.md`.
Repository-specific setup, build and test commands live in each repository's README.

## Workflow

Nobody pushes directly to `main`.
Every change goes through a pull request.

1. Create a branch in the repository itself (no forks) from the latest `main`.
2. Make your change, with tests or manual verification steps.
3. Open a pull request against `main` and fill in the template.
4. Get CI green and at least one approving review.
5. Squash and merge, then delete the branch.

If a change touches architecture, a public API or customer data, open an issue to discuss it before you start.

## Branch names

Use a prefix that says what kind of change it is, followed by a short kebab-case description:

| Prefix | Use for |
|---|---|
| `feat/` | new features |
| `fix/` | bug fixes |
| `chore/` | dependencies, tooling, config |
| `docs/` | documentation only |
| `refactor/` | code changes that do not change behavior |
| `test/` | adding or fixing tests |

Example: `fix/transcript-upload-timeout`.

## Commits

- Write a short subject in the imperative mood, for example `add retry to transcript upload`.
- Keep each commit focused on one thing.
- Pull requests are squash merged, so the pull request title becomes the commit on `main`.
  Make the title read like a good commit subject.

## Pull requests

- Keep them small and focused: one feature or fix per pull request.
- Link the related issue if there is one (`Closes #123`).
- Describe the user-facing impact and how you verified the change.
- Do not merge with failing checks.
  If a test is flaky, fix it or open an issue for it rather than re-running until it passes.
- Reviewers look for correctness, tests, security and maintainability, not just style.

## Secrets

- Never put API keys, passwords, tokens or other secrets in code, config files, commit messages or pull request descriptions.
- Use environment variables, and keep `.env` files out of git.
- If you commit a secret by accident, follow [SECURITY.md](SECURITY.md).

## Security issues

Do not report security problems in issues or pull requests.
See [SECURITY.md](SECURITY.md).
