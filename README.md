# Ian's Claude Code Setup

My personal Claude Code configuration for productive web development. This plugin provides **14 slash commands** and **11 specialized AI agents** to supercharge your development workflow.

## Quick Install

```bash
# Step 1: Add the marketplace
/plugin marketplace add Ianboc17/Ian's-claude-code

# Step 2: Install the plugin
/plugin install Ian's-claude-code
```

## What's Inside

### 📋 Development Commands (7)

- `/new-task` - Analyze task complexity and create implementation plans
- `/code-explain` - Generate detailed code explanations
- `/code-optimize` - Optimize code for performance
- `/code-cleanup` - Clean up and refactor code
- `/feature-plan` - Plan new feature implementations
- `/lint` - Run linting and fix issues
- `/docs-generate` - Generate documentation

### 🔌 API Commands (3)

- `/api-new` - Create new API endpoint with validation and types
- `/api-test` - Test API endpoints
- `/api-protect` - Add API protection and validation

### 🎨 UI Commands (2)

- `/component-new` - Create new React component
- `/page-new` - Create new Next.js page

### 💾 Supabase Commands (2)

- `/types-gen` - Generate Supabase TypeScript types
- `/edge-function-new` - Create new Supabase Edge Function

### 🤖 Specialized AI Agents (11)

**Architecture & Planning**
- **tech-stack-researcher** - Research and recommend technology choices for features
- **system-architect** - Design scalable system architecture with maintainability focus
- **backend-architect** - Design reliable backend systems with data integrity & security
- **frontend-architect** - Create accessible, performant UI with modern frameworks
- **requirements-analyst** - Transform ambiguous ideas into concrete specifications

**Code Quality & Performance**
- **refactoring-expert** - Improve code quality through systematic refactoring
- **performance-engineer** - Optimize performance through measurement-driven analysis
- **security-engineer** - Identify vulnerabilities and ensure security compliance

**Documentation & Research**
- **technical-writer** - Create clear, comprehensive technical documentation
- **learning-guide** - Teach programming concepts with progressive learning
- **deep-research-agent** - Comprehensive research with adaptive strategies

## Installation

### From GitHub (Recommended)

```bash
# Add marketplace
/plugin marketplace add Ianboc17/Ian's-claude-code

# Install plugin
/plugin install Ian's-claude-code
```

### From Local Clone (for development)

```bash
git clone https://github.com/Ianboc17/Ian's-claude-code.git
cd Ian's-claude-code

# Add as local marketplace
/plugin marketplace add /path/to/Ian's-claude-code

# Install plugin
/plugin install Ian's-claude-code
```

## Best For

- Next.js developers
- TypeScript projects
- Supabase users
- React developers
- Full-stack engineers

## Usage Examples

### Planning a Feature

```bash
/feature-plan
# Then describe your feature idea
```

### Creating an API

```bash
/api-new
# Scaffolds a complete API route with types, validation, and error handling
```

### Research Tech Choices

Ask Claude questions like:
- "Should I use WebSockets or SSE?"
- "How should I structure this database?"
- "What's the best library for X?"

The **tech-stack-researcher** agent activates automatically and provides detailed recommendations.

## Philosophy

This setup emphasizes:
- **Type Safety**: Never uses `any` types
- **Best Practices**: Follows modern Next.js/React patterns
- **Productivity**: Reduces repetitive scaffolding
- **Research**: AI-powered tech decisions with evidence

## Requirements

- Claude Code 2.0.13+
- Works with any project (optimized for Next.js + Supabase)

## Customization

After installation, you can customize any command by editing files in `.claude/commands/` and `.claude/agents/`.

## Contributing

Feel free to:
- Fork and customize for your needs
- Submit issues or suggestions
- Share your improvements

## License

MIT - Use freely in your projects

## Author

Created by Ian

GitHub: [Ianboc17](https://github.com/Ianboc17)

---

**Note**: This is my personal setup refined over time. Commands are optimized for Next.js + Supabase workflows but work great with any modern web stack.
