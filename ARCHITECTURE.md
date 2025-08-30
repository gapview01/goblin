# Architecture (4 Buckets)

Goblin is organised into four conceptual buckets. Buckets are **meta categories**; the real units are the repos they group.

1) **User, Developer & Agentic Experiences**
   Wallet (web/mobile), Developer Console, first bot (tranched staking), agentic UX.

2) **On-Chain Core (Solana)**
   Anchor programs: Bot Factory, Master, Individual Bot; token configs; treasuries.

3) **Off-Chain Smarts (platform-agnostic)**
   API, Indexer, Timekeeper; SDK + CLI; CI/CD and observability. Cloud-agnostic.

4) **Governance & Economics**
   Treasury policy, upgrade/pause rules, tokenomics, future DAO.

**Now vs Future**
- Now: wallet, dev console, programs, services (API/indexer/timekeeper), SDK/CLI, first bot.
- Future: more bots (added as separate repos), Swap, Stake UX, DAO.

Principle: **Open where it builds trust. Private where it protects money.**
