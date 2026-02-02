# Agent-First Development Hub — Agent Quick Start

> **⚠️ CRITICAL - READ FIRST:**
>
> - **Hub-and-Spoke Navigation:** Start here, follow links to spoke docs in `.github/instructions/`
> - **No Orphan Files:** Update existing spokes, don't create new `.md` files
> - **Docs-in-Commit:** Code changes + doc updates = same commit

**Mission:** Manage agent-driven workflows with automatic knowledge propagation across dependent agents.

**Stack:** VS Code Copilot • GitHub Actions • [Add your tech stack]

---

## 📚 Documentation Index

| Category        | Files                                                       | Purpose                          |
| --------------- | ----------------------------------------------------------- | -------------------------------- |
| **Core**        | [conventions.md](instructions/conventions.md)               | Standards, task tracking         |
| **Engineering** | [engineering-codebase-map.md](instructions/engineering-codebase-map.md) | File locations & patterns        |
| **Operations**  | [operations-deployment.md](instructions/operations-deployment.md) | Deploy, infrastructure           |

---

## 🎯 Quick Start

**First time?** Read [conventions.md](instructions/conventions.md) → Scan [engineering-codebase-map.md](instructions/engineering-codebase-map.md) → Start coding

**Making changes?** Check task router → Read relevant doc → Implement → Update docs in same commit

| Task Type                      | Primary Doc                                                             |
| ------------------------------ | ----------------------------------------------------------------------- |
| **Add/modify features**        | [engineering-codebase-map.md](instructions/engineering-codebase-map.md) |
| **Deploy**                     | [operations-deployment.md](instructions/operations-deployment.md)       |
| **Update agent configuration** | [doc-mapping.json](doc-mapping.json)                                    |

---

## 🏗️ Hub-and-Spoke Pattern

- **Hub** (this file): Central entry point
- **Spokes** (`.github/instructions/*.md`): Specialized docs
- **Triggers** (`doc-mapping.json`): Auto-update workflows

**How it works:** Hub update → `doc-mapping.json` detects changes → Notifies dependent spokes → Validates → Propagates

---

## ⚙️ Agent Configuration

Agents defined in `doc-mapping.json`:

```
Plan → AppModernization → CodeReview → Documentation
  ↓         ↓                ↓              ↓
  └─────────┴────────────────┴──────────────┘
```

---

## ✅ Before Completing Turn

- [ ] Tests pass
- [ ] Docs updated in same commit
- [ ] No new `.md` files outside `.github/instructions/`
- [ ] `doc-mapping.json` dependencies accurate
