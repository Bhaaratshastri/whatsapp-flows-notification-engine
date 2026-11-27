# Contributing Guide — WhatsApp Flows & Notification Engine

This repository follows GitHub Flow off `develop`, Conventional Commits, and automated static analysis to keep the package compliant with AppExchange Security Review standards (zero Severity 1 or Severity 2 findings).

---

## 1. Branching Strategy

| Branch | Purpose | Rules |
| :--- | :--- | :--- |
| **`main`** | Production / AppExchange release branch. | Protected. Untouched until release. Requires passing CI checks and at least **1 PR approval**. |
| **`develop`** | Default integration branch for active development. | All feature branches cut from `develop` and merge back into `develop` via PR. |
| **`feature/<ticket-id>-<short-name>`** | New features, stories, and engineering tasks. | Branch off `develop`, PR into `develop`. Example: `feature/WI016-ci-scanner-pipeline`. |
| **`hotfix/<ticket-id>-<short-name>`** | Urgent production fixes. | Branch off `main` (and back-merge into `develop`). Example: `hotfix/WI099-token-refresh-fix`. |

### Branch Naming Rules
- Use lowercase kebab-case after the ticket ID.
- Always include the tracking ticket ID (e.g., `WI016`).
- Delete feature branches after merging into `develop`.

---

## 2. Commit Message Conventions

All commits in a Pull Request must follow [Conventional Commits](https://www.conventionalcommits.org/):

```text
<type>(<optional-scope>): <short imperative description>