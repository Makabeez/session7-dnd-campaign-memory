# D&D Campaign Memory v2

[![Walrus Session 7](https://img.shields.io/badge/Walrus-Session%207-blue?style=flat-square)](https://thewalrussessions.wal.app/)
[![Prompt Evolution](https://img.shields.io/badge/Track-Prompt%20Evolution-purple?style=flat-square)](https://thewalrussessions.wal.app/)
[![Mainnet](https://img.shields.io/badge/Walrus-Mainnet-orange?style=flat-square)](https://memory.walrus.xyz)
[![Blobs](https://img.shields.io/badge/Mainnet%20Blobs-14-success?style=flat-square)](https://memory.walrus.xyz)

**Improved from the original [Campaign Vault](https://github.com/0xanjalii/Campaign-Vault) (Session 5).**  
A portable continuity engine for long-running D&D / TTRPG campaigns powered by [Walrus Memory](https://walrus.xyz/products/walrus-memory/).

---

## Live Evidence & Links

| Item | Link |
|------|------|
| **Medium article** | [How I stopped my D&D campaign from contradicting itself](https://medium.com/@tonystarks1220/how-i-stopped-my-d-d-campaign-from-contradicting-itself-across-sessions-with-walrus-memory-b966649d4070) |
| **Demo video** | [YouTube](https://youtu.be/Y-4kyyeZXKE) |
| **X post** | [View post](https://x.com/GeiserJoe2) *(add exact status URL)* |
| **GitHub Issue (original repo)** | [Session 7 improvement issue](https://github.com/0xanjalii/Campaign-Vault/issues) *(add exact issue number)* |
| **Namespace** | `session7-dnd-makabeez` |
| **Mainnet blobs** | **14** (verified) |
| **Account ID** | `0xedc0baac5f3ac60e536615d94766e1888c9ff1523d7af8e0693bfe7e937aad59` |
| **Screenshots** | See [`evidence/`](./evidence/) folder |

### Evidence screenshots (committed)

- `evidence/boot-session2.png` — BOOT ritual correctly recalled previous session state
- `evidence/continuity-conflict.png` — Contradiction-guard caught Gorruk appearing in the market
- `evidence/supersede-gorruk.png` — `npc-gorruk-v2` supersedes old record on Walrus
- `evidence/handoff-session1.png` — Session 1 handoff
- `evidence/handoff-session2.png` — Session 2 final handoff (Gorruk dead)
- `evidence/session1-opening.png` — Session 1 opening scene

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

1. Install Walrus Memory (Claude Code / Cursor / Codex / any MCP client).
2. Copy the entire contents of [`dnd-campaign-memory-v2.md`](./dnd-campaign-memory-v2.md) into your system prompt or `CLAUDE.md`.
3. Set the namespace (default used in testing: `session7-dnd-makabeez`) or tell the agent your campaign slug once.
4. Start a session. The agent will boot from memory.

---

## Security

- Never commit `.env`
- Keep your MemWal private key / account ID only in environment variables
- This prompt never stores secrets or real-world personal data

---

## Real test campaign (Shadowfen Road)

- **Session 1**: Party arrives in Shadowfen, meets Mara, establishes Gorruk at the old mill with the Moonstone. Handoff written.
- **Session 2** (fresh chat): BOOT correctly recalled everything. Deliberate contradiction (Gorruk in the market) was blocked. Gorruk killed → superseding record written. Final handoff correctly listed him as dead.

All 14 blobs live on **Walrus Mainnet** under namespace `session7-dnd-makabeez`.

---

**Original prompt author:** [0xanjalii](https://github.com/0xanjalii)  
**This evolution:** [Makabeez](https://github.com/Makabeez) — Walrus Session 7
