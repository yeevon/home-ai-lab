# Changelog

This file records completed implementation and repository changes. Planned work belongs in GitHub Projects, not this changelog.

## 2026-10-09

### Server and search baseline

The following completed setup is recorded here on October 9; this is not a claim that every installation step occurred on that date.

- Installed Docker on the Ubuntu XPS server.
- Pulled `searxng/searxng:latest` and `isokoliuk/mcp-searxng:latest` and started their containers.
- Connected the containers through `search-network`, with MCP using `http://searxng:8080` for search.
- Published host ports `8080` for SearXNG and `3000` for MCP so the services could be reached over the LAN.
- Updated Cline's MCP connection from a local Docker process to Streamable HTTP at `http://<Internal-IP>:3000/mcp`.
- Confirmed that the remote MCP search path returned search results.

### Cline project migration

- Moved `.clinerules/` and the previously empty `memory-bank/` from `second-brain` to `home-ai-lab`.
- Verified that all three migrated rule files were unchanged using SHA-256 hashes.
- Retained the existing user-level MCP settings; the remote endpoint did not depend on the project folder.
- Added the active project context and migration decision to the memory bank.

### Connection verification after migration

- Passed TCP connectivity, MCP initialization and discovery of four tools using an independent MCP client with Cline's configured endpoint.
- Received three results from `searxng_web_search` and page content from `web_url_read`.
- Recorded the responding MCP server as `ihor-sokoliuk/mcp-searxng` version `2.5.1`.
- Observed continuing upstream warnings: Brave rate limiting and DuckDuckGo CAPTCHA. Search still returned results. The running Cline UI was not exercised during this check.

### Repository documentation

- Added this changelog to record completed work.
- Updated the README to describe the implemented search setup, current verification results, actual repository layout and epic-level status.
- Removed claims that autocomplete hosting, audit logging, benchmark infrastructure and security hardening were already established, along with links to nonexistent implementation files.

### Documentation privacy

- Replaced internal IP addresses and machine-specific paths in shared documentation and the memory bank with placeholders or project-relative references.
- Added a Cline privacy rule for shared documentation and examples.
- Checked committable files for common address, path and credential patterns; confirmed that local reference PDFs, generated outputs and working files remain gitignored.
