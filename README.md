# D&D Campaign Memory v2

**Walrus Session 7 — Prompt Evolution**  
Improved from the original [Campaign Vault](https://github.com/0xanjalii/Campaign-Vault) (Session 5 winner).

## Why this exists
Long-running TTRPG campaigns collapse under their own lore. NPCs come back from the dead, quests reopen, and the DM spends more time fighting context loss than running the game. The original prompt was a good start but lacked structure, contradiction protection, and a reliable session boot.

## What changed (before → after)

| Area | Original | v2 |
|------|----------|----|
| Namespace | Single flat dump | One namespace + typed current-state nodes |
| Session start | Ad-hoc | Explicit BOOT ritual + continuity summary |
| Consistency | None | Contradiction-guard before finalizing scenes |
| State changes | Append only (stale facts keep surfacing) | Append-only **with** `supersedes:` so current truth wins |
| Session end | None | Clean handoff record |
| Tool honesty | Assumed tools | Only official MemWal tools listed; no invented delete |
| Safety | Minimal | Explicit write gate + no secrets rule |

## How to use
1. Install Walrus Memory (Claude Code / Cursor / Codex / any MCP client).
2. Copy the entire contents of `dnd-campaign-memory-v2.md` into your system prompt or `CLAUDE.md`.
3. Set the namespace (default in prompt: `session7-dnd-makabeez`) or tell the agent your campaign slug once.
4. Start a session. The agent will boot from memory.

## Security
- Never commit `.env`
- Keep your MemWal private key / account ID only in environment variables
- This prompt never stores secrets or real-world personal data

## Evidence & submission notes
- All memories written under the dedicated namespace for this Session 7 entry
- Before/after comparison and Mainnet blob proof will be linked in the Medium article and GitHub Issue on the original repo

Original prompt author: 0xanjalii  
This evolution: Makabeez — Session 7
