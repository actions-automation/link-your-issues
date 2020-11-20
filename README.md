# link-your-issues

A Github Action to test whether contributors properly link issues mentioned in commits in their PR descriptions.

Usage is simple; just include it in a workflow that runs on a pull request event:

```yml
name: link-your-issues

on:
  pull_request:
    types: [opened, reopened, synchronize, edited]

jobs:
  link-your-issues:
    runs-on: ubuntu-latest
    steps:
    - uses: actions-automation/link-your-issues@main
      with:
        repo-token: ${{ secrets.GITHUB_TOKEN }}
```

The `repo-token` input must be a valid Github access token; the `GITHUB_TOKEN` provisioned by Actions should suffice.

See [link-your-issues.yml](.github/workflows/link-your-issues.yml) for an example.
This is a test
