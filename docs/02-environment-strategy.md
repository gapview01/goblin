# 🏗️ Environment Strategy (Goblin)

A structured environment strategy ensures smooth promotion of code and controlled risk.

---

## 🌱 1. Sandbox
- Purpose: Experiments & pilots (not on main branch)
- Tests: Ad-hoc, prototypes
- Users: Developers
- Risks: Unstable, insecure

---

## 💻 2. Development
- Purpose: Active development on `main`
- Tests: Unit, component, smoke
- Users: Engineering team
- Risks: Can break often, optimized for speed

---

## 🔍 3. Test
- Purpose: QA validation
- Tests: Regression, integration, end-to-end, exploratory
- Users: QA & automation
- Risks: Should mirror production for meaningful results

---

## 🔗 4. Devnet (Solana)
- Purpose: Blockchain-linked testing on Solana Devnet
- Tests: Contract deployment, wallet flows, Solana APIs
- Notes: Safe, resettable

---

## 🌐 5. Testnet (Solana)
- Purpose: High-fidelity rehearsal
- Tests: Performance, chaos, compatibility, security
- Notes: Closer to mainnet conditions

---

## 🚀 6. Production
- Purpose: Live system
- Tests: UAT, OAT, DR, canary, monitoring
- Users: Real users
- Notes: Strict controls + rollback

---

## 📌 Promotion Flow
`Sandbox → Development → Test → (Devnet/Testnet as required) → Production`
