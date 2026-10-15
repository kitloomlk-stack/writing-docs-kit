---
description: "Edit a file or selection to remove AI-sounding prose without changing its meaning."
---

# de-slop

When invoked, edit the file or selection the user names so it stops reading as AI-generated, without changing its meaning.

1. Read the target text in full. If no target was given, ask which file or passage to edit.
2. Mark the patterns: filler openers and closers, "not just X but Y" contrasts, forced triads, stacked hedges, em-dash chains, inflated vocabulary, repeated sentence rhythm, and vague claims with no specifics.
3. Rewrite in place with the smallest edits that fix each pattern. Keep every fact, number, code block, link and heading as it was. Do not add new claims.
4. Keep the author's voice and the file's formatting conventions.
5. Use the `humanizer` skill for the rewrite pass when it is available.
6. Report the edits as a short list of before and after examples (at most five), plus anything you left alone because changing it could alter the meaning.
