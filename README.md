# Mini signage: an SDLC governance practice project

A small digital-signage system (API, web dashboard and screen player) built to practise software delivery governance. I ran it as Scrum Master and Product Owner. The code is kept small on purpose; the subject is the delivery process around it.

## Who did what

I am a Scrum Master with an electro-mechanical engineering background, not a developer. I set up the repository, branch protection, CI and the Jira integration myself, guided step by step by an AI coach (Claude), which also drafted most of the application code. I wrote the stories and acceptance criteria, made the product and process decisions, ran every command and reviewed every change before merge.

## Where to look

- [`signage/`](signage/): the application, with its own README covering how to run it, the API contract and the architecture.
- Pull requests [#8](https://github.com/dmoschochoritis/task-tracker/pull/8) to [#12](https://github.com/dmoschochoritis/task-tracker/pull/12): one Jira story per pull request, squash-merged with a Conventional Commits title.
- [PR #11](https://github.com/dmoschochoritis/task-tracker/pull/11) and [PR #12](https://github.com/dmoschochoritis/task-tracker/pull/12): an API contract change that broke a consumer while CI stayed green, and the follow-up that put the second consumer inside the CI gate.
- [Release v1.0.0](https://github.com/dmoschochoritis/task-tracker/releases/tag/v1.0.0): release notes for the MVP (SCRUM-9, 10, 11, 33 and 12).
- [`.github/workflows/`](.github/workflows/): the two required checks, commit message lint and pytest.
- [`docs/CONTRIBUTING.md`](docs/CONTRIBUTING.md): branch and commit rules.

## How a change reaches main

1. A story in Jira (project SCRUM) with acceptance criteria.
2. A branch named `feature/`, `fix/` or `chore/` plus the Jira key.
3. A pull request into `main`. Branch protection requires both checks to pass, with no bypass.
4. A squash merge, so each story lands on `main` as one commit.

## About the early history

The first commits, before PR #6, predate the commit-lint gate and do not follow the convention. They are left unchanged on purpose, as a record of the state before the gate.

## Next

Delivery metrics measured from this repository's own pull requests, CI runs and Jira history.
