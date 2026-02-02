# Agent-First Development Hub & Spoke Accelerator

**A framework for managing AI agent-driven development workflows with automatic propagation of updates across dependent projects.**

Created by: Peng Cao  
Category: AI/Engineering  
Tech Stack: VS Code Copilot, Agent Frameworks  
Status: 🟢 Open - Ready for selective usage with client projects

---

## 📋 What Is This?

The Agent-First Development Hub implements a **hub-and-spoke pattern** where:

- **Hub** (`.github/copilot-instructions.md`): Central file that AI agents read first
- **Spokes** (`.github/instructions/*.md`): Specialized docs for different domains
- **Triggers** (`doc-mapping.json`): Configuration that auto-propagates updates

**Benefits:**
- ✅ Agents automatically get project context
- ✅ Documentation stays synchronized with code
- ✅ Knowledge propagates across dependent projects
- ✅ No orphan documentation files

---

## 🚀 Quick Start

### 1. Copy the `.github` Folder to Your Project

**Important:** Copy the contents of `vscode-copilot/.github/` into your project's `.github/` directory:

```bash
# From this repo's root, copy to your project
cp -r vscode-copilot/.github /path/to/your-project/

# This will add:
# your-project/.github/copilot-instructions.md
# your-project/.github/doc-mapping.json
# your-project/.github/instructions/*.md
```

### 2. Customize the Files

**Edit `.github/copilot-instructions.md`:**
- Replace `[Add your tech stack]` with your actual stack
- Update Documentation Index with your spoke files
- Adjust task router for your project types

**Edit `.github/doc-mapping.json`:**
- Replace `[YOUR-PROJECT-NAME]` with your project name
- Uncomment and customize example spokes/agents
- Add your project-specific documentation paths

**Edit `.github/instructions/*.md`:**
- Update conventions.md with your git/code standards
- Update engineering-codebase-map.md with your file structure
- Update operations-deployment.md with your deployment process

### 3. Test with Copilot

Open your project in VS Code - Copilot will automatically read `.github/copilot-instructions.md` and provide context-aware suggestions.

---

## 📁 What's Included

```
Agent-First-Development-Hub/
├── .github/
│   ├── copilot-instructions.md       # Hub file (agent entry point)
│   ├── doc-mapping.json               # Agent dependencies & triggers
│   └── instructions/                  # Spoke documentation
│       ├── conventions.md             # Git commit format, code standards
│       ├── engineering-codebase-map.md # File locations, naming conventions
│       └── operations-deployment.md   # Deploy procedures, infrastructure
└── README.md                          # This file (setup guide)
```

---

## 🏗️ Hub-and-Spoke Pattern

```
copilot-instructions.md (Hub)
         │
         ├─→ conventions.md (Spoke)
         ├─→ engineering-codebase-map.md (Spoke)
         └─→ operations-deployment.md (Spoke)
```

**How it works:**

1. Agent reads hub file first
2. Hub links to relevant spoke docs
3. Agent reads specific spokes as needed
4. Code changes → Doc updates in same commit
5. `doc-mapping.json` validates dependencies

---

## 💡 Key Concepts

### No Orphan Files
All documentation lives in `.github/instructions/` - no scattered `.md` files

### Docs-in-Commit
Code changes and doc updates happen in the same commit

### Hub-First Navigation
Always start at the hub, follow links to spokes

### Auto-Propagation
Changes to hub automatically notify dependent spokes via `doc-mapping.json`

---

## 📝 Writing Good Instructions

**Be Specific:**
- ✅ "Use TypeScript with strict mode"
- ❌ "Use a typed language"

**Show Examples:**
```markdown
### Git Commit Format
```
feat(auth): add OAuth2 authentication
fix(api): resolve timeout issue
```
```

**Link to Real Files:**
- ✅ "See [conventions.md](instructions/conventions.md) for standards"
- ❌ "Check the conventions file"

**Use Placeholders:**
- `[Add your tech stack]`
- `[YOUR-PROJECT-NAME]`
- `[Add your deployment commands]`

---

## 🎯 For Production Projects

When using this template in a real project:

1. **Update placeholders** in all files
2. **Uncomment examples** in `doc-mapping.json`
3. **Add project-specific spokes** (business-strategy.md, product-roadmap.md, etc.)
4. **Define agent dependencies** for your workflow
5. **Enable documentation enforcement** for critical paths

See `receiptclaimer` project for a real-world example.

---

## 🤝 Contributing

Contributions welcome! This is a living template that improves through usage.

**What to contribute:**
- Examples for different tech stacks
- Agent configuration patterns
- Best practices from production usage
- Improvements to template structure

---

## 📖 Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [VS Code Copilot Extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

---

## License

**IP Status**: 🟢 Open - Ready for selective/cautious usage with clients' projects

---

**Questions?** Contact Peng Cao or open an issue!
