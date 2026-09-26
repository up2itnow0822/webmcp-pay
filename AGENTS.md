# webmcp-pay

## Purpose

Reserved X402 payment integration layer for webmcp-sdk and agentwallet-sdk. The repo is planned, not yet implemented. Current durable work is repository hygiene and CI so `main` can stay protected.

## Ownership

Agent Economy, LLC / Bill Wilson (`@up2itnow0822`).

## Local Contracts

- Do not claim the product is implemented; README status is planned.
- Required GitHub status check context for `main` is `build` from `.github/workflows/build.yml`.
- `.github/workflows/ci.yml` job is `ci` so it does not collide with that required context.
- Prefer merge commits; do not force-push shared branches.

## Work Guidance

- Keep `build.yml` toolchain detection honest: fail installs that fail, run Foundry when `foundry.toml` exists, and do not hide `npm ci` lockfile mismatches.
- Small contract or workflow changes belong in the owning workflow file, not a second overlapping `build` job.

## Verification

- `build` workflow on pull requests and on `main` / `master`.
- `CI` workflow (`ci` job) on pull requests and pushes to `main`.

## Child DOX Index

- `.github/workflows/AGENTS.md` — GitHub Actions contracts for required and advisory checks
