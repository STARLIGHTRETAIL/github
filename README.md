# github

This repository is the **GitHub Organization Management** repository for [STARLIGHTRETAIL](https://github.com/STARLIGHTRETAIL).

It contains automation, governance workflows, and the source content used to manage the organization's GitHub presence.

## Contents

| Path | Purpose |
|------|---------|
| `.github/workflows/harden-repos.yml` | Workflow to convert public repositories to private and maintain the public org profile repo (`STARLIGHTRETAIL/.github`) |
| `profile/README.md` | Sanitized public-facing content deployed to `STARLIGHTRETAIL/.github/profile/README.md` |

## Running the Hardening Workflow

The `Harden Repository Visibility` workflow converts all public code repositories to private and ensures the `STARLIGHTRETAIL/.github` repository exists with the correct profile content.

**Prerequisites:** an `ORG_ADMIN_PAT` organization secret containing a GitHub Personal Access Token with `admin:org` and `repo` scopes.

To trigger it:
1. Go to **Actions → Harden Repository Visibility** in this repository.
2. Click **Run workflow**.
3. Set `dry_run` to `false` to apply changes (defaults to `true` for safety).

## Security Governance

All public repositories in the STARLIGHTRETAIL organization, except `STARLIGHTRETAIL/.github`, should remain private. The `STARLIGHTRETAIL/.github` repository hosts only sanitized public-facing content in `profile/README.md`.