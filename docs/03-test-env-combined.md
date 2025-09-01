# 🔗 Combined Test & Environment Framework (Goblin)

This shows which **tests** belong in which **environment**, so Goblin moves safely from idea → live.

---

## 🌱 Sandbox
- SAST
- Ad-hoc Unit Testing
- Prototyping  
✅ Gate: code runs, rough validation

---

## 💻 Development
- Unit Tests
- Component Tests
- Code Reviews
- Smoke Tests  
✅ Gate: stable enough to move to QA

---

## 🔍 Test
- Regression Testing
- Integration Testing
- End-to-End
- Exploratory
- Sanity Checks  
✅ Gate: workflows validated, ready for blockchain testing

---

## 🔗 Devnet (Solana)
- Contract deployment
- Wallet flows
- Solana API integration
- Early security scans (DAST)  
✅ Gate: contracts behave correctly on dev cluster

---

## 🌐 Testnet (Solana)
- Performance & load
- Chaos & resilience
- Compatibility
- Accessibility
- Security scanning & pen testing
- Data migration (if relevant)  
✅ Gate: production-like rehearsal passed

---

## 🚀 Production
- UAT
- Alpha/Beta
- OAT
- DR drills
- Canary release
- Monitoring & observability
- Continuous pen testing
- Periodic audits  
✅ Gate: stable, secure, monitored production

---

## 🗺️ Visual Flow

Sandbox → Development → Test → Devnet → Testnet → Production

