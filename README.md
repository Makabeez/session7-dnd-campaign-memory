# D&D Campaign Memory v2

[![Walrus Session 7](https://img.shields.io/badge/Walrus-Session%207-blue?style=flat-square)](https://thewalrussessions.wal.app/)
[![Prompt Evolution](https://img.shields.io/badge/Track-Prompt%20Evolution-purple?style=flat-square)](https://thewalrussessions.wal.app/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Mainnet](https://img.shields.io/badge/Walrus-Mainnet-orange?style=flat-square)](https://memory.walrus.xyz)

**Improved from the original [Campaign Vault](https://github.com/0xanjalii/Campaign-Vault) (Session 5 winner).**  
A portable continuity engine for long-running D&D / TTRPG campaigns powered by [Walrus Memory](https://walrus.xyz/products/walrus-memory/).

---

## Why this exists

Long-running campaigns collapse under their own lore.  
NPCs come back from the dead. Quests reopen. The DM spends more time fighting context loss than running the game.

The original prompt was a solid start but lacked structure, contradiction protection, and a reliable session boot.  
**v2 turns a passive log into an active continuity engine.**

---

## What changed (before → after)

| Area              | Original                          | v2                                              |
|-------------------|-----------------------------------|-------------------------------------------------|
| Namespace         | Single flat dump                  | One namespace + typed current-state nodes        |
| Session start     | Ad-hoc                            | Explicit **BOOT** ritual + continuity summary   |
| Consistency       | None                              | Contradiction-guard before finalizing scenes    |
| State changes     | Append only (stale facts surface) | Append-only **with** `supersedes:` so current truth wins |
| Session end       | None                              | Clean handoff record                            |
| Tool honesty      | Assumed tools                     | Only official MemWal tools; no invented delete  |
| Safety            | Minimal                           | Explicit write gate + no-secrets rule           |

---

## How it works
Session start
↓
BOOT (recall active quests + key NPCs + latest handoff)
↓
Continuity summary → DM confirms
↓
Play / write scene
↓
Contradiction-guard (stop if canon is violated)
↓
Write gate → remember (or supersede)
↓
Session end → handoff record
text---

## Quick start

1. Install Walrus Memory in Claude Code / Cursor / Codex / any MCP client.
2. Copy the entire contents of [`dnd-campaign-memory-v2.md`](./dnd-campaign-memory-v2.md) into your system prompt or `CLAUDE.md`.
3. Set the namespace (default: `session7-dnd-makabeez`) or tell the agent your campaign slug once.
4. Start a session. The agent will boot from memory.

---

## Security

- Never commit `.env`
- Keep your MemWal private key / account ID only in environment variables
- This prompt never stores secrets or real-world personal data

---

## Evidence & submission notes

- All memories written under the dedicated namespace for this Session 7 entry
- Before/after comparison and Mainnet blob proof will be linked in the Medium article and GitHub Issue on the original repo

**Original prompt author:** [0xanjalii](https://github.com/0xanjalii)  
**This evolution:** [Makabeez](https://github.com/Makabeez) — Session 7
