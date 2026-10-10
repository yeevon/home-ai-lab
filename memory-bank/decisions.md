# Decisions

## 2026-10-09 21:16 America/Chicago - Document implemented baseline and epic status

**Decision:** Added `CHANGELOG.md` containing only completed setup, migration, verification and documentation changes. Reworked `README.md` around the implemented Docker/SearXNG/MCP connection, current test results, real repository layout and epic-level status.

**Reasoning:** The previous README presented unimplemented components and unverified security controls as established. The user clarified that the changelog must track implemented work, the README should remain at epic level, and planned work should be tracked through GitHub Projects.

**Files changed:** `README.md`, `CHANGELOG.md`, `memory-bank/activeContext.md`, `memory-bank/decisions.md`.

**Outcome:** Documentation reflects the user-confirmed server baseline and the successful connection checks already performed. No new deployment, configuration change, GitHub Project or issue was created. Historical setup steps are distinguished from the date they were entered in the changelog.

## 2026-10-09 21:05 America/Chicago - Migrate Cline project folders and verify MCP

**Decision:** Moved `.clinerules/` and `memory-bank/` from `second-brain` to `home-ai-lab`. Preserved all three rule files byte for byte and retained Cline's existing user-level MCP settings.

**Reasoning:** The Cline rules and relative memory-bank paths belong with the home-ai-lab project. Continue is a separate extension. The MCP configuration is user-level and points to a persistent remote service, so no path migration or connection edit was needed.

**Files changed:** Moved `.clinerules/coding.md`, `.clinerules/memory_bank.md`, `.clinerules/search.md`, and the empty `memory-bank/` directory. Added `memory-bank/activeContext.md` and this decision entry as required by the migrated memory-bank rule. Temporary verification scripts and search output are under the gitignored `work/` folder.

**Outcome:** Folder locations and rule-file SHA-256 hashes verified. TCP connectivity to `<Internal-IP>:3000`, MCP initialization, discovery of four tools, a search returning three results, and a bounded page read all passed. Brave rate limiting and DuckDuckGo CAPTCHA warnings remain. This tested the configured endpoint with an independent MCP client, not the running Cline UI. No commit, server change or model change was made.

## 2026-10-09 21:22 America/Chicago - Sanitize shared repository documentation

**Decision:** Replaced private server addresses with `<Internal-IP>` and personal or absolute workspace paths with environment-based or project-relative references. Added `.clinerules/privacy.md` to prevent recurrence.

**Reasoning:** The user requested that internal addresses and other potentially sensitive details stay out of shared documentation. Actual endpoint settings remain local and operational.

**Files changed:** `README.md`, `CHANGELOG.md`, `memory-bank/activeContext.md`, `memory-bank/decisions.md`, `.clinerules/privacy.md`.

**Outcome:** Sanitized current shared files and recorded the privacy preference. An earlier Git commit still contains original address and path details; no history rewrite was performed. Existing exclusions protect local PDFs, outputs and working files from normal staging.
