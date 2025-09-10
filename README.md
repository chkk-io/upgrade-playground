# Upgrade Playground

This repo contains example Infrastructure‑as‑Code (IaC) for various open‑source projects to demonstrate how to use Chkk + AI coding agents to upgrade while keeping changes in sync with your running environment.

### Without Chkk

You must manually:
- **Analyze live infrastructure and dependencies** across clusters, add‑ons, and apps
- **Decide target versions** and why, after **reading release notes and changelogs**
- **Identify breaking changes** and behavior changes, then plan mitigations
- **Edit all IaC files** (values.yaml, templates, CRDs) **while preserving customizations**
- Re‑validate everything in the correct order and fix fallout from subtle changes

### With Chkk
- Generate an upgrade plan in Chkk, **point your AI coding agent to the Chkk Upgrade Context server**, and **let it automate the heavy lifting**.

#### What you get?

  - **Environment‑aware diffs**, rationale, and specifications streamed into your IDE
  - Exact target files and edits proposed; customizations preserved where possible
  - **Breaking/behavior changes surfaced up front**; safer sequencing recommended
  - **You review the diff and merge** a clean, compliant PR

### Key Features

- **Bring your own model**: use Claude, GPT-5, Gemini, or any LLM your team runs
- **Use your favorite coding agent**: works with Cursor (Supported), Claude Code (Coming Soon), GitHub Copilot (Coming Soon)
- **Leverage existing AI contracts**: reuse your seats, tokens, and enterprise terms
- **Upgrade 100s of OSS projects**: Kubernetes, add‑ons, databases, data jobs/streams, and more
- **Read‑only by design**: no new repo permissions; source never leaves your repo
- **Minimal, relevant context**: fewer review cycles with rationale comments in PRs

### Start here
- [Chkk Upgrade Agent Quickstart](https://docs.chkk.io/overview/quickstart-upgrade-agent)
- [Cursor + Chkk in 5 minutes](https://docs.chkk.io/agentic-upgrades/cursor)
- [Claude Code + Chkk in 5 minutes](https://docs.chkk.io/agentic-upgrades/claude-code)

### Repo layout
- Top‑level IaC type directories:
  - `helm/` → `cert-manager/`, `external-secrets-operator/`, `argocd/` (ready to try)
  - `terraform/`  (placeholder)
  - `cloudformation/` → (placeholder)
- Inside each project directory:
  - You will find the source/IaC
  - Some directories are placeholders and may not contain files yet
