# GitHub Action: Run ktlint

This `GitHub Action` runs the lastest version of [ktlint](https://ktlint.github.io/) on pull requests to enforce best practices.

Based on [ScaCap implementation](https://github.com/ScaCap/action-ktlint).

## Example usage

```yml
name: Project
on: [pull_request]
jobs:
  ktlint:
    name: Check Code Quality
    runs-on: ubuntu-latest

    steps:
      - name: Clone PR
        uses: actions/checkout@v2
        with:
          fetch-depth: 1
      - name: Run Ktlint
        uses: lucasnlm/ktlint-action@master
```
