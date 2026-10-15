---
trigger: glob
globs: "README*,docs/**,CHANGELOG*"
description: "Every claim in a doc must be checked against the code, commands and files in the repository."
---

# Docs accuracy

Documentation must match the repository.

- Before writing a command, find where it is defined (a script, a Makefile target, a package manifest) and copy it exactly.
- Before naming a file, flag, option, env var or function, search for it. If it does not exist, do not write it.
- Take versions, supported platforms and requirements from config files such as lockfiles, manifests and CI definitions.
- Check that every relative link and anchor resolves to something that exists.
- When code changes in the same task, update the docs that describe it in the same change.
- If you cannot verify a statement, mark it `TODO: verify` and tell the user; do not present it as fact.
- Remove documentation for features that no longer exist rather than leaving it stale.
