# Contributing

## Branches

Name each branch `feature/`, `fix/` or `chore/` followed by the Jira key, for example `feature/SCRUM-12`.

## Commit messages and pull request titles

Use Conventional Commits: `type(scope): description`. The scope is optional.

Allowed types: `feat`, `fix`, `docs`, `chore`, `refactor`, `test`.

The `check-commit-message` workflow checks the latest commit of every pull request against this format.

Pull requests are squash-merged, so the pull request title becomes the commit on `main` and must follow the same format.

## Pull requests

All changes reach `main` through a pull request. Two checks must pass before merge: `check-commit-message` and `pytest`.
