# SuperClaude Framework User Guide

> **Version**: 4.1.9 | **Last Updated**: December 2025

SuperClaude is a meta-programming configuration framework that transforms Claude Code into a structured development platform through behavioral instruction injection and component orchestration.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Installation](#installation)
3. [Core Concepts](#core-concepts)
4. [Slash Commands](#slash-commands)
5. [PM Agent and Quality Patterns](#pm-agent-and-quality-patterns)
6. [MCP Server Integration](#mcp-server-integration)
7. [Workflow Patterns](#workflow-patterns)
8. [Configuration](#configuration)
9. [Best Practices](#best-practices)
10. [Troubleshooting](#troubleshooting)

---

## Getting Started

### What is SuperClaude?

SuperClaude is **not software** - it's a **behavioral configuration framework**. When you type `/sc:brainstorm`, Claude reads behavioral instructions from installed `.md` files and responds with enhanced capabilities.

### Key Components

| Component | Count | Description |
|-----------|-------|-------------|
| **Slash Commands** | 30 | Workflow automation triggers |
| **Specialized Agents** | 16 | Domain-specific AI experts |
| **Behavioral Modes** | 7 | Context adaptation patterns |
| **MCP Servers** | 8 | External tool integrations |

### How It Works

```
┌─────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  User Input     │────>│   Claude Code    │────>│  Context Files  │
│  /sc:command    │     │  Reads Context   │     │  (.md behaviors)│
└─────────────────┘     └──────────────────┘     └─────────────────┘
                               │                          │
                               ▼                          ▼
┌─────────────────┐      ┌──────────────────┐     ┌─────────────────┐
│   Enhanced      │<─────│    Behavioral    │<────│   MCP Servers   │
│   Response      │      │    Activation    │     │ (if configured) │
└─────────────────┘      └──────────────────┘     └─────────────────┘
```

---

## Installation

### Method 1: pipx (Recommended)

```bash
# Install pipx if not present
python3 -m pip install --user pipx
python3 -m pipx ensurepath

# Install SuperClaude
pipx install superclaude

# Run the installer (installs all 30 slash commands)
superclaude install

# Verify installation
superclaude install --list
superclaude doctor
```

### Method 2: pip

```bash
pip install superclaude
superclaude install
```

### Method 3: npm

```bash
npm install -g @bifrost_inc/superclaude
superclaude install
```

### Method 4: From Source

```bash
git clone https://github.com/SuperClaude-Org/SuperClaude_Framework.git
cd SuperClaude_Framework
./install.sh
```

### Post-Installation

After installation, restart Claude Code to access all commands:

```bash
# Test installation
/sc:help              # Show help
/sc                   # List all 30 commands
/sc:brainstorm "test" # Try first command
```

---

## Core Concepts

### Slash Commands

SuperClaude provides 30 slash commands with the `/sc:` namespace prefix:

```bash
/sc:brainstorm "project idea"    # Structured brainstorming
/sc:implement "feature name"     # Code implementation
/sc:analyze src/                 # Code analysis
/sc:test --coverage              # Testing workflows
```

### Specialized Agents

Agents are domain experts activated automatically based on context:

- **@agent-architect** - System architecture design
- **@agent-security** - Security analysis and auditing
- **@agent-frontend** - UI/UX development
- **@agent-backend** - API and server development
- **@agent-qa** - Quality assurance and testing

### Behavioral Modes

Modes adapt Claude's behavior to different contexts:

- **Brainstorming** - Interactive requirements discovery
- **Deep Research** - Autonomous web research
- **Orchestration** - Efficient tool coordination
- **Token-Efficiency** - 30-50% context savings
- **Task Management** - Systematic organization
- **Introspection** - Meta-cognitive analysis

---

## Slash Commands

### Planning & Design (4 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/brainstorm` | Structured brainstorming | `/sc:brainstorm "mobile app for fitness"` |
| `/design` | System architecture | `/sc:design "microservices architecture"` |
| `/estimate` | Effort estimation | `/sc:estimate "auth system"` |
| `/spec-panel` | Multi-expert analysis | `/sc:spec-panel "API design"` |

### Development (5 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/implement` | Code implementation | `/sc:implement "JWT authentication"` |
| `/build` | Build workflows | `/sc:build --target production` |
| `/improve` | Code improvements | `/sc:improve src/auth/` |
| `/cleanup` | Refactoring | `/sc:cleanup legacy-code/` |
| `/explain` | Code explanation | `/sc:explain utils.py` |

### Testing & Quality (4 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/test` | Test generation | `/sc:test --type unit auth/` |
| `/analyze` | Code analysis | `/sc:analyze --focus security` |
| `/troubleshoot` | Debugging | `/sc:troubleshoot "API 500 errors"` |
| `/reflect` | Retrospectives | `/sc:reflect session` |

### Documentation (2 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/document` | Doc generation | `/sc:document --type api` |
| `/help` | Command help | `/sc:help implement` |

### Version Control (1 command)

| Command | Description | Example |
|---------|-------------|---------|
| `/git` | Git operations | `/sc:git "feature branch"` |

### Project Management (3 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/pm` | Project management | `/sc:pm status` |
| `/task` | Task tracking | `/sc:task add "review PR"` |
| `/workflow` | Workflow automation | `/sc:workflow "CI/CD pipeline"` |

### Research & Analysis (2 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/research` | Deep web research | `/sc:research "latest AI developments 2024"` |
| `/business-panel` | Business analysis | `/sc:business-panel "market entry"` |

### Utilities (9 commands)

| Command | Description | Example |
|---------|-------------|---------|
| `/agent` | AI agents | `/sc:agent security` |
| `/index-repo` | Repository indexing | `/sc:index-repo .` |
| `/index` | Indexing alias | `/sc:index src/` |
| `/recommend` | Command recommendations | `/sc:recommend` |
| `/select-tool` | Tool selection | `/sc:select-tool` |
| `/spawn` | Parallel tasks | `/sc:spawn 3 tasks` |
| `/load` | Load sessions | `/sc:load "previous-session"` |
| `/save` | Save sessions | `/sc:save "checkpoint"` |
| `/sc` | Show all commands | `/sc` |

---

## PM Agent and Quality Patterns

The PM Agent provides intelligent quality assurance through three core patterns:

### 1. Confidence Checker (Pre-Implementation)

Prevents wrong-direction execution by assessing confidence BEFORE starting.

**Confidence Levels:**
- **High (≥90%)**: Proceed with implementation
- **Medium (70-89%)**: Present alternatives, continue investigation
- **Low (<70%)**: STOP and request clarification

**Required Checks:**
1. No duplicate implementations (check existing code first)
2. Architecture compliance (use existing tech stack)
3. Official documentation verified
4. Working OSS implementations referenced
5. Root cause identified with high certainty

**Token Budget**: 100-200 tokens
**ROI**: 25-250x token savings when stopping wrong direction

### 2. Self-Check Protocol (Post-Implementation)

Evidence-based validation after implementation:

- Verify implementation matches requirements
- Check for regressions
- Validate against official documentation
- No speculation - verify with tests/docs

### 3. Reflexion Pattern (Error Learning)

Continuous learning from mistakes:

- Immediate mistake documentation
- Root cause analysis
- Prevention checklist creation
- Cross-session pattern matching

### Using PM Agent in Tests

```python
import pytest

@pytest.mark.confidence_check
def test_feature(confidence_checker):
    """Pre-execution confidence check"""
    context = {"test_name": "test_feature", "has_official_docs": True}
    assert confidence_checker.assess(context) >= 0.7

@pytest.mark.self_check
def test_implementation(self_check_protocol):
    """Post-implementation validation"""
    implementation = {"code": "...", "tests": [...]}
    passed, issues = self_check_protocol.validate(implementation)
    assert passed, f"Validation failed: {issues}"

@pytest.mark.reflexion
def test_error_learning(reflexion_pattern):
    """Error learning and prevention"""
    pass
```

---

## MCP Server Integration

MCP (Model Context Protocol) servers extend Claude Code's capabilities. SuperClaude integrates 8 servers:

### Available Servers

| Server | Purpose | API Key Required |
|--------|---------|------------------|
| **context7** | Official library documentation | No |
| **sequential-thinking** | Multi-step reasoning | No |
| **magic** | UI component generation | Yes |
| **playwright** | Browser automation | No |
| **morphllm-fast-apply** | Code transformations | Yes |
| **serena** | Semantic code understanding | No |
| **tavily** | Web search | Yes (free tier) |
| **chrome-devtools** | Performance analysis | No |

### Installing MCP Servers

```bash
# List available MCP servers
superclaude mcp --list

# Interactive installation
superclaude mcp

# Install specific servers
superclaude mcp --servers tavily --servers context7
```

### Auto-Activation

MCP servers activate automatically based on request content:

| Request Contains | Servers Activated |
|-----------------|------------------|
| Library imports, API names | **context7** |
| `--think`, debugging | **sequential-thinking** |
| `component`, `UI`, frontend | **magic** |
| `test`, `e2e`, `browser` | **playwright** |
| Multi-file edits, refactoring | **morphllm-fast-apply** |
| Large projects, sessions | **serena** |
| `/sc:research`, `latest` | **tavily** |
| `performance`, `debug` | **chrome-devtools** |

### Configuration

MCP servers are configured in `~/.claude.json`:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    },
    "tavily": {
      "command": "npx",
      "args": ["-y", "tavily-mcp@latest"],
      "env": {"TAVILY_API_KEY": "${TAVILY_API_KEY}"}
    }
  }
}
```

### API Key Setup

```bash
# For Magic server (UI generation)
export TWENTYFIRST_API_KEY="your_key_here"

# For Morphllm server (bulk transformations)
export MORPH_API_KEY="your_key_here"

# For Tavily server (web search - free tier available)
export TAVILY_API_KEY="tvly-your_key_here"

# Add to shell profile for persistence
echo 'export TAVILY_API_KEY="your_key"' >> ~/.bashrc
```

---

## Workflow Patterns

### First Project Session

```bash
# Step 1: Discovery
/sc:brainstorm "e-commerce app"

# Step 2: Load context
/sc:load src/

# Step 3: Analysis
/sc:analyze --focus architecture

# Step 4: Planning
/sc:workflow "payment integration"

# Step 5: Implementation
/sc:implement "Stripe checkout"

# Step 6: Validation
/sc:test --coverage

# Step 7: Save session
/sc:save "payment-complete"
```

### Deep Research Workflow

```bash
# Basic research
/sc:research "latest AI developments 2024"

# Domain-filtered research
/sc:research "React patterns" --domains reactjs.org,github.com

# Research depth control
/sc:research "quantum computing" --depth exhaustive
```

**Research Depth Levels:**
| Depth | Sources | Time | Best For |
|-------|---------|------|----------|
| Quick | 5-10 | ~2min | Quick facts |
| Standard | 10-20 | ~5min | General research |
| Deep | 20-40 | ~8min | Comprehensive analysis |
| Exhaustive | 40+ | ~10min | Academic-level |

### Full-Stack Development

```bash
/sc:implement "e-commerce checkout"
# Automatically coordinates:
# → Sequential: workflow analysis
# → Context7: payment patterns
# → Magic: UI components
# → Serena: code organization
# → Playwright: E2E testing
```

### Domain-Specific Workflows

| Domain | Command | Agent | MCP Server |
|--------|---------|-------|------------|
| Frontend | UI component | @agent-frontend | Magic |
| Backend | API endpoint | @agent-backend | Sequential |
| Security | Auth implementation | @agent-security | Context7 |
| Testing | E2E scenarios | @agent-qa | Playwright |

---

## Configuration

### Project Structure

```
~/.claude/
├── settings.json        # User settings
└── commands/            # Slash commands (installed via superclaude install)
    ├── pm.md
    ├── research.md
    └── ...

project/
├── CLAUDE.md            # Project-specific instructions
├── PLANNING.md          # Architecture and design principles
├── TASK.md              # Current tasks
└── KNOWLEDGE.md         # Accumulated insights
```

### Essential Files

| File | Purpose | When to Read |
|------|---------|--------------|
| **PLANNING.md** | Architecture, design principles | Session start |
| **TASK.md** | Current tasks, priorities | Before starting work |
| **KNOWLEDGE.md** | Insights, best practices | When encountering issues |
| **CONTRIBUTING.md** | Contribution guidelines | Before submitting PRs |

### Development Commands

```bash
# Setup
make dev              # Install in editable mode

# Testing
make test             # Run full test suite
uv run pytest tests/  # Run specific tests

# Code Quality
make lint             # Run linter
make format           # Format code
make doctor           # Health check
```

---

## Best Practices

### 1. Evidence-Based Development

**Never guess** - verify with official docs before implementation:

```bash
# Good: Use Context7 for official patterns
/sc:implement "React authentication" --c7

# Bad: Implementing without verification
/sc:implement "React authentication"
```

### 2. Confidence-First Implementation

Check confidence BEFORE starting:

- **≥90%**: Proceed immediately
- **70-89%**: Present alternatives
- **<70%**: Ask questions

### 3. Parallel-First Execution

Use the **Wave → Checkpoint → Wave** pattern (3.5x faster):

```
[Read files in parallel] → Analyze → [Edit files in parallel]
```

### 4. Token Efficiency

| Task Complexity | Token Budget |
|-----------------|--------------|
| Simple (typo) | 200 tokens |
| Medium (bug fix) | 1,000 tokens |
| Complex (feature) | 2,500 tokens |

**Confidence check ROI**: Spend 100-200 tokens to save 5,000-50,000.

### 5. When to Use SuperClaude

**Use SuperClaude for:**
- Building complete software projects
- Systematic workflows with quality gates
- Complex, multi-component systems
- Long-term projects needing persistence
- Team collaboration with standards

**Use Standard Claude for:**
- Simple questions or explanations
- One-off coding tasks
- Learning programming concepts
- Quick prototypes

---

## Troubleshooting

### Common Issues

#### Command Not Found

```bash
# Check if package is installed
python3 -m pip show superclaude

# Run using Python module
python3 -m superclaude install

# Add to PATH
export PATH="$HOME/.local/bin:$PATH"
```

#### MCP Server Not Connecting

```bash
# Check Node.js version (need v16+)
node --version

# Clear npm cache
npm cache clean --force

# Test without MCP
/sc:command --no-mcp
```

#### PEP 668 Error

```bash
# Use pipx (recommended)
pipx install superclaude

# Or user installation
pip install --user superclaude

# Or virtual environment
python3 -m venv superclaude-env
source superclaude-env/bin/activate
pip install superclaude
```

### Verification Commands

```bash
# Full health check
superclaude doctor

# List installed commands
superclaude install --list

# Check MCP servers
superclaude mcp --list
```

### Getting Help

- **Documentation**: [docs.superclaude.dev](https://superclaude.netlify.app/)
- **Issues**: [GitHub Issues](https://github.com/SuperClaude-Org/SuperClaude_Framework/issues)
- **In-tool help**: `/sc:help` command

---

## Quick Reference Card

### Essential Commands

```bash
# Discovery & Planning
/sc:brainstorm "idea"        # Structured brainstorming
/sc:design "system"          # Architecture design
/sc:workflow "task"          # Workflow planning

# Development
/sc:implement "feature"      # Code implementation
/sc:improve path/            # Code improvements
/sc:test --coverage          # Testing

# Research
/sc:research "topic"         # Web research
/sc:analyze path/            # Code analysis

# Session Management
/sc:save "checkpoint"        # Save session
/sc:load "session"           # Load session
/sc                          # List all commands
```

### Command Flags

```bash
--think         # Enable sequential reasoning
--think-hard    # Enable deep analysis
--c7            # Force Context7 activation
--no-mcp        # Disable MCP servers
--all-mcp       # Enable all MCP servers
--coverage      # Include test coverage
--depth quick   # Research depth control
```

### Server Combinations

- **Free (No API Keys)**: context7 + sequential-thinking + playwright + serena
- **Learning**: context7 + sequential-thinking
- **Web Development**: magic + context7 + playwright
- **Deep Research**: tavily + sequential-thinking + serena
- **Enterprise Refactoring**: serena + morphllm + sequential-thinking

---

## Support the Project

SuperClaude is open source and maintained by the community. If you find value in it:

- **Ko-fi**: [ko-fi.com/superclaude](https://ko-fi.com/superclaude) - One-time contributions
- **Patreon**: [patreon.com/superclaude](https://patreon.com/superclaude) - Monthly support
- **GitHub Sponsors**: [github.com/sponsors/SuperClaude-Org](https://github.com/sponsors/SuperClaude-Org)

---

**License**: MIT

**Repository**: [github.com/SuperClaude-Org/SuperClaude_Framework](https://github.com/SuperClaude-Org/SuperClaude_Framework)
