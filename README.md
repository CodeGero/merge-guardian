# Merge Guardian

Enforce merge requirements on pull requests via the GitHub API.

## What it does
Checks that a PR has the required number of approving reviews, required status checks passing, an up-to-date branch, a linked issue in the body, and is not a WIP/Draft — and blocks merge when any requirement is unmet.

> Requires `permissions: pull-requests: read` (and `contents: read`) on the job.

## Usage
```yaml
- uses: CodeGero/merge-guardian@v1
  with:
    github-token: ${{ secrets.GITHUB_TOKEN }}
    require-reviews: '1'
    require-checks: 'true'
    require-up-to-date: 'true'
    require-linked-issue: 'true'
    block-wip: 'true'
```

## Inputs
| Input | Required | Default | Description |
|---|---|---|---|
| `github-token` | yes | — | Token with `pull-requests: read` permission. |
| `require-reviews` | no | `1` | Minimum approving reviews. |
| `require-checks` | no | `true` | Require status checks to pass. |
| `require-up-to-date` | no | `true` | Require branch to be up to date with base. |
| `require-linked-issue` | no | `true` | Require a linked issue in the PR body. |
| `block-wip` | no | `true` | Block PRs titled WIP/Draft. |

## License
MIT — free to use. Premium support via [Gumroad](https://kryptorious.gumroad.com/l/jbvet).
