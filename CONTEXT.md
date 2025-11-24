# Context Memory - Ian's Claude Code Plugin

**Last Updated**: 2025-11-24
**Status**: Debugging installation issues

---

## Project Overview

This is **Ian's Claude Code Plugin** - a comprehensive plugin for Claude Code with:
- **14 slash commands** organized in 4 categories (API, UI, Misc, Supabase)
- **11 specialized AI agents** (architects, engineers, writers, guides)
- **3 MCP servers** (context7, playwright, supabase)

**Plugin Name**: `ians-claude-code`
**Version**: 1.0.0
**Location**: `X:\GIT\Ians-plugin`
**GitHub**: https://github.com/Ianboc17/ians-claude-code

---

## Current Issue: Plugin Installation Failed

### Problem
- User tried to install the plugin but got error: "1 plugin failed to install"
- When using `/plugin manage`, no plugins appear (this is normal if no plugins are installed)
- Need to debug why installation is failing

### Root Cause Analysis
The most likely issue is the **folder name contains a space and apostrophe**: `Ian's Plugin`

This can cause problems with:
- Path parsing in Claude Code
- Marketplace resolution
- File system operations on Windows

### What We've Done
1. ✅ Verified `plugin.json` - valid JSON with correct structure
2. ✅ Verified `marketplace.json` - valid JSON format
3. ✅ Confirmed all 14 command files exist
4. ✅ Confirmed all 11 agent files exist
5. ✅ Fixed description mismatch in `new-task` command in `plugin.json:11`

---

## File Structure

```
X:\GIT\Ian's Plugin\
├── .claude/
│   ├── agents/                    (11 agents)
│   │   ├── backend-architect.md
│   │   ├── deep-research-agent.md
│   │   ├── frontend-architect.md
│   │   ├── learning-guide.md
│   │   ├── performance-engineer.md
│   │   ├── refactoring-expert.md
│   │   ├── requirements-analyst.md
│   │   ├── security-engineer.md
│   │   ├── system-architect.md
│   │   ├── tech-stack-researcher.md
│   │   └── technical-writer.md
│   │
│   ├── commands/
│   │   ├── api/                   (3 commands)
│   │   │   ├── api-new.md
│   │   │   ├── api-protect.md
│   │   │   └── api-test.md
│   │   ├── misc/                  (6 commands)
│   │   │   ├── code-cleanup.md
│   │   │   ├── code-explain.md
│   │   │   ├── code-optimize.md
│   │   │   ├── docs-generate.md
│   │   │   ├── feature-plan.md
│   │   │   └── lint.md
│   │   ├── supabase/              (2 commands)
│   │   │   ├── edge-function-new.md
│   │   │   └── types-gen.md
│   │   ├── ui/                    (2 commands)
│   │   │   ├── component-new.md
│   │   │   └── page-new.md
│   │   └── new-task.md            (1 root command)
│   │
│   ├── settings.local.json
│   └── settings.template.json
│
├── .claude-plugin/
│   ├── marketplace.json           ✅ Valid
│   ├── plugin.json                ✅ Valid (description fixed)
│   └── MCP-SERVERS.md
│
├── .git/
├── .gitignore
├── README.md
└── CONTEXT.md                     (this file)
```

---

## Commands Available

### Development (7)
1. `/new-task` - Analyze task complexity and create implementation plans
2. `/code-explain` - Generate detailed code explanations
3. `/code-optimize` - Optimize code for performance
4. `/code-cleanup` - Clean up and refactor code
5. `/feature-plan` - Plan new feature implementations
6. `/lint` - Run linting and fix issues
7. `/docs-generate` - Generate documentation

### API (3)
8. `/api-new` - Create new API endpoint with validation and types
9. `/api-test` - Test API endpoints
10. `/api-protect` - Add API protection and validation

### UI (2)
11. `/component-new` - Create new React component
12. `/page-new` - Create new Next.js page

### Supabase (2)
13. `/types-gen` - Generate Supabase TypeScript types
14. `/edge-function-new` - Create new Supabase Edge Function

---

## Agents Available (11)

### Architecture & Planning
1. **tech-stack-researcher** - Research technology choices
2. **system-architect** - Design scalable systems
3. **backend-architect** - Design backend systems
4. **frontend-architect** - Create accessible UI
5. **requirements-analyst** - Transform ideas into specs

### Code Quality & Performance
6. **refactoring-expert** - Improve code quality
7. **performance-engineer** - Optimize performance
8. **security-engineer** - Identify vulnerabilities

### Documentation & Research
9. **technical-writer** - Create documentation
10. **learning-guide** - Teach programming concepts
11. **deep-research-agent** - Comprehensive research

---

## MCP Servers (3)

1. **context7** - Access up-to-date documentation for any library
2. **playwright** - Browser automation and web testing
3. **supabase** - Supabase database operations

---

## Next Steps to Fix Installation

### Recommended Solution: Rename Folder

**Problem**: Folder name `Ian's Plugin` has space and apostrophe
**Solution**: Rename to `ians-plugin`

```bash
# In Windows Terminal (cmd or PowerShell):
cd X:\GIT
ren "Ian's Plugin" ians-plugin

# Then in Claude Code:
/plugin marketplace add X:\GIT\ians-plugin
/plugin install ians-claude-code
/plugin list
```

### Alternative Solutions

1. **Try with quotes**:
   ```bash
   /plugin marketplace add "X:\GIT\Ian's Plugin"
   /plugin install ians-claude-code
   ```

2. **Remove and re-add marketplace**:
   ```bash
   /plugin marketplace list
   /plugin marketplace remove "X:\GIT\Ian's Plugin"
   /plugin marketplace add "X:\GIT\Ian's Plugin"
   /plugin install ians-claude-code
   ```

3. **Check specific error**:
   ```bash
   /plugin
   ```
   This will show the detailed error message

4. **Restart Claude Code** after making changes

---

## GitHub Repository

**Repository URL**: https://github.com/Ianboc17/ians-claude-code
**Status**: Repository created, ready to push

### To Publish to GitHub:

1. ✅ Create repo: `Ianboc17/ians-claude-code` (DONE)
2. Push all files to `main` branch
3. Make repo public
4. Install via GitHub:
   ```bash
   /plugin marketplace add Ianboc17/ians-claude-code
   /plugin install ians-claude-code
   ```

---

## Git Status

```
Current branch: main
Status: clean

Recent commits:
- fa0f0a2 Fix: Remove apostrophe from plugin name for compatibility
- ed11d49 Fix: Align plugin name in marketplace.json
- 1f4eca2 Initial commit: Ian's Claude Code plugin with 14 commands and 11 agents
```

---

## Key Configuration Files

### plugin.json
- Location: `.claude-plugin/plugin.json`
- Status: ✅ Valid JSON
- Last modified: Fixed `new-task` description (line 11)
- Contains: 14 commands, 11 agents, 3 MCP servers, 8 tags

### marketplace.json
- Location: `.claude-plugin/marketplace.json`
- Status: ✅ Valid JSON
- Owner: Ian (github.com/Ianboc17)
- Plugin source: `./` (local directory)

---

## Important Notes

1. **Folder Name Issue**: The apostrophe and space in `Ian's Plugin` is likely causing the installation failure
2. **All Files Valid**: All command/agent markdown files exist and are properly formatted
3. **JSON Valid**: Both plugin.json and marketplace.json are syntactically correct
4. **Next Action**: Rename folder to remove special characters

---

## Quick Reference Commands

```bash
# Check plugin status
/plugin
/plugin list

# Marketplace management
/plugin marketplace list
/plugin marketplace add <path-or-github-repo>
/plugin marketplace remove <name>

# Plugin management
/plugin install <plugin-name>
/plugin uninstall <plugin-name>
/plugin manage

# Use commands (after installation)
/new-task <description>
/api-new <endpoint-name>
/component-new <component-name>
```

---

## To Resume Next Session

1. Read this file: `X:\GIT\Ian's Plugin\CONTEXT.md`
2. Check if user renamed folder to fix installation
3. Verify plugin installation status: `/plugin list`
4. If still failing, check error details: `/plugin`
5. Continue troubleshooting or move to GitHub publishing

---

**End of Context Memory**
