# Contributing

Thanks for your interest in contributing to this ARGVUS project. This document
outlines the guidelines for reporting issues and submitting changes. Short
version: be clear, be respectful, and keep changes focused and reviewable.

Please also read [DEVELOPMENT.md](DEVELOPMENT.md) for the build workflow.

## Code of Conduct

By participating, you agree to abide by the
[Contributor Covenant v2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).
Instances of unacceptable behavior may be reported to the project maintainers.

## What to contribute

- Bug reports and reproductions (asset issues, rendering problems)
- Asset improvements (logo refinements, new branding elements)
- Documentation improvements (`README.md`, `DEVELOPMENT.md`, this file)
- Packaging fixes (PKGBUILDs, build tooling)
- Anything in the issue tracker labeled `good first issue` or `help wanted`

Please open an issue first for larger changes or anything that alters the assets,
so the approach can be agreed on before work starts.

## Reporting bugs

- Search the issue tracker first to avoid duplicates.
- Use a clear, descriptive title.
- Include, when relevant:
  - Distro / Arch version and architecture (`pacman -Q core/pacman`)
  - How the asset is being used (component, context)
  - `make build` log output
  - The relevant version/tag you are on
- Label the issue with `bug` if you can.

## Development flow

1. Read [DEVELOPMENT.md](DEVELOPMENT.md) and set up your environment.

2. Create a branch from `main`:

   ```sh
   git checkout -b feat/describe-the-change
   ```

   Branch naming: `fix/...`, `feat/...`, `docs/...`, `chore/...`,
   `refactor/...`.

3. Make small, focused commits following
   [Conventional Commits](https://www.conventionalcommits.org/):

   ```text
   feat(assets): add secondary logo variant
   fix(svg): correct aspect ratio in wordmark
   docs: explain asset usage and guidelines
   ```

4. Validate locally before pushing:

   ```sh
   make validate
   make build
   ```

   `ci.yml` runs the same checks (plus `namcap` and cspell) on push/PR.

5. Push and open a pull request against `main`.

### Pull requests

- Reference the issue it fixes: `Closes #123`.
- Keep the diff minimal; do not mix unrelated changes.
- Do not commit build outputs (`build/`) or generated temporary PKGBUILDs.
