# Examples Directory

This directory contains code examples for reference when implementing features with Claude Code.

## Structure

```
examples/
├── README.md          # This file
├── agent/             # Agent patterns
│   ├── agent.py       # Agent creation pattern
│   ├── providers.py   # Multi-provider LLM configuration
│   └── tools.py       # Tool implementation pattern
├── cli.py             # CLI implementation pattern
└── tests/             # Testing patterns
    ├── test_agent.py  # Unit test patterns
    └── conftest.py    # Pytest configuration
```

## Usage

These examples serve as reference patterns for:

1. **Agent Creation** - How to create and configure AI agents
2. **Tool Implementation** - How to add tools to agents
3. **CLI Structure** - How to build command-line interfaces
4. **Testing Patterns** - How to write unit tests
5. **Provider Configuration** - How to handle multiple LLM providers

## Guidelines

- Use these as **reference patterns**, not direct copies
- Follow the coding style and conventions shown
- Adapt patterns to your specific use case
- Reference these in your `INITIAL.md` when creating PRPs

## Example Usage in INITIAL.md

```markdown
## EXAMPLES:

- `examples/agent/agent.py` - Use as reference for creating your agent
- `examples/cli.py` - Use as reference for CLI structure
- `examples/tests/` - Use as reference for testing patterns
```