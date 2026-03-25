---
name: changelog
description: Generate a changelog entry from recent commits
disable-model-invocation: true
---

Run `git log --oneline` to get recent commits, then generate a changelog entry.

Format the output as a `## [version] - date` section with grouped entries:

```
## [x.y.z] - YYYY-MM-DD

### Added
- ...

### Changed
- ...

### Fixed
- ...
```

Rules:
- Only include sections that have relevant commits
- Use plain language — rewrite git messages into user-facing descriptions
- Skip merge commits and chore/internal changes unless significant
- Ask the user for the version number if it isn't clear from context

Output only the changelog section, no explanation.
