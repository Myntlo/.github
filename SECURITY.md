# Security policy

This policy applies to every Myntlo repository that does not have its own `SECURITY.md`.

## Reporting a vulnerability

Do not open a public issue, pull request or discussion for a security problem, even in a private repository.

- **Myntlo team members:** send a private message to [@JustinK33](https://github.com/JustinK33).
- **Everyone else:** email [support@myntlo.com](mailto:support@myntlo.com) with "Security" in the subject line.

Please include:

- what you found and which repository, file or URL it affects;
- steps to reproduce or a proof of concept;
- the impact you think it has.

We will acknowledge your report within two business days and keep you updated until it is resolved.
Please give us a reasonable chance to fix the issue before sharing it with anyone else.

## Leaked secrets

If you find an API key, password, token or other secret committed to a repository, treat it as leaked.
Report it right away, rotate it, and only then remove it from the git history.
Removing it from history alone is not enough, because clones and caches may still have it.
