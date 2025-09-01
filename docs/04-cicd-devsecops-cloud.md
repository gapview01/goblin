# 🤖 Goblin CI/CD + DevSecOps + Cloud Hosting Framework

This framework explains how Goblin’s tests, environments, and cloud hosting all connect into one automated lifecycle.  
The goal is **speed + safety**: changes move from idea → production with minimal human effort, but with strong gates, monitoring, and security.

---

## 🔄 Lifecycle Loop (always repeating)

**Plan → Analyse → Design → Build → Integrate → Test → Deploy → Monitor → Manage → Learn → Adapt**

- **Plan/Analyse/Design:** Ideas and requirements are logged in GitHub (issues/PRs).  
- **Build/Integrate:** Developers push code → GitHub Actions builds and integrates automatically.  
- **Test:** Tests run in sequence, mapped to environments.  
- **Deploy:** Code is promoted into Google Cloud environments with approvals at critical gates.  
- **Monitor/Manage:** Cloud + GitHub tools watch performance, errors, costs, security.  
- **Learn/Adapt:** Incidents feed back into improved tests and playbooks.  

---

## 🏗️ Environments + Cloud Hosting

Each Goblin environment has a matching **GCP project**:

- **Sandbox** → quick experiments (no cloud hosting guarantees).  
- **Development** → deployed to **Cloud Run (Dev)** for rapid smoke + unit tests.  
- **Test** → full QA on **Cloud Run (Test)** + Cloud SQL/Firestore.  
- **Devnet (Solana)** → contracts tested against Solana Devnet, API backend in **Cloud Run (Devnet)**.  
- **Testnet (Solana)** → blockchain rehearsals, load & chaos tests on **Cloud Run (Testnet)**.  
- **Production** → live services on **Cloud Run (Prod)**, behind a global load balancer with monitoring, backups, and disaster recovery.  

---

## 🚛 CI/CD Assembly Line (GitHub Actions)

Every code change runs through **automated workflows**:

1. **Pull Request → CI**  
   - Static scans, unit tests, build check.  
   - Optional preview environment (temporary Cloud Run service).  

2. **Push to `main` → Development**  
   - Auto-deploy to GCP Dev environment.  
   - Run smoke tests.  

3. **Promotion → Test**  
   - Full regression, integration, end-to-end, exploratory.  
   - Must pass before moving to blockchain-linked tests.  

4. **Release Branch → Devnet → Testnet**  
   - Solana program deploys + API deploys.  
   - Performance, chaos, security rehearsals.  

5. **Tag Release → Production**  
   - Canary (small % traffic).  
   - Monitoring → rollback if unhealthy.  
   - Full rollout once stable.  

---

## 🛡️ DevSecOps Safety Nets

Automation adds **security + reliability** everywhere:

- **Before deploy:**  
  - Code scanning (SAST).  
  - Dependency checks.  
  - Vulnerability scans.  

- **During deploy:**  
  - Canary rollout + auto-rollback.  
  - Environment gates (approvals for Testnet/Production).  
  - All secrets pulled from **GCP Secret Manager** (no passwords in code).  

- **After deploy:**  
  - Monitoring dashboards for uptime, latency, cost.  
  - Alerts to Slack/Email if error budgets or costs spike.  
  - Continuous penetration testing & compliance audits.  
