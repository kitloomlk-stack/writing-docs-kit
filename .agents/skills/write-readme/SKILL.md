---
name: write-readme
description: "Draft or rewrite the project README from what the repository actually contains."
disable-model-invocation: true
---

# write-readme

When invoked, draft or rewrite the project README from what the repository actually contains.

1. Inspect the repository: top-level files, the package or project manifest, scripts, entry points, existing docs, CI config and the licence file. Read any existing README in full.
2. Identify the audience and the one thing a new reader should be able to do after reading. If either is unclear, ask a single short question.
3. Propose an outline (one line per section) and wait for the user's go-ahead if the README is more than a small edit.
4. Write the README with: a one-sentence description, who it is for, quick start, basic usage, configuration, development setup, contributing pointer, and licence. Drop sections that have no real content.
5. Use only commands that exist in the repository scripts or manifests. Do not run installs or builds; describe them. Mark anything unverifiable as `TODO: verify`.
6. Apply the prose rules from AGENTS.md. Use the `humanizer` skill if the draft reads machine-written.
7. Finish with a summary: what you changed, the sources you used for each command, and open TODOs.
