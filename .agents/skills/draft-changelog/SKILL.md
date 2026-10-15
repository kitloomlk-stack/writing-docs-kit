---
name: draft-changelog
description: "Build a changelog entry or release notes from the commits since the last tag."
disable-model-invocation: true
---

# draft-changelog

When invoked, produce a changelog entry or release notes for the changes since the last release.

1. Ask the user for the range if it is not given (for example the last tag to HEAD). If the repository has tags, suggest the most recent one.
2. Read the existing CHANGELOG file, if any, and match its format. Otherwise use Keep a Changelog headings: Added, Changed, Deprecated, Removed, Fixed, Security.
3. Read the commit log and merged PR titles for the range using read-only git commands. Group related commits; drop merge noise, version bumps and purely internal refactors.
4. Write each entry for a user of the project: what changed for them and, where relevant, what they must do. Link to the PR or issue only if the number appears in the commit data.
5. Flag breaking changes at the top of the entry.
6. Put the draft in the changelog file under an "Unreleased" heading or in your reply, as the user prefers. Do not create tags, commit, or push.
7. List any commits you could not classify so the user can decide.
