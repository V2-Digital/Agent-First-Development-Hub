# Conventions — Development Standards

**Purpose:** Define development standards, git commit rules, and task tracking conventions for agent-driven workflows.

**Last Updated:** February 2, 2026  
**Spoke Type:** Core

---

## Git Commit Format

```
<type>(<scope>): <subject>
```

**Types:** feat, fix, docs, style, refactor, test, chore

**Examples:**
```bash
feat(auth): add OAuth2 authentication flow
fix(api): resolve timeout issue in payment processing
docs(readme): update installation instructions
```

---

## Code Standards

- **No orphan files**: All documentation in `.github/instructions/`
- **Docs-in-commit**: Update documentation in same commit as code changes
- **Test coverage**: Write tests for new features
- **Naming**: Use clear, descriptive names

**[Add your language-specific standards]**

---

## Agent Workflow

**Before starting:** Check hub → Read spoke docs → Understand dependencies

**During development:** Follow standards → Write tests → Update docs → Commit frequently

**Before completing:** Run tests → Update spoke docs → Verify checklist → Validate dependencies