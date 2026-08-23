# D&D Campaign Memory v2

[![Walrus Session 7](https://img.shields.io/badge/Walrus-Session%207-blue?style=flat-square)](https://thewalrussessions.wal.app/)
[![Prompt Evolution](https://img.shields.io/badge/Track-Prompt%20Evolution-purple?style=flat-square)](https://thewalrussessions.wal.app/)
[![Mainnet](https://img.shields.io/badge/Walrus-Mainnet-orange?style=flat-square)](https://memory.walrus.xyz)

**Improved from the original [Campaign Vault](https://github.com/0xanjalii/Campaign-Vault) (Session 5).**  
A portable continuity engine for long-running D&D / TTRPG campaigns powered by [Walrus Memory](https://walrus.xyz/products/walrus-memory/).

---

## Live Evidence & Links

- **Medium article:** https://medium.com/@tonystarks1220/how-i-stopped-my-d-d-campaign-from-contradicting-itself-across-sessions-with-walrus-memory-b966649d4070
- **Demo video:** https://youtu.be/Y-4kyyeZXKE
- **X post:** https://x.com/GeiserJoe2/status/ (paste your exact post URL)
- **GitHub Issue on original:** (paste the issue URL)
- **Namespace:** `session7-dnd-makabeez` (Mainnet)
- **Screenshots:** see [`evidence/`](./evidence/) folder

---

## What changed (before → after)

| Area              | Original                          | v2                                              |
|-------------------|-----------------------------------|-------------------------------------------------|
| Namespace         | Single flat dump                  | One namespace + typed current-state nodes        |
| Session start     | Ad-hoc                            | Explicit **BOOT** ritual + continuity summary   |
| Consistency       | None                              | Contradiction-guard before finalizing scenes    |
| State changes     | Append only (stale facts surface) | Append-only **with** `supersedes:`              |
| Session end       | None                              | Clean handoff record                            |
| Tool honesty      | Assumed tools                     | Only official MemWal tools; no invented delete  |
| Safety            | Minimal                           | Explicit write gate + no-secrets rule           |

---

## How to use

1. Install Walrus Memory in Claude Code / Cursor / Codex.
2. Copy the contents of [`dnd-campaign-memory-v2.md`](./dnd-campaign-memory-v2.md) into your system prompt.
3. Use namespace `session7-dnd-makabeez` (or your own).
4. Start a session — the agent will BOOT from memory.

---

**Original author:** [0xanjalii](https://github.com/0xanjalii)  
**This evolution:** [Makabeez](https://github.com/Makabeez) — Session 7
