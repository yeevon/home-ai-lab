# Decisions

## 2026-10-09 21:05 America/Chicago - Migrate Cline project folders and verify MCP

**Decision:** Moved `.clinerules/` and `memory-bank/` from `C:\src\second-brain` to `C:\src\home-ai-lab`. Preserved all three rule files byte for byte and retained Cline's existing user-level MCP settings.

**Reasoning:** The Cline rules and relative memory-bank paths belong with the home-ai-lab project. Continue is a separate extension. The MCP configuration is user-level and points to a persistent remote service, so no path migration or connection edit was needed.

**Files changed:** Moved `.clinerules/coding.md`, `.clinerules/memory_bank.md`, `.clinerules/search.md`, and the empty `memory-bank/` directory. Added `memory-bank/activeContext.md` and this decision entry as required by the migrated memory-bank rule. Temporary verification scripts and search output are under the gitignored `work/` folder.

**Outcome:** Folder locations and rule-file SHA-256 hashes verified. TCP connectivity to `10.0.0.204:3000`, MCP initialization, discovery of four tools, a search returning three results, and a bounded page read all passed. Brave rate limiting and DuckDuckGo CAPTCHA warnings remain. This tested the configured endpoint with an independent MCP client, not the running Cline UI. No commit, server change or model change was made.
