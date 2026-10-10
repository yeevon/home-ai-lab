# Privacy in shared files

- Use `<Internal-IP>` instead of real private server addresses in README content, changelogs, memory-bank notes, diagrams and configuration examples.
- Use `%USERPROFILE%`, other appropriate environment variables, or project-relative paths instead of personal usernames and absolute local filesystem paths.
- Never copy passwords, tokens, API keys, private keys, SSH public-key payloads or credentials embedded in URLs into shared files.
- Read real endpoints from local runtime settings when needed. Do not replace working connection values with documentation placeholders.
- Check tracked and newly added files for sensitive details before proposing a commit. Report matches by location and category without echoing secret values.
- Keep ignored local references, generated artifacts, test outputs and working files private; review and sanitize them separately before sharing.
- If private details already exist in Git history, report that separately. Do not rewrite history or force-push without explicit authorization.
