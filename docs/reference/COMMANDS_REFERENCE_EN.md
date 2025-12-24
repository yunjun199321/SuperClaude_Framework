# SuperClaude Framework - Command Reference

> **Version**: 4.1.9 | **Total Commands**: 30 | **Last Updated**: December 2025

This document is the complete command reference manual for SuperClaude Framework, containing detailed descriptions, parameters, usage examples, and best practices for all 30 slash commands.

---

## Table of Contents

1. [Command Overview](#command-overview)
2. [Planning & Requirements (4)](#planning--requirements)
3. [Development (5)](#development)
4. [Testing & Quality (4)](#testing--quality)
5. [Documentation (3)](#documentation)
6. [Research & Analysis (3)](#research--analysis)
7. [Project Management (5)](#project-management)
8. [Session Management (3)](#session-management)
9. [Utilities (3)](#utilities)
10. [MCP Server Integration](#mcp-server-integration)
11. [Best Practices](#best-practices)

---

## Command Overview

### Quick Reference Table

| Category | Commands | Count |
|----------|----------|-------|
| Planning & Requirements | brainstorm, design, estimate, workflow | 4 |
| Development | implement, build, improve, cleanup, git | 5 |
| Testing & Quality | test, analyze, troubleshoot, reflect | 4 |
| Documentation | document, explain, index | 3 |
| Research & Analysis | research, business-panel, spec-panel | 3 |
| Project Management | pm, task, spawn, select-tool, index-repo | 5 |
| Session Management | load, save, agent | 3 |
| Utilities | help, recommend, sc | 3 |

### Command Namespace

All commands use the `/sc:` namespace prefix:

```bash
/sc:brainstorm "project idea"    # Structured brainstorming
/sc:implement "feature name"     # Code implementation
/sc:research "topic"             # Deep research
/sc:test --coverage              # Test execution
```

---

## Planning & Requirements

### /sc:brainstorm

**Description**: Interactive requirements discovery through Socratic dialogue and systematic exploration

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:brainstorm [options] "[topic/idea]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | systematic, agile, enterprise | Exploration strategy selection |
| `--depth` | shallow, normal, deep | Analysis depth |
| `--parallel` | - | Enable parallel exploration paths |

**MCP Servers**: sequential, context7, magic, playwright, morphllm, serena

**Personas**: architect, analyzer, frontend, backend, security, devops, project-manager

**Behavioral Flow**:
1. **Explore**: Transform vague ideas through Socratic dialogue
2. **Analyze**: Coordinate multiple personas for domain expert analysis
3. **Validate**: Apply feasibility assessment and requirements validation
4. **Specify**: Generate concrete specifications
5. **Handoff**: Create actionable implementation briefs

**Examples**:

Systematic product discovery (deep analysis)
```bash
/sc:brainstorm --strategy systematic --depth deep "AI-powered project management tool"
```
---
Agile feature exploration (parallel paths)
```bash
/sc:brainstorm --strategy agile --parallel "real-time collaboration features"
```
---
Enterprise solution validation
```bash
/sc:brainstorm --strategy enterprise "enterprise data analytics platform"
```
---
Quick shallow exploration
```bash
/sc:brainstorm --depth shallow "mobile app idea"
```
---
Systematic parallel deep exploration
```bash
/sc:brainstorm --strategy systematic --depth deep --parallel "microservices architecture"
```
---
Agile iterative exploration
```bash
/sc:brainstorm --strategy agile --depth normal "user authentication improvements"
```

**Boundaries**:
- **Will**: Transform vague ideas into concrete specifications, coordinate multiple personas and MCP servers
- **Will Not**: Make implementation decisions during exploration phase without proper requirements discovery

---

### /sc:design

**Description**: Design system architecture, APIs, and component interfaces with comprehensive specifications

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:design [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | architecture, api, component, database | Design type |
| `--format` | diagram, spec, code | Output format |

**Behavioral Flow**:
1. **Analyze**: Examine target requirements and existing system context
2. **Plan**: Define design approach based on type and format
3. **Design**: Create comprehensive specifications following industry best practices
4. **Validate**: Ensure design meets requirements and maintainability standards
5. **Document**: Generate clear design documentation

**Examples**:

System architecture design
```bash
/sc:design --type architecture --format diagram user-management-system
```
---
API specification design
```bash
/sc:design --type api --format spec payment-api
```
---
Component interface design
```bash
/sc:design --type component --format code notification-service
```
---
Database schema design
```bash
/sc:design --type database --format diagram e-commerce-db
```

---

### /sc:estimate

**Description**: Provide intelligent development estimates for tasks, features, or projects

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:estimate [options] "[target]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | time, effort, complexity | Estimation type |
| `--unit` | hours, days, weeks | Time unit |
| `--breakdown` | - | Enable detailed breakdown |

**Examples**:

Time estimation
```bash
/sc:estimate --type time --unit days "authentication system"
```
---
Complexity analysis
```bash
/sc:estimate --type complexity --breakdown "API refactoring"
```

---

### /sc:workflow

**Description**: Generate structured implementation workflows from PRDs and feature requirements

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:workflow [options] "[feature-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | systematic, agile, enterprise | Workflow strategy |
| `--depth` | shallow, normal, deep | Workflow depth |
| `--parallel` | - | Enable parallel execution |

**Examples**:

Systematic workflow
```bash
/sc:workflow --strategy systematic "payment integration"
```
---
Agile iterative workflow
```bash
/sc:workflow --strategy agile --depth deep "user onboarding"
```

---

## Development

### /sc:implement

**Description**: Feature and code implementation with intelligent persona activation and MCP integration

**Category**: workflow | **Complexity**: standard

**Syntax**:
```bash
/sc:implement [options] "[feature-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | component, api, service, feature | Implementation type |
| `--framework` | react, vue, express, etc. | Framework selection |
| `--safe` | - | Enable safe mode |
| `--with-tests` | - | Include test generation |

**MCP Servers**: context7, sequential, magic, playwright

**Personas**: architect, frontend, backend, security, qa-specialist

**Behavioral Flow**:
1. **Analyze**: Examine implementation requirements, detect technical context
2. **Plan**: Select approach, activate relevant personas
3. **Generate**: Create code using framework-specific best practices
4. **Validate**: Apply security and quality validation
5. **Integrate**: Update documentation, provide test suggestions

**Examples**:

React component implementation
```bash
/sc:implement --type component --framework react "user profile component"
```
---
API service implementation (safe mode + tests)
```bash
/sc:implement --type api --safe --with-tests "user authentication API"
```
---
Full-stack feature
```bash
/sc:implement --type feature --with-tests "payment processing system"
```
---
Vue framework component
```bash
/sc:implement --type component --framework vue "dashboard widget"
```
---
Express backend service
```bash
/sc:implement --type service --framework express --safe "file upload service"
```
---
React secure component (with tests)
```bash
/sc:implement --type component --framework react --safe --with-tests "admin panel"
```
---
Next.js page implementation
```bash
/sc:implement --type feature --framework nextjs "user settings page"
```
---
Pure API implementation (no tests)
```bash
/sc:implement --type api "notification endpoint"
```

---

### /sc:build

**Description**: Build, compile, and package projects with intelligent error handling and optimization

**Category**: utility | **Complexity**: enhanced

**Syntax**:
```bash
/sc:build [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | dev, prod, test | Build type |
| `--clean` | - | Clean build |
| `--optimize` | - | Enable optimization |
| `--verbose` | - | Verbose output |

**Examples**:

Development build
```bash
/sc:build --type dev
```
---
Production build
```bash
/sc:build --type prod --clean --optimize
```
---
Verbose build
```bash
/sc:build --verbose
```

---

### /sc:improve

**Description**: Apply systematic improvements to code quality, performance, and maintainability

**Category**: workflow | **Complexity**: standard

**Syntax**:
```bash
/sc:improve [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | quality, performance, maintainability, style | Improvement type |
| `--safe` | - | Safe mode (conservative improvements) |
| `--interactive` | - | Interactive improvement |
| `--preview` | - | Preview mode (show changes) |
| `--validate` | - | Enable validation |

**MCP Servers**: sequential, context7

**Personas**: architect, performance, quality, security

**Examples**:

Quality improvement
```bash
/sc:improve --type quality src/auth
```
---
Performance optimization (safe mode)
```bash
/sc:improve --type performance --safe api/
```
---
Interactive style improvement
```bash
/sc:improve --type style --interactive components/
```
---
Maintainability improvement (preview)
```bash
/sc:improve --type maintainability --preview src/utils
```
---
Quality improvement (validate + interactive)
```bash
/sc:improve --type quality --validate --interactive src/services
```
---
Safe performance optimization (preview)
```bash
/sc:improve --type performance --safe --preview database/
```
---
Comprehensive quality review
```bash
/sc:improve --type quality --validate --safe src/
```
---
Style unification (safe + preview)
```bash
/sc:improve --type style --safe --preview --validate components/
```

---

### /sc:cleanup

**Description**: Systematically clean up code, remove dead code, and optimize project structure

**Category**: workflow | **Complexity**: standard

**Syntax**:
```bash
/sc:cleanup [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | code, imports, files, all | Cleanup type |
| `--safe` | - | Safe mode (conservative cleanup) |
| `--aggressive` | - | Aggressive mode (thorough cleanup) |
| `--interactive` | - | Interactive cleanup |
| `--preview` | - | Preview mode (show changes) |

**MCP Servers**: sequential, context7

**Personas**: architect, quality, security

**Examples**:

Safe code cleanup
```bash
/sc:cleanup --type code --safe src/
```
---
Import cleanup
```bash
/sc:cleanup --type imports
```
---
Comprehensive interactive cleanup
```bash
/sc:cleanup --type all --interactive
```
---
Aggressive file cleanup (preview)
```bash
/sc:cleanup --type files --aggressive --preview
```
---
Safe code cleanup (preview)
```bash
/sc:cleanup --type code --safe --preview src/legacy
```
---
Interactive import cleanup
```bash
/sc:cleanup --type imports --interactive
```
---
Comprehensive aggressive cleanup
```bash
/sc:cleanup --type all --aggressive
```
---
Safe comprehensive cleanup (preview + interactive)
```bash
/sc:cleanup --type all --safe --preview --interactive
```

---

### /sc:git

**Description**: Git operations with intelligent commit messages and workflow optimization

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:git [options] "[operation]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--smart-commit` | - | Smart commit message generation |
| `--interactive` | - | Interactive Git operations |

**Examples**:

Smart commit
```bash
/sc:git --smart-commit
```
---
Create feature branch
```bash
/sc:git "feature/user-auth"
```
---
Interactive operations
```bash
/sc:git --interactive
```

---

## Testing & Quality

### /sc:test

**Description**: Execute tests with coverage analysis and automated quality reporting

**Category**: utility | **Complexity**: enhanced

**Syntax**:
```bash
/sc:test [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | unit, integration, e2e, all | Test type |
| `--coverage` | - | Enable coverage analysis |
| `--watch` | - | Watch mode |
| `--fix` | - | Auto-fix simple failures |

**MCP Servers**: playwright (for e2e)

**Personas**: qa-specialist

**Behavioral Flow**:
1. **Discover**: Categorize available tests using runner patterns
2. **Configure**: Set up test environment and execution parameters
3. **Execute**: Run tests with real-time monitoring
4. **Analyze**: Generate coverage reports and failure diagnostics
5. **Report**: Provide actionable recommendations and quality metrics

**Examples**:

Basic test execution
```bash
/sc:test
```
---
Unit test coverage analysis
```bash
/sc:test --type unit --coverage src/components
```
---
End-to-end browser testing
```bash
/sc:test --type e2e
```
---
Development watch mode (auto-fix)
```bash
/sc:test --watch --fix
```
---
Integration testing
```bash
/sc:test --type integration
```
---
Comprehensive testing (with coverage)
```bash
/sc:test --type all --coverage
```
---
Unit test watch mode
```bash
/sc:test --type unit --watch
```
---
E2E testing (auto-fix)
```bash
/sc:test --type e2e --fix
```
---
Coverage watch mode
```bash
/sc:test --coverage --watch
```

---

### /sc:analyze

**Description**: Comprehensive code analysis across quality, security, performance, and architecture domains

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:analyze [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--focus` | quality, security, performance, architecture | Analysis focus |
| `--depth` | quick, deep | Analysis depth |
| `--format` | text, json, report | Output format |

**Behavioral Flow**:
1. **Discover**: Categorize source files using language detection and project analysis
2. **Scan**: Apply domain-specific analysis techniques
3. **Evaluate**: Generate prioritized findings with severity ratings
4. **Recommend**: Create actionable recommendations
5. **Report**: Present comprehensive analysis report

**Examples**:

Comprehensive project analysis
```bash
/sc:analyze
```
---
Focused security assessment (deep)
```bash
/sc:analyze --focus security --depth deep src/auth
```
---
Performance optimization analysis (report format)
```bash
/sc:analyze --focus performance --format report
```
---
Quick quality check
```bash
/sc:analyze --focus quality --depth quick src/components
```
---
Architecture deep analysis (JSON output)
```bash
/sc:analyze --focus architecture --depth deep --format json
```
---
Security quick scan
```bash
/sc:analyze --focus security --depth quick
```
---
Performance deep analysis
```bash
/sc:analyze --focus performance --depth deep api/
```
---
Quality report (deep)
```bash
/sc:analyze --focus quality --depth deep --format report src/
```

---

### /sc:troubleshoot

**Description**: Diagnose and resolve issues in code, builds, deployments, and system behavior

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:troubleshoot [options] "[issue-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | bug, build, performance, deployment | Issue type |
| `--trace` | - | Enable tracing |
| `--fix` | - | Auto-fix |

**Examples**:

Bug diagnosis
```bash
/sc:troubleshoot --type bug "login form not submitting"
```
---
Build issues
```bash
/sc:troubleshoot --type build --trace "build failing on CI"
```
---
Performance issues
```bash
/sc:troubleshoot --type performance --fix "API response slow"
```

---

### /sc:reflect

**Description**: Task reflection and validation using Serena MCP analysis capabilities

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:reflect [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | task, session, completion | Reflection type |
| `--analyze` | - | Enable deep analysis |
| `--validate` | - | Enable validation |

**Examples**:

Task reflection
```bash
/sc:reflect --type task --analyze
```
---
Session review
```bash
/sc:reflect --type session
```
---
Completion validation
```bash
/sc:reflect --type completion --validate
```

---

## Documentation

### /sc:document

**Description**: Generate focused documentation for components, functions, APIs, and features

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:document [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | inline, external, api, guide | Documentation type |
| `--style` | brief, detailed | Documentation style |

**Examples**:

Inline documentation
```bash
/sc:document --type inline src/utils.ts
```
---
API documentation
```bash
/sc:document --type api --style detailed api/
```
---
User guide
```bash
/sc:document --type guide --style brief
```

---

### /sc:explain

**Description**: Provide clear explanations of code, concepts, and system behavior

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:explain [options] "[target]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--level` | basic, intermediate, advanced | Explanation level |
| `--format` | text, examples, interactive | Explanation format |
| `--context` | [domain] | Context domain |

**Examples**:

Basic explanation
```bash
/sc:explain --level basic src/auth/middleware.ts
```
---
Advanced detailed explanation
```bash
/sc:explain --level advanced --format examples "JWT authentication flow"
```
---
Interactive explanation
```bash
/sc:explain --format interactive "database optimization"
```

---

### /sc:index

**Description**: Generate comprehensive project documentation and knowledge base

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:index [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | docs, api, structure, readme | Index type |
| `--format` | md, json, yaml | Output format |

**Examples**:

Documentation index
```bash
/sc:index --type docs
```
---
API index
```bash
/sc:index --type api --format json api/
```
---
Project structure index
```bash
/sc:index --type structure --format yaml
```

---

## Research & Analysis

### /sc:research

**Description**: Deep web research with adaptive planning and intelligent search

**Category**: command | **Complexity**: advanced

**Syntax**:
```bash
/sc:research [options] "[query]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--depth` | quick, standard, deep, exhaustive | Research depth |
| `--strategy` | planning, intent, unified | Planning strategy |

**MCP Servers**: tavily, sequential, playwright, serena

**Personas**: deep-research-agent

**Research Depth Levels**:
| Depth | Sources | Hops | Time | Best For |
|-------|---------|------|------|----------|
| Quick | 5-10 | 1 | ~2min | Quick fact queries |
| Standard | 10-20 | 2-3 | ~5min | General research (default) |
| Deep | 20-40 | 3-4 | ~8min | Comprehensive analysis |
| Exhaustive | 40+ | 5 | ~10min | Academic-level research |

**Behavioral Flow**:
1. **Understand** (5-10%): Assess query complexity and ambiguity
2. **Plan** (10-15%): Select planning strategy, identify parallel opportunities
3. **TodoWrite** (5%): Create adaptive task hierarchy
4. **Execute** (50-60%): Parallel search, intelligent extraction, multi-hop exploration
5. **Track** (ongoing): Monitor progress, update confidence
6. **Validate** (10-15%): Verify evidence chain, check source credibility

**Examples**:

Basic research (default depth)
```bash
/sc:research "latest developments in quantum computing 2024"
```
---
Deep competitive analysis
```bash
/sc:research --depth deep "competitive analysis of AI coding assistants"
```
---
Unified strategy research
```bash
/sc:research --strategy unified "best practices for distributed systems"
```
---
Quick fact query
```bash
/sc:research --depth quick "current React version"
```
---
Academic-level deep research
```bash
/sc:research --depth exhaustive "machine learning optimization techniques"
```
---
Intent planning research
```bash
/sc:research --strategy intent "cloud architecture patterns"
```
---
Deep + planning combination
```bash
/sc:research --depth deep --strategy planning "microservices security best practices"
```
---
Standard research (explicit)
```bash
/sc:research --depth standard "database scaling strategies"
```

**Output**: Reports saved to `claudedocs/research_[topic]_[timestamp].md`

---

### /sc:business-panel

**Description**: Multi-expert business strategy analysis with 9 renowned business thinkers

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:business-panel [options] "[topic]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--mode` | discussion, debate, socratic | Analysis mode |
| `--experts` | [name1,name2,...] | Expert selection |

**Available Experts**:
- Christensen (Disruptive Innovation)
- Porter (Competitive Strategy)
- Drucker (Management)
- Godin (Marketing)
- Kim & Mauborgne (Blue Ocean Strategy)
- Collins (Excellence)
- Taleb (Risk)
- Meadows (Systems Thinking)
- Doumont (Communication)

**Examples**:

Market entry strategy analysis
```bash
/sc:business-panel --mode discussion "market entry strategy"
```
---
Debate mode
```bash
/sc:business-panel --mode debate --experts porter,godin "pricing strategy"
```
---
Socratic exploration
```bash
/sc:business-panel --mode socratic "digital transformation"
```

---

### /sc:spec-panel

**Description**: Multi-expert specification review and improvement with renowned software engineering experts

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:spec-panel [options] "[specification]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--mode` | discussion, critique, socratic | Review mode |
| `--experts` | [name1,name2,...] | Expert selection |
| `--focus` | requirements, architecture, testing, compliance | Review focus |
| `--iterations` | [N] | Number of iterations |
| `--format` | standard, structured, detailed | Output format |

**Examples**:

Requirements specification review
```bash
/sc:spec-panel --focus requirements "API specification"
```
---
Architecture critique mode
```bash
/sc:spec-panel --mode critique --focus architecture "microservices design"
```
---
Detailed iterative review
```bash
/sc:spec-panel --iterations 3 --format detailed "security policy"
```
---
Socratic testing review
```bash
/sc:spec-panel --mode socratic --focus testing "test coverage strategy"
```
---
Compliance discussion review
```bash
/sc:spec-panel --mode discussion --focus compliance "GDPR requirements"
```
---
Expert-specific architecture review
```bash
/sc:spec-panel --experts fowler,beck --focus architecture "domain-driven design"
```
---
Multi-round structured requirements review
```bash
/sc:spec-panel --iterations 5 --format structured --focus requirements "user stories"
```
---
Critique mode testing review (detailed)
```bash
/sc:spec-panel --mode critique --focus testing --format detailed "integration tests"
```
---
Comprehensive specification review
```bash
/sc:spec-panel --mode discussion --focus requirements --iterations 3 --format detailed "system specification"
```

---

## Project Management

### /sc:pm

**Description**: Project Manager Agent - Default orchestration agent that coordinates all sub-agents and manages workflows seamlessly

**Category**: orchestration | **Complexity**: meta

**Syntax**:
```bash
/sc:pm [options] "[request]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | brainstorm, direct, wave | Execution strategy |
| `--verbose` | - | Verbose output |

**MCP Servers**: sequential, context7, magic, playwright, morphllm, serena, tavily, chrome-devtools

**Personas**: pm-agent

**Auto-Activation Triggers**:
- Session start (mandatory)
- All user requests (default entry point)
- Status questions ("progress", "status")
- Vague requests ("want to", "implement")
- Multi-domain tasks
- Complex projects

**Session Lifecycle**:

1. **Session Start Protocol**:
```yaml
Context Restoration:
  - list_memories() → Check existing state
  - read_memory("pm_context") → Restore overall context
  - read_memory("current_plan") → Current work
  - read_memory("last_session") → Previous work
  - read_memory("next_actions") → Next actions
```

2. **During Work (PDCA Cycle)**:
```yaml
Plan (Hypothesis):
  - write_memory("plan", goal_statement)
  - Create docs/temp/hypothesis-YYYY-MM-DD.md

Do (Experiment):
  - TodoWrite for task tracking
  - write_memory("checkpoint", progress) every 30min

Check (Evaluation):
  - think_about_task_adherence()
  - Assess against goals

Act (Improvement):
  - Success → docs/patterns/[pattern-name].md
  - Failure → docs/mistakes/mistake-YYYY-MM-DD.md
```

**Examples**:

Default usage (no command needed, describe requirements directly, PM Agent handles orchestration automatically)
```bash
"Need to add payment processing to the app"
```
---
Explicit strategy selection (using wave strategy)
```bash
/sc:pm --strategy wave "Improve application security"
```
---
Brainstorm mode (PM Agent activates brainstorm mode)
```bash
"Maybe we could improve the user experience?"
```

---

### /sc:task

**Description**: Complex task execution with intelligent workflow management and delegation

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:task [options] "[task-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | systematic, agile, enterprise | Task strategy |
| `--parallel` | - | Enable parallel execution |
| `--delegate` | - | Enable agent delegation |

**Examples**:

Systematic task execution
```bash
/sc:task --strategy systematic "implement authentication"
```
---
Parallel task execution
```bash
/sc:task --parallel --delegate "refactor API endpoints"
```

---

### /sc:spawn

**Description**: Meta-system task orchestration with intelligent breakdown and delegation

**Category**: special | **Complexity**: high

**Syntax**:
```bash
/sc:spawn [complex-task] [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | sequential, parallel, adaptive | Coordination strategy |
| `--depth` | normal, deep | Decomposition depth |

**Behavioral Flow**:
1. **Analyze**: Parse complex operation requirements, assess cross-domain scope
2. **Decompose**: Break down into coordinated subtask hierarchies
3. **Orchestrate**: Execute tasks using optimal strategy
4. **Monitor**: Track progress across task hierarchies
5. **Integrate**: Aggregate results, provide orchestration summary

**Task Hierarchy**:
```
Epic → Story → Task → Subtask
```

**Examples**:

Complex feature implementation
```bash
/sc:spawn "implement user authentication system"
```
Breakdown: Database design → Backend API → Frontend UI → Testing

---
Large-scale system operation
```bash
/sc:spawn --strategy adaptive --depth deep "migrate legacy monolith to microservices"
```
---
Cross-domain infrastructure
```bash
/sc:spawn "establish CI/CD pipeline with security scanning"
```

---

### /sc:select-tool

**Description**: Intelligent MCP tool selection based on complexity scoring and operation analysis

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:select-tool [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--analyze` | - | Analyze current context |
| `--explain` | - | Explain tool selection |

**Examples**:

Analyze tool selection
```bash
/sc:select-tool --analyze
```
---
Explain tool selection reasoning
```bash
/sc:select-tool --explain
```

---

### /sc:index-repo

**Description**: Repository indexing for context optimization (94% token reduction: 58K → 3K)

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:index-repo [path]
```

**Examples**:

Index current repository
```bash
/sc:index-repo .
```
---
Index specific directory
```bash
/sc:index-repo src/
```

---

## Session Management

### /sc:load

**Description**: Session lifecycle management with Serena MCP integration for project context loading

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:load [target] [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | project, config, deps, checkpoint | Load type |
| `--refresh` | - | Refresh cache |
| `--analyze` | - | Enable analysis |

**Examples**:

Load project context
```bash
/sc:load --type project src/
```
---
Load checkpoint
```bash
/sc:load --type checkpoint "auth-feature"
```
---
Refresh and analyze
```bash
/sc:load --refresh --analyze
```

---

### /sc:save

**Description**: Session lifecycle management with Serena MCP integration for session context persistence

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:save [name] [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | session, learnings, context, all | Save type |
| `--summarize` | - | Generate summary |
| `--checkpoint` | - | Create checkpoint |

**Examples**:

Save session
```bash
/sc:save --type session "auth-complete"
```
---
Save learnings
```bash
/sc:save --type learnings --summarize
```
---
Create checkpoint
```bash
/sc:save --checkpoint "midpoint"
```

---

### /sc:agent

**Description**: SC Agent - Session controller that orchestrates the complete workflow of investigation, implementation, and review

**Category**: orchestration | **Complexity**: advanced

**Note**: This agent starts automatically at session start, no manual invocation required.

**Startup Behavior**:
1. `git status --porcelain` → Report `📊 Git: clean|X files|not a repo`
2. Remind user: `💡 Use /context to confirm token budget.`
3. Report core service status: confidence check, deep research, repository index

**Task Protocol**:
1. **Clarify scope** - Confirm success criteria, blockers, and constraints
2. **Plan investigation** - Use parallel tool calls
3. **Iterate until confident** - Track confidence until ≥0.90
4. **Implementation wave** - Prepare edits as single checkpoint summary
5. **Self-review and reflexion** - Call `@self-review` to verify results

**Helper Skills**:
- `@confidence-check` - Pre-implementation score check (requires ≥0.90)
- `@deep-research` - Web/MCP research
- `@repo-index` - Repository structure and file manifest
- `@self-review` - Post-implementation verification

**Examples**:

Agent starts automatically at session start, takes over complete workflow after user describes task
```bash
# No manual invocation required, auto-activated
```

---

## Utilities

### /sc:help

**Description**: List all available /sc commands and their functionality

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:help [command-name]
```

**Examples**:

Show all command help
```bash
/sc:help
```
---
Specific command help
```bash
/sc:help implement
```

---

### /sc:recommend

**Description**: Hyper-intelligent command recommendation engine

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:recommend
```

**Examples**:

Get command recommendations
```bash
/sc:recommend
```

---

### /sc:sc

**Description**: SuperClaude command dispatcher - Display all available commands

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc
```

**Examples**:

Show all commands
```bash
/sc
```

---

## MCP Server Integration

### Available Servers

| Server | Purpose | API Key | Auto-Activation Triggers |
|--------|---------|---------|-------------------------|
| **context7** | Official library documentation | No | Import statements, framework keywords |
| **sequential** | Multi-step reasoning | No | `--think`, debugging, complex analysis |
| **magic** | UI component generation | Yes | `component`, `UI`, frontend requests |
| **playwright** | Browser automation | No | `test`, `e2e`, `browser` |
| **morphllm** | Code transformations | Yes | Multi-file edits, refactoring |
| **serena** | Semantic code understanding | No | Large projects, session management |
| **tavily** | Web search | Yes (free tier) | `/sc:research`, `latest` |
| **chrome-devtools** | Performance analysis | No | `performance`, `debug` |

### Server Combinations

```yaml
Free (No API Keys):
  - context7 + sequential + playwright + serena

Learning:
  - context7 + sequential

Web Development:
  - magic + context7 + playwright

Deep Research:
  - tavily + sequential + serena

Enterprise Refactoring:
  - serena + morphllm + sequential
```

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

---

## Best Practices

### 1. Command Selection Guide

| Scenario | Recommended Command | Reason |
|----------|---------------------|--------|
| New project kickoff | `/sc:brainstorm` | Structured requirements discovery |
| Feature implementation | `/sc:implement` | Intelligent persona coordination |
| Code review | `/sc:analyze` | Multi-dimensional analysis |
| Test execution | `/sc:test` | Coverage and quality reporting |
| Deep research | `/sc:research` | Adaptive multi-source search |
| Daily tasks | `/sc:pm` | Auto-orchestration (default) |

### 2. Flag Combination Patterns

```bash
# Deep security analysis
/sc:analyze --focus security --depth deep

# Comprehensive testing
/sc:test --type all --coverage

# Safe implementation
/sc:implement "feature" --safe --with-tests

# Detailed research
/sc:research "topic" --depth exhaustive --strategy unified
```

### 3. Workflow Patterns

**New Feature Development**:
```bash
/sc:brainstorm "feature idea" --strategy systematic
/sc:design "feature" --type architecture
/sc:workflow "implementation plan"
/sc:implement "feature" --with-tests
/sc:test --coverage
/sc:document --type api
```

**Bug Fixing**:
```bash
/sc:troubleshoot "bug description" --trace
/sc:analyze --focus quality --depth deep
/sc:implement "fix" --safe
/sc:test --type regression
```

**Code Optimization**:
```bash
/sc:analyze --focus performance
/sc:improve --type performance --safe
/sc:cleanup --type all --interactive
/sc:test --coverage
```

### 4. Token Efficiency

| Task Complexity | Token Budget | Recommended Approach |
|-----------------|--------------|---------------------|
| Simple (typo) | 200 | Direct fix |
| Medium (bug fix) | 1,000 | Confidence check |
| Complex (new feature) | 2,500 | Full workflow |

**Confidence Check ROI**: Spending 100-200 tokens can save 5,000-50,000 tokens

---

## Quick Reference Card

### Core Commands

```bash
# Discovery & Planning
/sc:brainstorm "idea"        # Structured brainstorming
/sc:design "system"          # Architecture design
/sc:workflow "task"          # Workflow planning

# Development
/sc:implement "feature"      # Code implementation
/sc:improve path/            # Code improvement
/sc:test --coverage          # Test execution

# Research
/sc:research "topic"         # Web research
/sc:analyze path/            # Code analysis

# Session Management
/sc:save "checkpoint"        # Save session
/sc:load "session"           # Load session
/sc                          # List all commands
```

### Common Flags

```bash
--think         # Enable sequential reasoning
--think-hard    # Enable deep analysis
--c7            # Force Context7 activation
--no-mcp        # Disable MCP servers
--all-mcp       # Enable all MCP servers
--coverage      # Include test coverage
--depth quick   # Research depth control
--safe          # Safe mode
--with-tests    # Include tests
--interactive   # Interactive mode
```

---

**License**: MIT

**Repository**: [github.com/SuperClaude-Org/SuperClaude_Framework](https://github.com/SuperClaude-Org/SuperClaude_Framework)
