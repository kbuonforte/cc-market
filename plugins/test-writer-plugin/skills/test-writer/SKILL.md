---
name: test-writer
description: Generate unit tests for selected code
disable-model-invocation: true
---

Generate unit tests for the selected code or the file I'm currently editing.

- Cover happy paths, edge cases, and error conditions
- Use the testing framework already present in the project (or suggest one if none exists)
- Keep tests focused and independent — one assertion per test where practical
- Add a brief comment for any non-obvious test scenario

Be concise. Output only the test code, no explanations unless something is ambiguous.
