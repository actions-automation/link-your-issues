# link-your-issues

A Github Action to test whether contributors properly link issues mentioned in commits in their PR descriptions.

Usage is simple; just include it in a workflow that runs on a pull request event:

```yml
name: link-your-issues

on:
  pull_request

jobs:
  link-your-issues:
    runs-on: ubuntu-latest
    steps:
    - uses: mbestavros/link-your-issues@master
```
