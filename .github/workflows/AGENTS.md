# GitHub Actions

## Purpose

CI for this planned repo: a required `build` check plus a lightweight `CI` workflow.

## Ownership

Inherited from repo root. Workflow files here are the only automation that gates `main`.

## Local Contracts

- Job `build` in `build.yml` is the unique required status-check context (`build`).
- Job `ci` in `ci.yml` must not be named `build`.
- Foundry detection in `build.yml` runs before the Node branch so `foundry.toml` without `package.json` still builds.
- When `package-lock.json` exists, `npm ci` must fail closed.
- Python dependency installs must fail the job; do not swallow pip errors with `|| true`.

## Work Guidance

- Change the ruleset required context only together with a job rename that keeps exactly one `build` check.
- Do not add a second job named `build` in any workflow.

## Verification

- Pull request and `main`/`master` runs of `build`.
- Pull request and `main` runs of `CI`.

## Child DOX Index

None.
