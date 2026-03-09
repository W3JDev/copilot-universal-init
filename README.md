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
