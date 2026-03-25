---
name: commit-message
description: Generate a conventional commit message from staged changes
disable-model-invocation: true
---

Run `git diff --staged` to see what's staged. If nothing is staged, run `git diff HEAD` instead.

Write a commit message following the Conventional Commits format:

```
<type>(<scope>): <short summary>

<optional body>
```

Rules:
- **type**: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, or `perf`
- **scope**: the affected area (e.g. `auth`, `api`, `ui`) — omit if unclear or too broad
- **summary**: imperative mood, lowercase, no period, under 72 characters
- **body**: include only if the *why* isn't obvious from the summary; wrap at 72 characters

Output only the commit message, no explanation.
