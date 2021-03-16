# Github Action: Rubocop

- [Github Action: Rubocop](#github-action-rubocop)
  - [How it works](#how-it-works)
  - [Instructions](#instructions)

Lint your Ruby code in parallel to your builds.


## How it works

- Ruby 2.6.3
- Rubocop + Rubocop Performance


![](screenshots/annotations.png)


## Instructions

In order to use this action you will need to specify the `$GITHUB_TOKEN` alongside the check:


```yaml
# Worflow example
name: CI
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    - uses: actions/checkout@v1

    - name: Rubocop checks
        uses: dockwa/github-actions-rubocop@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

