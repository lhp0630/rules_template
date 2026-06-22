# AI Rules Template

A comprehensive rules template for AI coding assistants, supporting **Cursor AI** and **Claude Code** with Context Engineering.

## Overview

This template provides a structured framework for AI-assisted development based on software engineering best practices and documentation-driven development. It helps AI coding assistants understand project context, follow conventions, and maintain code quality.

## Features

- **Cursor AI Support**: `.cursor/rules/` directory with `.mdc` files for on-demand loading
- **Claude Code Support**: Context Engineering workflow with PRP (Product Requirements Prompts)
- **Memory Bank**: Persistent documentation system in `docs/` and `tasks/`
- **Agile Workflow**: Built on software engineering principles and best practices
- **Auto-Documentation**: Automatically updates documentation after changes

## Quick Start

### Cursor AI

1. Copy `.cursor/rules/` to your project root
2. Start coding with Cursor AI

### Claude Code

1. Copy `.claude/` directory and `CLAUDE.md` to your project root
2. Install Claude Code from [Anthropic](https://docs.anthropic.com/en/docs/claude-code)
3. Use PRP workflow:
   - Write requirements in `INITIAL.md`
   - Run `/generate-prp INITIAL.md`
   - Run `/execute-prp PRPs/your-feature-name.md`

## Directory Structure

```
project/
├── .cursor/rules/      # Cursor AI rules
├── .claude/            # Claude Code config
├── CLAUDE.md           # Claude Code global rules
├── AGENTS.md           # MiMoCode rules
├── MEMORY.md           # Memory documentation system
├── docs/               # Documentation
│   ├── architecture.md
│   ├── technical.md
│   └── product_requirement_docs.md
├── tasks/              # Task management (general project tasks)
│   ├── active_context.md
│   ├── tasks_plan.md
│   └── changelog.md
├── PRPs/               # Product Requirements Prompts (Claude Code workflow)
│   ├── templates/
│   │   └── prp_base.md
│   └── EXAMPLE_multi_agent_prp.md
├── examples/           # Code examples
└── src/                # Source code
```

### tasks/ vs PRPs/

- **tasks/**: General project task management for all AI assistants
  - `active_context.md`: Current development context and focus
  - `tasks_plan.md`: Task backlog and project progress
  - `changelog.md`: Change history and documentation

- **PRPs/**: Claude Code-specific Product Requirements Prompts
  - `templates/prp_base.md`: PRP template with validation loops
  - `EXAMPLE_multi_agent_prp.md`: Complete PRP example
  - Used with `/generate-prp` and `/execute-prp` commands

## Rule Files

### Cursor AI

```
.cursor/rules/
├── rules.mdc           # Core rules
├── plan.mdc            # Planning workflow
├── implement.mdc       # Implementation workflow
├── debug.mdc           # Debugging workflow
├── memory.mdc          # Documentation system
└── directory-structure.mdc
```

### Memory System

`MEMORY.md` provides a comprehensive documentation system for persistent project memory:

- **Core Files** (required): Product requirements, architecture, technical specs, task plans, active context, error documentation, lessons learned
- **Context Files** (optional): Literature surveys, RFCs
- **Workflow**: PLAN/ACT modes for reading and writing memory files
- **Auto-Updates**: Documentation automatically updated after changes

### Claude Code

```
.claude/
├── commands/
│   ├── generate-prp.md
│   └── execute-prp.md
└── settings.local.json
```

## Core Principles

1. **Context Engineering**: Provide comprehensive context for AI assistants
2. **Validation Loops**: Self-correcting workflows with executable tests
3. **Documentation-Driven**: Persistent memory through structured documentation
4. **Modular Design**: Separation of concerns and incremental development

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Acknowledgments

This project is inspired by and references:
- [rules_template](https://github.com/Bhartendu-Kumar/rules_template) by Bhartendu Kumar
- [context-engineering-intro](https://github.com/coleam00/context-engineering-intro) by Cole McMahan

## License

MIT