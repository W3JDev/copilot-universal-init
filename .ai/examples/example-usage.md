# 📘 Example Usage Scenarios

## Scenario 1: Brand New Next.js Project

**Before:**
```bash
npx create-next-app@latest my-app
cd my-app


**After adding template:**
```bash
# Copy the prompt
cp ~/.ai-templates/copilot-init/.github/COPILOT_UNIVERSAL_INIT.md .github/

# Open in VS Code
code .

# In Copilot Chat, paste the prompt
# Result: Agents auto-configure ESLint, Prettier, Playwright, GitHub Actions


**What You Get:**
- ✅ TypeScript strict mode configured
- ✅ ESLint with Next.js rules
- ✅ Prettier with Tailwind plugin
- ✅ Playwright E2E tests setup
- ✅ GitHub Actions CI/CD
- ✅ Pre-commit hooks with Husky
- ✅ 7 specialist agents documented

---

## Scenario 2: Legacy Python Django Project

**Context:**
- 5-year-old codebase
- No tests
- Manual deployment
- Inconsistent code style

**What Agents Do:**
1. **Architect Agent** → Identifies monolithic structure, suggests service extraction
2. **QA Agent** → Sets up Pytest, creates test pyramid plan
3. **DevOps Agent** → Adds Dockerfile, GitHub Actions, pre-commit hooks
4. **Security Agent** → Finds 23 vulnerabilities, patches critical ones
5. **Refactor Agent** → Flags 847 lines of duplicate code
6. **Docs Agent** → Generates API docs with Sphinx

**Output:**
```markdown
## 🔴 CRITICAL ISSUES
1. **Django 2.2 (End of Life)** → Upgrade to 4.2 LTS
2. **Hardcoded AWS Keys** in settings.py → Move to env vars
3. **SQL Injection Risk** in raw queries → Use ORM

## 🟢 RECOMMENDED NEXT ACTIONS
1. Add Pytest + coverage (Effort: 8h | Impact: Prevents regressions)
2. Containerize with Docker (Effort: 4h | Impact: Reproducible deploys)
3. Add Black + isort (Effort: 1h | Impact: Code consistency)




## Scenario 3: Microservices Monorepo (Turborepo)

**Structure:**

apps/
  web/          (Next.js)
  mobile/       (React Native)
  api/          (NestJS)
packages/
  ui/           (Shared components)
  utils/        (Shared utilities)


**Usage:**
```bash
# Root-level analysis
# Paste prompt in Copilot → Analyzes entire monorepo structure

# Per-app analysis
cd apps/api
# Ask: "Deep dive into this NestJS API within monorepo context"


**Result:**
- ✅ Root-level `AGENTS.md` with cross-cutting agents
- ✅ Per-app `.github/copilot-instructions.md`
- ✅ Shared ESLint config detected and respected
- ✅ Turborepo cache optimization suggestions
- ✅ Unified CI/CD pipeline for all apps

---

## Scenario 4: Open Source Onboarding

**Use Case:** Contributing to unfamiliar repo

**Before:**
- Spend 2 hours reading docs
- Grep codebase for patterns
- Guess at testing conventions

**After:**
```bash
# Clone unfamiliar repo
git clone https://github.com/some-org/cool-project.git
cd cool-project

# Add prompt
cp ~/.ai-templates/copilot-init/.github/COPILOT_UNIVERSAL_INIT.md .github/

# In Copilot Chat: "Onboard me to this codebase"


**What You Get in 30 Seconds:**
- ✅ Complete tech stack breakdown
- ✅ Architecture patterns explained
- ✅ Code conventions documented
- ✅ Test commands identified
- ✅ Build/run instructions verified
- ✅ Contribution workflow mapped

---

## Scenario 5: Security Audit Before Production

**Context:** About to deploy new feature

**Command:**

"Run Phase 0 security scan and generate audit report"


**Output:**
```markdown
## 🔒 Security Audit Summary

### Critical Vulnerabilities (2)
1. **CVE-2024-12345** in axios@0.21.1 → RCE via SSRF
   - Fix: `npm update axios@1.6.0`
2. **Hardcoded JWT Secret** in src/auth/config.ts
   - Fix: Move to VITE_JWT_SECRET env var

### High Severity (5)
- CORS misconfiguration (allows all origins)
- No rate limiting on /api/login
- Passwords logged in plaintext (logger.debug)
- localStorage used for tokens (use httpOnly cookies)
- Missing CSRF protection

### Medium Severity (12)
[... detailed list ...]

### Recommendations
- Enable Dependabot automated PRs
- Add GitHub CodeQL scanning
- Implement Helmet.js security headers
- Add express-rate-limit middleware


## Tips & Tricks

### 1. Incremental Adoption
Don't let agents change everything at once:

"Phase 1 only — generate knowledge base files, no code changes yet"


### 2. Focus on One Area

"Security Agent: audit dependencies and auth flow only"


### 3. Get Specific Recommendations

"What's the best caching strategy for this GraphQL API?"


### 4. Before/After Comparisons

"Show me the health score improvement if I implement all critical fixes"


### 5. Custom Constraints

"Analyze with constraint: must support Node 16 (cannot upgrade yet)"




## Common Questions

**Q: Will this overwrite my existing configs?**
A: No — agents **merge** with existing files. Existing `.eslintrc` is validated, not replaced.

**Q: How long does Phase 0 analysis take?**
A: 15-30 seconds for most repos, up to 2 minutes for large monorepos.

**Q: Can I use this with other AI tools (Cursor, Cline)?**
A: Yes — the prompt is tool-agnostic. Works with any AI that accepts context.

**Q: Does this work for non-JavaScript projects?**
A: Yes — supports Python, Go, Rust, .NET, PHP. Stack detection is automatic.

**Q: What if my repo uses an unsupported framework?**
A: Agents will still analyze common patterns (tests, linting, CI/CD). You can extend the prompt.



**Want more examples? [Open a discussion](https://github.com/W3JDev/copilot-universal-init/discussions)!**
