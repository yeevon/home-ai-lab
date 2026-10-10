# Active context

Updated: 2026-10-09 21:22 America/Chicago.

## Current task state

- Added `CHANGELOG.md` for completed work and corrected `README.md` to reflect the implemented Docker, SearXNG and remote MCP baseline.
- README scope is an epic-level overview and actual setup status. Planned work and task-level tracking belong in GitHub Projects; do not add planned tasks to the changelog. No GitHub Project or issues were created in this documentation task.
- Migrated `.clinerules/` and the previously empty `memory-bank/` from `second-brain` into `home-ai-lab` at the user's request.
- The three migrated rule files (`coding.md`, `memory_bank.md`, `search.md`) are unchanged; SHA-256 hashes matched before and after the move.
- Continue's `.continue/` configuration and other second-brain project files remain in the original project.
- No commit or deployment was performed. Wait for the user's next task before implementing the proposed research architecture.

## Cline MCP connection

- Active user-level settings: `%USERPROFILE%\.cline\data\settings\cline_mcp_settings.json`.
- Enabled server: `searxng`; transport: `streamableHttp`; endpoint: `http://<Internal-IP>:3000/mcp`.
- Settings were not changed because the endpoint has no dependency on either project path.
- Verified after migration using an independent MCP client configured from that file: initialization, tool discovery, a three-result `searxng_web_search` call, and `web_url_read` all succeeded.
- Server identified itself as `ihor-sokoliuk/mcp-searxng` version `2.5.1`.
- Available tools: `searxng_web_search`, `searxng_search_suggestions`, `searxng_instance_info`, `web_url_read`.
- Remaining upstream warnings: Brave `too many requests`; DuckDuckGo `CAPTCHA`. Search results were still returned.
- The running Cline UI itself was not exercised. Open `home-ai-lab` as the Cline workspace to use the migrated project rules.

## User scope preference

When asked to read material for context, read and wait. Do not create documents or implement proposals without an action request. The current migration and connection check were explicitly requested.

The user explicitly requested a completed-work changelog and accurate README. Keep the README at epic level and use GitHub Projects for planned work; do not invent a detailed backlog in either document.

## Documentation privacy

- Use `<Internal-IP>` for private server addresses and `%USERPROFILE%` or relative paths for local locations in shared files. Read real connection details from the local Cline settings when needed; do not copy them into the repository.
- Do not publish credentials, key material or personal filesystem details in documentation, examples, changelog entries or memory-bank notes.
- Runtime MCP settings were not changed during documentation sanitization.
- Existing Git history includes an earlier commit containing private addresses and paths. History was not rewritten. Ignored local reference PDFs, outputs and working files may still contain machine-specific details and should not be published as-is.
