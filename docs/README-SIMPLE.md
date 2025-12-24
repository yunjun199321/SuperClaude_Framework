# SuperClaude Framework

> Transform Claude Code into a Structured Development Platform

**Version**: 4.1.9 | **License**: MIT | **Python**: >=3.10

## What is SuperClaude?

SuperClaude is a **meta-programming configuration framework** that enhances Claude Code through:

- **30 Slash Commands** - Complete development lifecycle automation
- **16 Specialized Agents** - Domain-specific AI experts
- **7 Behavioral Modes** - Context-adaptive responses
- **8 MCP Servers** - External tool integrations

## Quick Start

```bash
# Install
pipx install superclaude
superclaude install

# Verify
superclaude doctor

# Optional: Install MCP servers for enhanced performance
superclaude mcp --servers tavily context7
```

After installation, restart Claude Code and try:

```bash
/sc:brainstorm "project idea"    # Structured brainstorming
/sc:implement "feature"          # Code implementation
/sc:research "topic"             # Deep web research
/sc                              # List all 30 commands
```

## Core Commands

| Category | Commands |
|----------|----------|
| **Planning** | `/brainstorm`, `/design`, `/estimate`, `/spec-panel` |
| **Development** | `/implement`, `/build`, `/improve`, `/cleanup`, `/explain` |
| **Testing** | `/test`, `/analyze`, `/troubleshoot`, `/reflect` |
| **Research** | `/research`, `/business-panel` |
| **Management** | `/pm`, `/task`, `/workflow`, `/git` |
| **Utilities** | `/load`, `/save`, `/index-repo`, `/spawn`, `/sc` |

## MCP Servers

| Server | Purpose | API Key |
|--------|---------|---------|
| **context7** | Official documentation | No |
| **sequential-thinking** | Multi-step reasoning | No |
| **tavily** | Web search | Yes (free tier) |
| **playwright** | Browser automation | No |
| **serena** | Code understanding | No |
| **magic** | UI components | Yes |
| **morphllm** | Code transformations | Yes |
| **chrome-devtools** | Performance | No |

## PM Agent Quality Patterns

SuperClaude includes intelligent quality assurance:

- **Confidence Checker**: Assess before implementation (>=90% proceed, <70% stop)
- **Self-Check Protocol**: Evidence-based validation
- **Reflexion Pattern**: Learn from mistakes

## Project Structure

```
~/.claude/commands/     # Slash commands (installed via superclaude install)
project/CLAUDE.md       # Project-specific instructions
project/PLANNING.md     # Architecture and design
project/TASK.md         # Current tasks
```

## Development

```bash
# Clone and setup
git clone https://github.com/SuperClaude-Org/SuperClaude_Framework.git
cd SuperClaude_Framework
make dev

# Run tests
make test

# Health check
make doctor
```

## Documentation

- [Quick Start Guide](docs/getting-started/quick-start.md)
- [Installation Guide](docs/getting-started/installation.md)
- [Commands Reference](docs/reference/commands-list.md)
- [MCP Servers Guide](docs/user-guide/mcp-servers.md)
- [User Guide](docs/user-guide/USER_GUIDE.md)

## Links

- **Website**: [superclaude.netlify.app](https://superclaude.netlify.app/)
- **PyPI**: [pypi.org/project/superclaude](https://pypi.org/project/superclaude/)
- **npm**: [@bifrost_inc/superclaude](https://www.npmjs.com/package/@bifrost_inc/superclaude)
- **Issues**: [GitHub Issues](https://github.com/SuperClaude-Org/SuperClaude_Framework/issues)

## Support

- [Ko-fi](https://ko-fi.com/superclaude) - One-time contributions
- [Patreon](https://patreon.com/superclaude) - Monthly support
- [GitHub Sponsors](https://github.com/sponsors/SuperClaude-Org) - Flexible tiers

## Disclaimer

This project is not affiliated with or endorsed by Anthropic. Claude Code is a product built and maintained by [Anthropic](https://www.anthropic.com/).

---

**Made with care by the SuperClaude community**
