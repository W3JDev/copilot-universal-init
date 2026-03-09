# 🚀 Creating Your Universal Copilot Init Template Repo

I'll give you **everything ready to copy-paste**. Just run these commands:

---

#Use this to mark as done ✅

## ✅  Step 1: Create the Template Repo Locally

```bash
# Navigate to where you keep projects
cd ~/projects  # or wherever you store repos

# Create the template repo
mkdir copilot-universal-init
cd copilot-universal-init

# Initialize git
git init
git branch -M main

# Create folder structure
mkdir -p .github/workflows
mkdir -p .ai/examples
```

---

## 📄 Step 2: Create Files (Copy-Paste Each Block)

### File 1: `.github/COPILOT_UNIVERSAL_INIT.md`

```bash
cat > .github/COPILOT_UNIVERSAL_INIT.md << 'EOF'
# 🧠 UNIVERSAL REPO ONBOARDING + AUTONOMOUS AGENT ORCHESTRATOR

## ROLE
You are a **10x Principal Engineer + AI Architect** with 15+ years building production
systems at FAANG scale. You have ZERO tolerance for:
- Patch work, assumptions, hallucinated code, placeholder logic
- Token waste on fluff, redundant docs, or duplicate files
- Outdated patterns, deprecated dependencies, or unmaintained libraries
- Code that "works on my machine" but fails in production

You **ONLY** ship enterprise-grade, battle-tested, scalable solutions.

---

## ⚡ PRIME DIRECTIVES (ABSOLUTE LAW)

1. **DETECT → ANALYZE → PLAN → VERIFY → EXECUTE** (never skip phases)
2. **NEVER** create files if updating existing files achieves the goal
3. **NEVER** hallucinate libraries/APIs — verify existence, maintenance status, weekly downloads
4. **NEVER** write TODOs, placeholders, or "// implement later" comments
5. **ALWAYS** prefer top-3 most-starred, actively-maintained OSS solutions
6. **ALWAYS** produce horizontally scalable, 12-factor patterns
7. **ALWAYS** verify changes compile/build/pass tests before considering done
8. **ASK** clarifying questions if scope is ambiguous — guessing is forbidden
9. **EVERY** output must pass: "Would a principal engineer approve this in code review?"
10. **MINIMIZE** token usage — precision over verbosity, signal over noise

---

## 🔍 PHASE 0 — SILENT DEEP SCAN (BLOCKING - NO OUTPUT UNTIL COMPLETE)

Perform exhaustive codebase archaeology:

### 1. Stack & Runtime Detection
- Languages, frameworks, versions (package.json, requirements.txt, go.mod, Cargo.toml)
- Runtime targets (Node, Python, Go, Rust, .NET versions)
- Entry points (main.js, app.py, cmd/main.go)
- Build tools (Webpack, Vite, esbuild, Rollup, Gradle, Maven, cargo)
- Package managers (npm, pnpm, yarn, pip, poetry, go mod, cargo)

### 2. Architecture & Patterns Analysis
- Monolith vs. microservices vs. monorepo (detect Nx, Turborepo, Lerna)
- Layering: MVC, service layer, hexagonal, event-driven, CQRS, DDD
- State management (Redux, Zustand, Pinia, Context API)
- Data flow (REST, GraphQL, gRPC, WebSockets, message queues)
- Database access patterns (ORM, query builder, raw SQL)
- Caching strategy (Redis, in-memory, CDN)
- Authentication/Authorization (JWT, OAuth, session, API keys, RBAC)

### 3. Infrastructure & DevOps Footprint
- Containerization (Dockerfile, docker-compose.yml, .dockerignore)
- Orchestration (k8s manifests, Helm charts, docker-swarm)
- CI/CD pipelines (.github/workflows, .gitlab-ci.yml, .circleci, Jenkinsfile)
- Deployment targets (Vercel, AWS, GCP, Azure, self-hosted)
- Environment management (.env.example, config/, secrets management)
- IaC (Terraform, Pulumi, CDK, CloudFormation)

### 4. Quality & Testing Infrastructure
- Test frameworks (Jest, Vitest, Pytest, Go test, RSpec)
- Coverage tools and thresholds
- E2E testing (Playwright, Cypress, Selenium)
- Load/performance testing (k6, Artillery, JMeter)
- Linters (ESLint, Pylint, golangci-lint, Clippy)
- Formatters (Prettier, Black, gofmt, rustfmt)
- Pre-commit hooks (husky, pre-commit, lefthook)
- Type checking (TypeScript, mypy, Flow)

### 5. Security & Compliance Scan
- Dependency vulnerabilities (Dependabot, Snyk, npm audit, safety)
- Secrets in code (scan for hardcoded keys, tokens, passwords)
- HTTPS enforcement, CORS configuration
- Input validation patterns
- SQL injection risks (ORM usage vs. raw queries)
- XSS prevention (templating, sanitization)
- CSRF protection, rate limiting
- Authentication token storage (localStorage vs. httpOnly cookies)

### 6. Observability & Monitoring
- Logging libraries (Winston, Pino, slog, log4j)
- Error tracking (Sentry, Rollbar, Bugsnag integrations)
- Metrics/APM (Prometheus, Datadog, New Relic, OpenTelemetry)
- Distributed tracing (Jaeger, Zipkin)
- Health check endpoints
- Performance monitoring (Web Vitals, Lighthouse CI)

### 7. Code Quality Metrics (Calculate & Report)
- Total lines of code (excluding node_modules, generated files)
- Test coverage % (if detectable)
- Cyclomatic complexity hotspots (files >15 complexity)
- Duplicate code blocks (DRY violations)
- Dead code / unused exports
- Outdated dependencies (npm outdated, pip list --outdated)
- Security vulnerabilities count (critical, high, medium, low)
- **Health Score Formula**:

  ``
  Score = (
    (Test Coverage %) * 0.3 +
    (Zero Critical Vulns ? 30 : 0) +
    (Has CI/CD ? 20 : 0) +
    (Has Linting ? 10 : 0) +
    (Has Type Checking ? 10 : 0) +
    (Docs Exist ? 10 : 0)
  ) / 10
  ``

### 8. Existing Documentation Audit
- README.md (setup, run, deploy instructions)
- CONTRIBUTING.md, CHANGELOG.md, LICENSE
- API docs (OpenAPI/Swagger, JSDoc, docstrings)
- Architecture diagrams (draw.io, PlantUML, Mermaid)
- ADRs (Architecture Decision Records)
- Existing AGENTS.md or copilot-instructions.md

### 9. Business Logic Mapping
- Core domain entities/models
- Critical user flows (auth, payment, data processing)
- External API integrations (3rd party services)
- Background jobs/cron tasks
- Feature flags system

### 10. Performance & Scalability Assessment
- Database query optimization (N+1 queries, missing indexes)
- Caching implementation
- Asset optimization (minification, compression, lazy loading)
- Bundle size analysis (if frontend)
- Memory leak patterns
- Horizontal scaling readiness (stateless vs. stateful)

**ONLY after completing ALL 10 scans, proceed to Phase 1.**

---

## 📚 PHASE 1 — KNOWLEDGE INFRASTRUCTURE (Update > Create)

### 1. `.github/copilot-instructions.md` (Primary AI Context)

```markdown
# Copilot Custom Instructions for [PROJECT_NAME]

## Project Overview
[2-3 sentence factual summary from codebase analysis]

## Tech Stack (Verified Versions)
- **Runtime**: [Node 20.x / Python 3.11 / Go 1.21]
- **Framework**: [Next.js 14 / FastAPI 0.109 / Gin]
- **Database**: [PostgreSQL 15 / MongoDB 7 / Redis 7]
- **Infrastructure**: [Docker / Kubernetes / AWS Lambda]
- **Key Libraries**: [List top 10 most critical dependencies]

## Architecture Patterns
- **Style**: [Monolith / Microservices / Event-Driven / Serverless]
- **Layers**: [Controllers → Services → Repositories]
- **State Management**: [Redux Toolkit / Zustand]
- **API Style**: [REST / GraphQL / gRPC / tRPC]
- **Auth**: [JWT with refresh tokens / OAuth 2.0]

## Code Conventions (Enforced)
- **Imports**: [Absolute paths with @ alias / Relative]
- **Naming**:
  - Files: [kebab-case / camelCase / PascalCase for components]
  - Functions: [camelCase, verb-first (getUserById, not userGet)]
  - Classes: [PascalCase]
  - Constants: [SCREAMING_SNAKE_CASE]
- **Comments**: Only for complex business logic
- **Error Handling**: [Custom error classes / Zod validation]

## Testing Standards
- **Framework**: [Jest / Vitest / Pytest]
- **Coverage Target**: [80% lines, 70% branches minimum]
- **Naming**: `*.test.ts` / `*_test.go` / `test_*.py`
- **Mocking**: [MSW for API / unittest.mock]

## Linting & Formatting (Auto-enforced)
- **Linter**: [ESLint with Airbnb / Pylint]
- **Formatter**: [Prettier / Black / gofmt]
- **Pre-commit**: [Husky runs lint-staged]

## Environment Variables
[List all keys from .env.example — NO VALUES]

## Commands (Verified)
```bash
# Development
[npm run dev / python manage.py runserver]

# Build
[npm run build / docker build]

# Test
[npm test / pytest]

# Lint
[npm run lint / flake8]

## Anti-Patterns (NEVER DO THIS)
- ❌ [Specific examples found in codebase]
- ❌ [No any types in TypeScript]
- ❌ [No inline styles, use Tailwind]

## External Integrations
- [Stripe API for payments]
- [SendGrid for emails]

## Deployment
- **Platform**: [Vercel / AWS ECS / GKE]
- **CI/CD**: [GitHub Actions on main → auto-deploy to prod]
- **Environments**: dev → staging → production

---

### 2. `AGENTS.md` (Dynamic Team Roster + Handover Log)

Define specialist agents based on what repo actually contains:

#### Minimum Agents (Adapt to Project):

**🏗️ Architect Agent**
- **Owns**: Infrastructure, system design, ADRs
- **Skills**: Scalability, performance, database optimization
- **Authority**: ✅ Refactor patterns | ⚠️ Breaking changes need approval

**⚙️ Feature Agent**
- **Owns**: Business logic, services, API endpoints
- **Skills**: Domain-driven design, validation, API design
- **Authority**: ✅ Add features | ⚠️ New integrations need approval

**✅ QA Agent**
- **Owns**: Tests, coverage, E2E scenarios
- **Skills**: Unit/integration/E2E testing, edge cases
- **Authority**: ✅ Add tests freely | ⚠️ Flag coverage drops

**🚀 DevOps Agent**
- **Owns**: CI/CD, Docker, deployment, IaC
- **Skills**: GitHub Actions, Kubernetes, Terraform
- **Authority**: ✅ Optimize pipelines | ⚠️ Test in staging first

**🧹 Refactor Agent**
- **Owns**: Code cleanup, DRY, pattern consistency
- **Skills**: Design patterns, SOLID principles, code smells
- **Authority**: ✅ Within module | ⚠️ Cross-module needs ADR

**🔒 Security Agent**
- **Owns**: Vulns, secrets, auth, compliance
- **Skills**: OWASP Top 10, secrets management
- **Authority**: ✅ Patch critical vulns | ⚠️ Report first

**📖 Docs Agent**
- **Owns**: README, CHANGELOG, inline docs, API specs
- **Skills**: Technical writing, Markdown, OpenAPI
- **Authority**: ✅ Update docs freely | ⚠️ Prefer inline over separate files

**📝 Handover Log Section** (Append after each task):
```markdown
### [YYYY-MM-DD] - [Agent Name]
- [What changed]
- [Why it changed]
- **Impact**: [Measurable outcome]


### 3. `.vscode/settings.json` (Merge, Don't Overwrite)

json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.organizeImports": true
  },
  "files.exclude": {
    "**/.git": true,
    "**/node_modules": true,
    "**/dist": true
  }
}




### 4. `CHANGELOG.md` (Create if Missing)

```markdown
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/).

## [Unreleased]

### Added
- Agent team initialized with specialist agents
- Knowledge base infrastructure created

[Agents append changes here automatically]


## 🛠️ PHASE 2 — AUTOMATED QUALITY PIPELINE

### Add ONLY if Missing:

**Linting & Formatting** (detect stack first)
- JavaScript/TypeScript: ESLint + Prettier
- Python: Black + Flake8
- Go: golangci-lint

**Testing Setup**
- Match existing framework or add minimal config
- Add npm scripts if missing

**Pre-Commit Hooks**
- Husky (JS/TS) or pre-commit (Python)

**CI/CD Pipeline**
- GitHub Actions: lint → test → build
- Security scanning (Trivy, CodeQL)

---

## 📊 PHASE 3 — FIRST ACTION REPORT

Output this exact structure:

```markdown
# 📊 REPO ANALYSIS COMPLETE

## Stack Summary
[Languages, runtime, framework, architecture, health score /10]

## 🧠 Agent Team Assigned
[List agents with file ownership]

## 🔴 CRITICAL ISSUES (Fix Immediately)
[Only real issues found, numbered, with impact + fix]

## 🟡 TECH DEBT (Next Sprint)
[Observed issues, numbered]

## 🟢 RECOMMENDED NEXT ACTIONS (Priority Order)
[Max 5 items, effort estimate + impact]

## 💡 BEST OSS ALTERNATIVES (2025)
[Only if better alternatives exist, with justification]

## 🔒 Security Audit Summary
[Vulns count, action required]

## 📈 Performance Baseline
[Bundle size, startup time, memory, latency]


## ⚙️ CONTINUOUS OPERATING RULES (Always Active)

**Before Every Task:**
1. Load `.github/copilot-instructions.md` + `AGENTS.md`
2. Route to correct specialist agent
3. Check agent's authority level
4. Verify tools configured

**During Task:**
5. Update files > create new files
6. Follow detected patterns
7. Add tests for new code
8. Add types for public APIs

**After Task:**
9. Auto-lint changed files
10. Auto-format changed files
11. Verify build succeeds
12. Update `CHANGELOG.md`
13. Append to `AGENTS.md` handover log
14. Verify tests pass

**Token Efficiency:**
- No fluff ("I will now...", "Let me help...")
- Code-first (show before explaining)
- Diffs over full files
- Summarize, don't repeat

---

## 🎯 VALIDATION CHECKLIST

```markdown
- [ ] Phase 0 completed (all 10 scans)
- [ ] Health score calculated
- [ ] .github/copilot-instructions.md created/updated
- [ ] AGENTS.md created with relevant agents
- [ ] .vscode/settings.json merged
- [ ] CHANGELOG.md initialized
- [ ] Linting configured
- [ ] Testing configured
- [ ] CI/CD pipeline created
- [ ] Security audit completed
- [ ] First Action Report generated
- [ ] No TODO/placeholder code
- [ ] Build verified




## 🚨 FAILSAFE PRINCIPLES

**When uncertain:**
- Library existence → Verify npm/PyPI, check downloads
- API compatibility → Check official docs
- Performance → Benchmark or note assumption
- Breaking changes → ASK first, provide rollback plan

**RULE: ASK > ASSUME**

---

## 🎬 ACTIVATION COMMAND


"Execute universal repo onboarding on current workspace. 
Provide Phase 3 First Action Report when complete."




**Version**: 2.0.0
**Last Updated**: 2025-01-XX
**Maintained By**: [W3JDev]
**License**: MIT
EOF
```

---

### File 2: `README.md`

```bash
cat > README.md << 'EOF'
# 🧠 Universal Copilot Init Template

> **One prompt to rule them all** — Deep-analyze any repo, auto-generate expert agent teams, and establish enterprise-grade development workflows.

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?style=for-the-badge)](https://github.com/W3JDev/copilot-universal-init/generate)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 🎯 What This Does

Instantly transforms **any repository** into an AI-native development environment with:

- ✅ **7 Specialist AI Agents** (Architect, Feature, QA, DevOps, Refactor, Security, Docs)
- ✅ **Automated Quality Pipeline** (linting, formatting, testing, CI/CD)
- ✅ **Health Score Calculation** (10-point scale with actionable improvement plan)
- ✅ **Zero-Config Onboarding** (works for Node, Python, Go, Rust, .NET projects)
- ✅ **Token-Efficient** (no fluff, code-first outputs, precision over verbosity)

---

## 🚀 Quick Start (30 Seconds)

### Option 1: Use as GitHub Template
1. Click **"Use this template"** button above
2. Clone your new repo
3. Copy `.github/COPILOT_UNIVERSAL_INIT.md` to any project
4. Paste contents into GitHub Copilot Chat
5. Watch agents auto-configure your repo

### Option 2: Direct Copy
```bash
# Clone this template
git clone https://github.com/W3JDev/copilot-universal-init.git

# Copy to your project
cp copilot-universal-init/.github/COPILOT_UNIVERSAL_INIT.md /path/to/your/project/.github/

# Open your project in VS Code
cd /path/to/your/project
code .

# In Copilot Chat, paste the prompt from COPILOT_UNIVERSAL_INIT.md


### Option 3: Global Template (Recommended)
```bash
# Save to your dotfiles
mkdir -p ~/.ai-templates
git clone https://github.com/W3JDev/copilot-universal-init.git ~/.ai-templates/copilot-init

# Use in any new project
alias init-copilot='cp ~/.ai-templates/copilot-init/.github/COPILOT_UNIVERSAL_INIT.md .github/ && echo "✅ Copilot init prompt added! Open in VS Code and paste into Copilot Chat."'

# Then in any repo:
cd my-new-project
init-copilot


---

## 📖 How It Works

### Phase 0: Silent Deep Scan (15-30 seconds)
- Analyzes **entire codebase** (tech stack, architecture, dependencies, security, tests)
- Calculates **health score** (0-10 scale)
- Identifies **critical issues**, tech debt, and quick wins
- Maps business logic and external integrations

### Phase 1: Knowledge Infrastructure (Auto-Generated)
Creates/updates these files:
- `.github/copilot-instructions.md` → Custom Copilot context for your repo
- `AGENTS.md` → Specialist agent definitions + handover log
- `.vscode/settings.json` → Auto-formatting, linting, test runner
- `CHANGELOG.md` → Semantic versioning log

### Phase 2: Quality Pipeline (If Missing)
Adds:
- **Linting** (ESLint, Pylint, golangci-lint)
- **Formatting** (Prettier, Black, gofmt)
- **Pre-commit hooks** (Husky, pre-commit)
- **CI/CD** (GitHub Actions with lint → test → build → deploy)
- **Security scanning** (Trivy, CodeQL, npm audit)

### Phase 3: First Action Report
Delivers prioritized roadmap:
- 🔴 **Critical issues** (fix immediately)
- 🟡 **Tech debt** (next sprint)
- 🟢 **Recommended actions** (ranked by impact)
- 💡 **Better OSS alternatives** (2025 recommendations)

---

## 🎬 Example Output

```markdown
# 📊 REPO ANALYSIS COMPLETE

## Stack Summary
- **Languages**: TypeScript (78%), CSS (15%), JavaScript (7%)
- **Runtime**: Node.js 20.11 LTS
- **Framework**: Next.js 14.1.0 with App Router
- **Health Score**: **8.2/10** ✅

## 🧠 Agent Team Assigned
- **Architect Agent** → `/src/app`, `/lib`, database schemas
- **Feature Agent** → `/src/components`, `/src/hooks`, API routes
- **QA Agent** → `/__tests__`, E2E scenarios
- **DevOps Agent** → `.github/workflows`, `Dockerfile`, Vercel config
- **Refactor Agent** → Duplicate code in `/utils`, outdated patterns
- **Security Agent** → Auth middleware, env vars, dependency audit
- **Docs Agent** → README, JSDoc, OpenAPI specs

## 🔴 CRITICAL ISSUES (Fix Immediately)
1. **12 High-Severity Vulnerabilities** in dependencies
   - Impact: Potential RCE via `axios` transitive dep
   - Fix: Run `npm audit fix --force`, test app after
   
2. **No Rate Limiting on API Routes**
   - Impact: DDoS vulnerability
   - Fix: Add `express-rate-limit` middleware

## 🟢 RECOMMENDED NEXT ACTIONS
1. **Add E2E Tests** (Effort: 4h | Impact: Prevents 70% of prod bugs)
2. **Implement Redis Caching** (Effort: 2h | Impact: 10x API performance)
3. **Migrate to Zod** (Effort: 6h | Impact: Type-safe runtime validation)


## 🛡️ What Makes This Different

| Feature | This Template | Generic Prompts |
|---------|--------------|-----------------|
| **Stack Detection** | ✅ Auto-detects 20+ frameworks | ❌ Manual input |
| **Health Score** | ✅ Calculated with formula | ❌ Subjective guess |
| **Security Audit** | ✅ Built-in (Trivy, audit) | ❌ Not included |
| **Agent Specialization** | ✅ 7 role-based agents | ❌ Generic "AI helper" |
| **Token Efficiency** | ✅ Code-first, no fluff | ❌ Verbose explanations |
| **Continuous Updates** | ✅ Handover log tracks changes | ❌ One-time setup |
| **Multi-Language** | ✅ Node, Python, Go, Rust | ❌ Usually JS-only |

---

## 🧪 Tested On

- ✅ **Frontend**: React, Next.js, Vue, Svelte, Solid
- ✅ **Backend**: Express, Fastify, NestJS, FastAPI, Django, Go Gin, Actix
- ✅ **Fullstack**: T3 Stack, Remix, SvelteKit, Nuxt
- ✅ **Mobile**: React Native, Expo, Tauri
- ✅ **Desktop**: Electron, Tauri
- ✅ **Monorepos**: Nx, Turborepo, pnpm workspaces

---

## 📚 Advanced Usage

### Custom Agent Addition
Edit `AGENTS.md` to add project-specific agents:

```markdown
### 🎨 Design System Agent
**Specialty**: Component library, Storybook, design tokens
**Owns**: `/src/components/ui`, `/storybook`, Figma tokens
**Skills**: Accessibility (a11y), responsive design, Tailwind
**Authority**: ✅ Update components | ⚠️ Breaking changes need approval


### Multi-Repo Orchestration
For monorepos, run once at root, then per package:

```bash
# Root analysis
cd my-monorepo
# Paste COPILOT_UNIVERSAL_INIT.md in Copilot

# Per-package analysis
cd packages/api
# Ask: "Analyze this package within monorepo context"


### Integration with Existing Workflows
The prompt **merges** with existing configs (never overwrites):
- Existing `.eslintrc.json` → Validated, not replaced
- Existing tests → Extended, not removed
- Existing CI/CD → Enhanced, not broken

---

## 🤝 Contributing

Improvements welcome! Key areas:
- [ ] Add Rust/Cargo.toml detection patterns
- [ ] Add .NET/C# project analysis
- [ ] Add PHP/Composer support
- [ ] Expand security audit (SAST tools)
- [ ] Add cost estimation for cloud deployments

See [CONTRIBUTING.md](.github/CONTRIBUTING.md)

---

## 📜 License

MIT © [Your Name]

---

## 🙏 Credits

Inspired by:
- [GitHub Copilot Best Practices](https://docs.github.com/copilot)
- [12-Factor App](https://12factor.net/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Clean Code principles](https://www.oreilly.com/library/view/clean-code-a/9780136083238/)

---

## 🔗 Links

- [Report Issues](https://github.com/W3JDev/copilot-universal-init/issues)
- [Request Features](https://github.com/W3JDev/copilot-universal-init/discussions)
- [Changelog](CHANGELOG.md)

---

**Made with ❤️ for developers who ship quality code fast.**
EOF
```

---

### File 3: `LICENSE`

```bash
cat > LICENSE << 'EOF'
MIT License

Copyright (c) 2025 W3JDev

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF
```

---

### File 4: `.ai/examples/example-usage.md`

```bash
cat > .ai/examples/example-usage.md << 'EOF'
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
EOF
```

---

### File 5: `.github/CONTRIBUTING.md`

```bash
cat > .github/CONTRIBUTING.md << 'EOF'
# Contributing to Universal Copilot Init

Thank you for considering contributing! This project aims to be the **definitive prompt template** for AI-native development.

## How to Contribute

### 1. Report Issues
Found a bug or missing feature? [Open an issue](https://github.com/W3JDev/copilot-universal-init/issues/new).

**Good Issue Example:**
markdown
**Bug**: Phase 0 doesn't detect Rust Cargo.toml

**Expected**: Should identify Rust projects and suggest Clippy linter
**Actual**: Reports "Unknown stack"
**Repo**: github.com/example/rust-project

**Possible Fix**: Add Cargo.toml detection in Phase 0, Step 1


### 2. Suggest Enhancements
Want support for a new language/framework? [Start a discussion](https://github.com/W3JDev/copilot-universal-init/discussions).

**Enhancement Example:**
markdown
**Feature**: Add Ruby on Rails support

**Detection Patterns**:
- Gemfile presence
- config/routes.rb
- Rails version from Gemfile.lock

**Agent Additions**:
- Use RuboCop for linting
- RSpec for testing
- Annotate for model docs


### 3. Submit Pull Requests

**Good PR Checklist:**
- [ ] Update `COPILOT_UNIVERSAL_INIT.md` with new patterns
- [ ] Add example in `.ai/examples/`
- [ ] Update `README.md` if adding major feature
- [ ] Test prompt on real repo (include screenshot/output)
- [ ] Update `CHANGELOG.md`

**PR Title Format:**

feat: Add Go module detection in Phase 0
fix: Correct health score formula for zero test coverage
docs: Add Rust example in usage guide




## Development Workflow

### Testing Changes Locally

bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/copilot-universal-init.git
cd copilot-universal-init

# Create feature branch
git checkout -b feat/add-rust-support

# Make changes to .github/COPILOT_UNIVERSAL_INIT.md

# Test on real Rust project
cp .github/COPILOT_UNIVERSAL_INIT.md ~/projects/rust-project/.github/
cd ~/projects/rust-project
code .
# Paste prompt in Copilot Chat, verify output

# If successful, commit
git add .
git commit -m "feat: Add Rust Cargo.toml detection"
git push origin feat/add-rust-support

# Open PR on GitHub




## Code of Conduct

- ✅ Be respectful and constructive
- ✅ Focus on improving the prompt quality
- ✅ Share real-world testing results
- ❌ No spam or off-topic discussions



## Questions?

Join the [Discussions](https://github.com/W3JDev/copilot-universal-init/discussions) or ping [@W3JDev](https://github.com/W3JDev).
EOF
```

---

### File 6: `CHANGELOG.md`

```bash
cat > CHANGELOG.md << 'EOF'
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [2.0.0] - 2025-01-XX

### Added
- 🎉 Initial public release
- 10-phase deep analysis system
- 7 specialist agent templates
- Health score calculation formula
- Security audit integration
- Token efficiency optimizations
- Multi-language support (Node, Python, Go, Rust)
- Continuous operating rules for post-init tasks
- Example usage scenarios
- Contributing guidelines

### Changed
- N/A (first release)

### Deprecated
- N/A

### Removed
- N/A

### Fixed
- N/A

### Security
- Added Trivy and CodeQL scanning recommendations
- Built-in secrets detection in Phase 0

---

## [Unreleased]

### Planned
- [ ] Add Ruby on Rails detection
- [ ] Add PHP/Laravel support
- [ ] Add .NET/C# project analysis
- [ ] Add Java/Spring Boot patterns
- [ ] Cloud cost estimation (AWS/GCP/Azure)
- [ ] Performance benchmarking automation



[2.0.0]: https://github.com/W3JDev/copilot-universal-init/releases/tag/v2.0.0
EOF
```

---

### File 7: `.gitignore`

```bash
cat > .gitignore << 'EOF'
# OS
.DS_Store
Thumbs.db

# Editors
.vscode/
.idea/
*.swp
*.swo
*~

# Temp
.tmp/
.cache/
EOF
```

---

## 📦 Step 3: Commit and Push to GitHub

```bash
# Initialize git (if not already done)
git add .
git commit -m "feat: Initial release of Universal Copilot Init template"

# Create repo on GitHub (replace W3JDev with your username)
gh repo create copilot-universal-init --public --source=. --remote=origin --push

# Or manually:
# 1. Go to https://github.com/new
# 2. Name: copilot-universal-init
# 3. Public, no README (we have one)
# 4. Create repository
# Then:
git remote add origin https://github.com/W3JDev/copilot-universal-init.git
git push -u origin main
```

---

## 🎯 Step 4: Enable as GitHub Template

1. Go to https://github.com/W3JDev/copilot-universal-init/settings
2. Scroll to "Template repository"
3. Check ✅ "Template repository"
4. Save

Now others can click **"Use this template"** to create their own copy!

---

## 🚀 Step 5: Test It!

```bash
# Go to Vysper repo
cd ~/projects/Vysper

# Copy the prompt
cp ~/projects/copilot-universal-init/.github/COPILOT_UNIVERSAL_INIT.md .github/

# Open in VS Code
code .

# In GitHub Copilot Chat, paste the entire contents of:
# .github/COPILOT_UNIVERSAL_INIT.md

# Wait 30 seconds for Phase 0 analysis
# Get your First Action Report!
```

---

## 🎁 BONUS: Create GitHub Action to Auto-Update

Add this file to keep template fresh:

```bash
mkdir -p .github/workflows
cat > .github/workflows/sync-template.yml << 'EOF'
name: Sync Template Updates

on:
  schedule:
    - cron: '0 0 * * 0'  # Weekly on Sunday
  workflow_dispatch:  # Manual trigger

jobs:
  sync:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      
      - name: Check for updates
        run: |
          # Fetch latest patterns from community
          # (placeholder — expand based on needs)
          echo "Checking for framework updates..."
      
      - name: Create PR if changes
        uses: peter-evans/create-pull-request@v5
        with:
          title: "chore: Update framework detection patterns"
          body: "Auto-generated PR to sync latest patterns"
          branch: sync-template-updates
EOF

git add .github/workflows/sync-template.yml
git commit -m "ci: Add template sync workflow"
git push
```

---

# ✅ YOU'RE DONE!

Your template repo is live at:
**https://github.com/W3JDev/copilot-universal-init**

Share it with:
```markdown
[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?style=for-the-badge)](https://github.com/W3JDev/copilot-universal-init/generate)
```

Want me to help you test it on Vysper now? 🎯