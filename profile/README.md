# Zephyr Systems

> Building the infrastructure for safe, autonomous AI agents

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux-lightgrey)](https://github.com/zephyr-systems)
[![Discord](https://img.shields.io/badge/community-Discord-7289da)](https://discord.gg/zephyr) *(coming soon)*

**[Get Started](https://github.com/zephyr-systems/zephyr)** • **[Documentation](https://github.com/zephyr-systems/zephyr/tree/main/docs)** • **[Community](https://github.com/zephyr-systems/zephyr/discussions)**

</div>

## What is Zephyr Systems?

**Zephyr Systems** is an open-source organization dedicated to making autonomous AI agents safer, faster, and more capable through better shell infrastructure.

We're building [Zephyr](https://github.com/zephyr-systems/zephyr)—a security-focused shell environment designed from the ground up for AI agents like Claude Code, Codex Computer Use, and similar AI-driven automation systems—along with a growing ecosystem of modules, tools, and integrations.

### The Problem We're Solving

AI agents today execute shell commands with full user privileges but operate in shell environments designed for humans, not autonomous systems. This creates serious challenges:

- **No safety boundaries** – Agents can accidentally (or maliciously) run destructive commands
- **Hidden capabilities** – Agents can't discover what shell functions are available without trial and error
- **Security blind spots** – No way to scan or validate code before it runs
- **Fragmented tooling** – Every team rebuilds the same utilities from scratch

### Our Solution

Zephyr provides the missing infrastructure layer between AI agents and the shell:

- **🔒 Security by design** – Built-in scanning prevents execution of malicious code
- **📦 Modular ecosystem** – Reusable, composable modules instead of scattered scripts
- **🤖 Agent-first API** – Machine-readable outputs and structured capability discovery
- **⚡ Zero friction** – Fast loading, simple installation, no configuration headaches

---

## The Zephyr Ecosystem

Our organization hosts several repositories that work together to create a complete platform for AI agents:

### 🏗️ Core Infrastructure

#### **[zephyr](https://github.com/zephyr-systems/zephyr)**
The foundation—a fast, secure shell loader that manages modules and enforces security policies.

**What it does:**
- Loads shell modules with dependency awareness
- Scans code for security risks before execution
- Provides JSON APIs for programmatic shell interaction
- Manages module installation from Git repositories

**Start here if you're:** A user wanting to install Zephyr, an AI engineer integrating agents, or a developer wanting to understand the technical architecture.

---

### 📚 Module Ecosystem

#### **[awesome-zephyr-modules](https://github.com/zephyr-systems/awesome-zephyr-modules)** *(coming soon)*
A curated directory of community and official modules, vetted for quality and security.

**What you'll find:**
- Recommended modules organized by category
- Security ratings and compatibility info
- Installation guides and quick examples
- Community module submissions

**Start here if you're:** Looking for existing modules to extend your shell, or wanting to publish your own module to the community.

---

### 🎯 Standard Library Modules

Pre-built, security-audited modules that solve common agent automation needs:

#### **Core Utilities** *(in development)*
- **[zephyr-core](https://github.com/zephyr-systems/zephyr-core)** – Essential shell helpers and common patterns
- **[zephyr-colors](https://github.com/zephyr-systems/zephyr-colors)** – Terminal theming and color utilities
- **[zephyr-utils](https://github.com/zephyr-systems/zephyr-utils)** – File operations, string manipulation, common tasks

#### **Security & Compliance** *(in development)*
- **[zephyr-audit](https://github.com/zephyr-systems/zephyr-audit)** – Command logging and audit trails for agents
- **[zephyr-sandbox](https://github.com/zephyr-systems/zephyr-sandbox)** – Isolated execution with resource limits
- **[zephyr-secrets](https://github.com/zephyr-systems/zephyr-secrets)** – Secure credential management

#### **AI Agent Integrations** *(in development)*
- **[zephyr-claude](https://github.com/zephyr-systems/zephyr-claude)** – Anthropic Claude Code integration helpers
- **[zephyr-codex](https://github.com/zephyr-systems/zephyr-codex)** – OpenAI Codex Computer Use utilities
- **[zephyr-openclaw](https://github.com/zephyr-systems/zephyr-openclaw)** – OpenClaw environment integration

#### **Development Tools** *(in development)*
- **[zephyr-git](https://github.com/zephyr-systems/zephyr-git)** – Git workflow automation
- **[zephyr-docker](https://github.com/zephyr-systems/zephyr-docker)** – Container management utilities
- **[zephyr-k8s](https://github.com/zephyr-systems/zephyr-k8s)** – Kubernetes helpers

---

## Who is Zephyr For?

### 🤖 AI/ML Engineers
Building autonomous agents that need safe shell access? Zephyr gives you security scanning, capability discovery, and structured APIs right out of the box.

**Your path:** [Core repo](https://github.com/zephyr-systems/zephyr) → [Integration guide](https://github.com/zephyr-systems/zephyr/blob/main/docs/INTEGRATION.md) → Agent-specific modules

### 💻 Power Users
Want a cleaner, more organized shell with security built in? Zephyr's modular approach means you only load what you need, when you need it.

**Your path:** [Quick start](https://github.com/zephyr-systems/zephyr#quick-start) → [Standard library modules](#-standard-library-modules) → Community modules

### 🛠️ Module Developers
Building tools for the shell? Publish to our ecosystem and reach users who need secure, vetted modules.

**Your path:** [Module development guide](https://github.com/zephyr-systems/zephyr/blob/main/docs/MODULE_DEVELOPMENT.md) → [awesome-zephyr-modules](#-module-ecosystem) → Community support

### 🏢 Enterprise Teams
Deploying AI agents at scale? Zephyr's audit trails, policy enforcement, and module verification provide the governance layer you need.

**Your path:** [Enterprise features roadmap](#phase-3-enterprise-features-q3-2026) → [Security model](https://github.com/zephyr-systems/zephyr/blob/main/docs/SECURITY_PIPELINE.md) → Community discussions

---

## Quick Start

Get Zephyr running in under 5 minutes:

```bash
# 1. Install the core loader
git clone https://github.com/zephyr-systems/zephyr.git
cd zephyr && make install

# 2. Add to your shell
echo 'eval "$($HOME/.zsh/bin/zephyr load)"' >> ~/.zshrc

# 3. Start using it
exec zsh
zephyr list
```

For detailed installation instructions, troubleshooting, and configuration options, see the [core repository](https://github.com/zephyr-systems/zephyr).

---

## Roadmap

We're building Zephyr in public. Here's what's coming:

### Phase 1: Foundation (Q1 2026)
**Status:** In progress

Establishing the core infrastructure and initial module ecosystem.

- ✅ Core zephyr loader with security scanning
- ✅ Module installation and dependency management
- ✅ JSON APIs for AI integration
- ⏳ First stdlib modules (core, colors, utils)
- ⏳ awesome-zephyr-modules directory launch

### Phase 2: AI Agent Hardening (Q2 2026)
**Status:** Planning

Purpose-built tools for autonomous agent safety and observability.

- Agent-specific integration modules
- Command audit logging and replay
- Sandboxed execution environments
- Resource monitoring and limits
- Policy-based command filtering

### Phase 3: Enterprise Features (Q3 2026)
**Status:** Design phase

Enterprise-grade governance and compliance capabilities.

- Centralized module registry with signing
- Organization-level policy management
- Module approval workflows
- Multi-tenancy and user isolation
- Compliance reporting

### Phase 4: Ecosystem Growth (Q4 2026)
**Status:** Conceptual

Building community and expanding the module marketplace.

- Public module marketplace
- Automated module testing framework
- CI/CD integration templates
- Official certification program
- Commercial support options

---

## Why Open Source?

We believe the infrastructure that powers AI agents should be:

- **Transparent** – Anyone can audit the security model and scanning logic
- **Community-driven** – Better modules come from diverse perspectives and use cases
- **Freely available** – Critical safety infrastructure shouldn't be behind paywalls
- **Collaborative** – The challenges of agent security are industry-wide

That's why Zephyr and all first-party modules are MIT-licensed and developed in the open.

---

## Get Involved

Zephyr is stronger with community contributions. Here's how you can help:

### 🐛 Report Issues
Found a bug or security concern? [Open an issue](https://github.com/zephyr-systems/zephyr/issues) in the relevant repository.

### 💡 Share Ideas
Have suggestions for modules, features, or integrations? Start a [discussion](https://github.com/zephyr-systems/zephyr/discussions).

### 🔨 Contribute Code
Ready to build? Check our [contribution guide](https://github.com/zephyr-systems/zephyr/blob/main/CONTRIBUTING.md) and look for `good-first-issue` labels.

### 📦 Build Modules
Created something useful? Share it with the community via [awesome-zephyr-modules](https://github.com/zephyr-systems/awesome-zephyr-modules).

### 📢 Spread the Word
Using Zephyr? Star our repos, share your experience, and help others discover the project.

---

## Community & Support

### 📖 Documentation
- **[Main Docs](https://github.com/zephyr-systems/zephyr/tree/main/docs)** – Complete guides and API reference
- **[Module Development](https://github.com/zephyr-systems/zephyr/blob/main/docs/MODULE_DEVELOPMENT.md)** – Create your own modules
- **[Security Model](https://github.com/zephyr-systems/zephyr/blob/main/docs/SECURITY_PIPELINE.md)** – How scanning works
- **[AI Integration](https://github.com/zephyr-systems/zephyr/blob/main/docs/INTEGRATION.md)** – Agent integration patterns

### 💬 Discussion
- **[GitHub Discussions](https://github.com/zephyr-systems/zephyr/discussions)** – Questions, ideas, and community
- **[Discord](https://discord.gg/zephyr)** *(coming soon)* – Real-time chat and support

### 🐦 Updates
- Follow development updates and announcements *(coming soon)*

---

## Related Projects

Zephyr builds on and works alongside these excellent tools:

- **[Oh My Zsh](https://ohmyz.sh/)** – The original modular ZSH configuration (Zephyr is compatible!)
- **[Zinit](https://github.com/zdharma-continuum/zinit)** – Fast ZSH plugin manager
- **[Claude Code](https://www.anthropic.com/claude)** – AI assistant with shell execution
- **[OpenClaw](https://openclaw.ai/)** – Open-source agent framework

---

## License

All Zephyr Systems projects are released under the **[MIT License](LICENSE)** unless otherwise specified.

Third-party modules in the ecosystem maintain their own licenses.

---

## Acknowledgments

Zephyr is built with modern systems programming tools:

- **[Odin](https://odin-lang.org/)** – Fast, productive systems language
- **[libgit2](https://libgit2.org/)** – Git integration for module management
- **[TOML](https://toml.io/)** – Human-friendly configuration format

---

<div align="center">

### Ready to build safer AI agents?

**[Install Zephyr](https://github.com/zephyr-systems/zephyr)** | **[Read the Docs](https://github.com/zephyr-systems/zephyr/tree/main/docs)** | **[Join the Community](https://github.com/zephyr-systems/zephyr/discussions)**

*Making autonomous agents safer, one shell at a time*

</div>
