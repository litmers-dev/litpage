# Contributing to Litpage

Thanks for helping improve Litpage. You can usually expect an initial response within seven days.

## Propose a change

Open an issue before starting a feature or a large change. Describe the problem and agree on scope with the maintainers before implementing a large feature. Bug fixes, typo fixes, and small improvements can go straight to a pull request.

Maintainers close unsolicited large feature PRs, such as platform ports or desktop apps, and encourage their authors to publish the work as a separate community project.

## Develop and test

Use Node.js 26 or later and pnpm 10.x. Install dependencies and check types from the repository root.

```sh
pnpm install --frozen-lockfile
pnpm typecheck
```

The workspace test command includes the E2E smoke test, which expects Google Chrome at its default macOS path.
Start `pnpm dev` in another terminal before running `pnpm test`. To run the smoke test on its own, use `pnpm e2e`.
The CI test job runs the workspace tests with the E2E package excluded.

## Open a pull request

Keep changes focused, link the issue when there is one, and summarize the change and the checks you ran.
Add or update tests when you change behavior, including the relevant E2E script for app behavior changes.
Keep commit messages concise.

Your contributions are distributed under the same [MIT license](LICENSE) as Litpage.

## Track review status

Maintainers use one status label at a time on issues and pull requests:

- `waiting-on-review` when a maintainer needs to review a new item or an author has supplied the requested update.
- `waiting-on-author` when a maintainer has requested information or changes from the author.
- `blocked` when work depends on another issue, PR, or decision. Once it is unblocked, assign the label for whoever acts next.

## Close an out-of-scope proposal

Thank the contributor, explain the scope decision, link to the relevant guidance, and close the proposal. For example:

> Thanks for putting this together. A desktop app is outside the scope the core team can maintain, so we're closing this PR. We'd welcome it as a separate community project. See our [feature contribution guidelines](https://github.com/litmers-dev/litpage/blob/main/CONTRIBUTING.md#propose-a-change).
