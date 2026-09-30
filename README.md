---
__cgxx: |
  # vim:set expandtab shiftwidth=2 filetype=markdown foldlevel=3:
  # SPDX-License-Identifier: GPL-3.0-only

  #
  #
  # ~chewygumxx/learn-node.git
  # ::: :/README.md
  #
  #

ctime: 2026-09-30
title: "learn-node"
description: "My Node and NPM learning playground"
tags:
  - node
  - npm
  - learn
  - hello-world
---

# learn-node

My Node and NPM learning playground

## CI

`.github/workflows/ci.yaml` calls the shared
[standard workflow](https://github.com/chewygumxx/.github#standard-workflow):
commitlint, the header sync, generic lint and format checks for workflows,
shell and zsh scripts, TOML, YAML and `.editorconfig`, and the metadata sync.
This repository's own `npm run check` follows, against the commit the header
sync pushed.

## Development

- `npm run commit` composes a commit interactively.
- `npm run check` runs the typecheck, format check, lint, Markdown lint and YAML
  checks (prettier, then yamllint with `@chewygumxx/yamllint-config`) that CI
  runs.
- `npm run format` applies Biome formatting, and prettier's to YAML, which Biome
  does not read.

The pre-commit hook runs the same checks on staged files, and rejects em dashes.
The commit-msg hook runs commitlint.
