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
