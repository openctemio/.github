# Contributing to OpenCTEM

This is the default contributing guide for `openctemio` repositories that do not
have their own. A repository's own `CONTRIBUTING.md` wins where it says more.

## Where to open a pull request

| Repository | Base branch | Notes |
|---|---|---|
| `openctem` (platform monorepo) | `develop` | `main` takes only `release/vX.Y.Z` and hotfix branches, opened by the release workflow. A pull request into `main` from any other branch fails the `Workflow Lint` check. |
| every other repository | `main` | `release/vX.Y.Z` branches are opened by the repository's Release Prepare workflow, not by hand. |

Fork the repository (outside contributors) or push a branch (maintainers), then
open the pull request against the base branch above.

## Branch names

`<type>/<short-slug>`, where `<type>` is one of `feat`, `fix`, `docs`, `refactor`,
`test`, `ci`, `build`, `chore`, `perf` or `security`. Example: `fix/scope-gate-ipv6`.
`release/*` and `hotfix/*` are reserved for the release workflows.

## Commits

- [Conventional Commits](https://www.conventionalcommits.org/): `type(scope): summary`.
  A breaking change uses `type!:` or a `BREAKING CHANGE:` footer. Versions are
  proposed from these messages, so they matter.
- Sign off every commit (`git commit -s`). Repositories with a `dco` check
  require it; the others ask for it as well.
- Do not add AI or tool attribution: no `Co-Authored-By` trailer naming a tool or
  assistant, no "Generated with" lines, no links to a tool session. The
  `No AI attribution` check fails on them. You are the author of what you submit.
- Never commit secrets, customer data, internal hostnames or private addresses.
  Push protection blocks known secret formats; the `Secret Scan` check covers the rest.

## Contributor License Agreement

Repositories with a `cla` check accept outside contributions under the
OpenCTEM Contributor License Agreement. When a commit author has not signed,
the check comments on the pull request with the one-line comment to post.
Texts: [Individual CLA](https://docs.openctem.io/legal/cla/) and
[Corporate CLA](https://docs.openctem.io/legal/cla-corporate/).

## Changelog fragments

Where a repository has a `changelog.d/` directory (in `openctem`: `api/changelog.d/`),
a user-visible change adds one file `changelog.d/<short-slug>.md` and never edits
`CHANGELOG.md`. The `changelog` check enforces it; the format is in that
directory's `README.md`.

## Checks and merging

- Every required check must pass, and every review conversation must be resolved.
- Workflows from forks wait for a maintainer to approve the run.
- `openctem` merges through the merge queue. Do not ask for an admin merge.
- A change to a security-sensitive path (listed in `.github/security-paths.yml`)
  gets the `security-sensitive` label and an automated review; the `security-gate`
  check passes only after a maintainer has reviewed it and added `security-ack`.
  Contributors and automation never add that label.
- Release tags (`v*`) are created by the release workflow or a maintainer and
  are never moved or deleted.

## Security issues

Never in a public issue or pull request. See [SECURITY.md](SECURITY.md).
