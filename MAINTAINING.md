# Maintaining Litpage

## Triage and review

Check new issues and pull requests regularly. Aim to give an initial response within seven days.

Assign one review status label at a time. Follow the [contributor review statuses](CONTRIBUTING.md#track-review-status).

- `waiting-on-review` when a maintainer needs to review a new item or an update.
- `waiting-on-author` when the contributor needs to respond or make changes.
- `blocked` when work depends on another issue, pull request, or decision. Once unblocked, switch to the label for whoever acts next.

Ask contributors to open an issue before starting a feature and agree on scope before building a large one. Review pull requests for scope, correctness, and relevant tests. Update the label as responsibility shifts.

## Merge

Make all changes to `main` through pull requests. Branch protection requires one approving review and passing `typecheck` and `test` checks. Once those requirements are met, squash merge by default.

## Closing replies

Close unsolicited large feature PRs and suggest publishing the work as a separate community project. When closing a proposal, adapt the reply to the discussion and post it before closing.

### Unsolicited large feature

```markdown
Thanks for putting this together. Large features need an issue and agreement on scope before implementation. We'd welcome this work as a separate community project. See our [feature contribution guidelines](https://github.com/litmers-dev/litpage/blob/main/CONTRIBUTING.md#propose-a-change). We're closing this PR.
```

### Out of scope

```markdown
Thanks for the proposal. [Explain why this falls outside what the core team can maintain.] See our [feature contribution guidelines](https://github.com/litmers-dev/litpage/blob/main/CONTRIBUTING.md#propose-a-change). We're closing this proposal.
```

### Duplicate or already resolved

```markdown
Thanks for flagging this. [Explain where this is already tracked or how it was resolved.] See [the existing issue or fix](LINK). We're closing this thread.
```

## Stale issues and pull requests

Issues and pull requests are marked stale after 30 days without activity and closed after 14 more days of inactivity. An update clears the stale label and restarts the timer. See the [daily stale workflow](.github/workflows/stale.yml).

## Releases

Litpage has no tags or releases yet. Follow SemVer and increment the major version for breaking changes, the minor version for backward-compatible features, and the patch version for backward-compatible fixes.

1. Check out the reviewed commit from `main` after its required checks pass. Create an annotated tag and push it to GitHub.

   ```sh
   git tag -a vX.Y.Z -m "Release vX.Y.Z"
   git push origin vX.Y.Z
   ```

2. In GitHub Releases, select the tag, write notes covering the main changes and any breaking changes or migration steps, and publish the release manually.

## Security and ownership

Prioritize reports filed through GitHub private vulnerability reporting. Follow [SECURITY.md](SECURITY.md) when handling them.

The current maintainer is [@yeongjun-cigro](https://github.com/yeongjun-cigro), listed in [CODEOWNERS](.github/CODEOWNERS). Update that file when adding a maintainer.
