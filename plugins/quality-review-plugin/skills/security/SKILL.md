---
name: security
description: Review selected code for security vulnerabilities
disable-model-invocation: true
---

Review the selected code or current file for security vulnerabilities.

Focus on:
- Injection risks (SQL, command, XSS, etc.)
- Insecure handling of secrets, tokens, or credentials
- Authentication and authorization flaws
- Unsafe deserialization or input validation
- Dependency or supply chain concerns

For each issue found, state the vulnerability, the risk, and a concrete fix.
If no issues are found, say so explicitly.
