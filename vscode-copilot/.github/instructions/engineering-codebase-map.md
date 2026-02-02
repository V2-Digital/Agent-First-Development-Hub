# Engineering Codebase Map — File Locations & Patterns

**Purpose:** Map of file locations, directory structure, and code organization patterns for quick navigation.

**Last Updated:** February 2, 2026  
**Spoke Type:** Engineering

---

## Directory Structure

```
project-root/
├── .github/
│   ├── copilot-instructions.md    # Hub file
│   ├── doc-mapping.json            # Agent configuration
│   ├── instructions/               # Spoke docs
│   │   ├── conventions.md
│   │   ├── engineering-codebase-map.md
│   │   └── operations-deployment.md
│   └── workflows/                  # CI/CD (optional)
├── src/                            # Source code
│   ├── [Add your structure]
├── tests/                          # Test files
├── docs/                           # Additional documentation
└── [Add your directories]
```

---

## Core Files

| File                          | Purpose                              |
| ----------------------------- | ------------------------------------ |
| `.github/copilot-instructions.md` | Hub file - agent entry point     |
| `.github/doc-mapping.json`    | Agent dependencies & triggers        |
| `package.json` / `pom.xml`    | Dependencies & scripts               |
| `.env.example`                | Environment variable template        |
| `README.md`                   | Project overview & setup             |

---

## Source Code Organization

**[Add your source code structure]**

Example:
```
src/
├── components/     # UI components
├── services/       # Business logic
├── config/         # Configuration
└── utils/          # Utility functions
```

---

## Naming Conventions

- **Components**: PascalCase (`UserProfile.tsx`)
- **Services**: camelCase (`userService.ts`)
- **Tests**: Match source + `.test` or `.spec`
- **Constants**: UPPER_SNAKE_CASE
- **Functions**: camelCase
- **Classes/Types**: PascalCase