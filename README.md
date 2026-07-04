# Merge Guardian — Gate Your Merges

Enforce merge requirements: reviews, passing checks, up-to-date branches, linked issues.

## Quick Start

```yaml
- uses: CodeGero/merge-guardian@v1
  with:
    github-token: ${{ secrets.GITHUB_TOKEN }}
    require-reviews: 1
```

## Premium
Custom policies, Slack notifications, merge analytics — https://kryptorious.gumroad.com/l/jbvet

MIT License
