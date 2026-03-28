# Project Analyzer - Path Guide

## Core Principle

**Analysis documents are ALWAYS saved to the centralized hub at `~/ai/code-analysi/{project-name}/`**

The `{project-name}` is derived from the project directory's basename. This centralized layout enables the `docs-site` skill to scaffold a multi-project hub that hosts all analysis documents as a browsable web site.

## Directory Structure

```
~/ai/code-analysi/
├── kubernetes/                      # Project: kubernetes
│   ├── changelog.md
│   ├── kubernetes-analysis.md
│   ├── analysis-todo.md
│   ├── topics/
│   │   ├── 01-project-basic-info.md
│   │   ├── 02-project-structure.md
│   │   └── ...
│   └── assets/
├── tokio/                           # Project: tokio
│   └── ...
├── zinx/                            # Project: zinx
│   └── ...
└── site/                            ← docs-site skill scaffolds this
    ├── src/
    ├── package.json
    └── wrangler.toml
```

## Path Resolution Rules

### From Project Path to Output Path

| User Input | Project Name | Output Directory |
|---|---|---|
| `/Users/ccc/work/todo/kubernetes` | `kubernetes` | `~/ai/code-analysi/kubernetes/` |
| `/Users/ccc/work/my-project` | `my-project` | `~/ai/code-analysi/my-project/` |
| `.` (current dir named `zinx`) | `zinx` | `~/ai/code-analysi/zinx/` |
| `../neighbor-project` | `neighbor-project` | `~/ai/code-analysi/neighbor-project/` |
| `owner/repo` (GitHub) | `repo` | `~/ai/code-analysi/repo/` |

**Derivation**: `basename(project-path)` → `~/ai/code-analysi/{basename}/`

## Why This Design?

1. **Centralized Hub**: All analysis in one place, making it easy for `docs-site` to build a multi-project documentation site
2. **Separation of Concerns**: Analysis docs are separate from the project source code — no pollution of the analyzed repo
3. **Easy Browsing**: The `docs-site` skill provides a web UI at `~/ai/code-analysi/site/` with project cards, sidebars, and topic navigation
4. **Multi-project**: New analyses are automatically picked up when re-running `docs-site --multi`

## docs-site Integration

After analysis completes, the `docs-site` skill is automatically invoked:

1. It scans `~/ai/code-analysi/` for project directories
2. It scaffolds a TanStack Start site at `~/ai/code-analysi/site/`
3. Each project gets its own section with sidebar navigation
4. The site is deployed to Cloudflare Workers via `bun run deploy`

**Already have a site?** Running analysis on a new project and then `docs-site --multi` will automatically add the new project to the existing site.

## Implementation

```bash
# Creating directories
mkdir -p ~/ai/code-analysi/{project-name}/topics
mkdir -p ~/ai/code-analysi/{project-name}/assets

# After analysis, scaffold docs site
# (invoked automatically by the skill)
```
