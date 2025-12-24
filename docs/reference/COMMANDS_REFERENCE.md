# SuperClaude Framework - 命令参考大全

> **Version**: 4.1.9 | **Total Commands**: 30 | **Last Updated**: December 2025

本文档为 SuperClaude Framework 的完整命令参考手册，包含所有 30 个斜杠命令的详细说明、参数、使用示例和最佳实践。

---

## 目录

1. [命令概览](#命令概览)
2. [Planning & Requirements (4)](#planning--requirements-计划与需求)
3. [Development (5)](#development-开发)
4. [Testing & Quality (4)](#testing--quality-测试与质量)
5. [Documentation (3)](#documentation-文档)
6. [Research & Analysis (3)](#research--analysis-研究与分析)
7. [Project Management (5)](#project-management-项目管理)
8. [Session Management (3)](#session-management-会话管理)
9. [Utilities (3)](#utilities-工具)
10. [MCP Server Integration](#mcp-server-integration)
11. [Best Practices](#best-practices)

---

## 命令概览

### 快速参考表

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

### 命令命名空间

所有命令使用 `/sc:` 命名空间前缀：

```bash
/sc:brainstorm "project idea"    # 结构化头脑风暴
/sc:implement "feature name"     # 代码实现
/sc:research "topic"             # 深度研究
/sc:test --coverage              # 测试执行
```

---

## Planning & Requirements (计划与需求)

### /sc:brainstorm

**Description**: 通过苏格拉底式对话和系统化探索进行交互式需求发现

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:brainstorm [options] "[topic/idea]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | systematic, agile, enterprise | 探索策略选择 |
| `--depth` | shallow, normal, deep | 分析深度 |
| `--parallel` | - | 启用并行探索路径 |

**MCP Servers**: sequential, context7, magic, playwright, morphllm, serena

**Personas**: architect, analyzer, frontend, backend, security, devops, project-manager

**Behavioral Flow**:
1. **Explore**: 通过苏格拉底式对话转化模糊想法
2. **Analyze**: 协调多个角色进行领域专业分析
3. **Validate**: 应用可行性评估和需求验证
4. **Specify**: 生成具体规格说明
5. **Handoff**: 创建可执行的实施简报

**Examples**:

系统化产品发现（深度分析）
```bash
/sc:brainstorm --strategy systematic --depth deep "AI-powered project management tool"
```
---
敏捷功能探索（并行路径）
```bash
/sc:brainstorm --strategy agile --parallel "real-time collaboration features"
```
---
企业解决方案验证
```bash
/sc:brainstorm --strategy enterprise "enterprise data analytics platform"
```
---
快速浅层探索
```bash
/sc:brainstorm --depth shallow "mobile app idea"
```
---
系统化并行深度探索
```bash
/sc:brainstorm --strategy systematic --depth deep --parallel "microservices architecture"
```
---
敏捷迭代探索
```bash
/sc:brainstorm --strategy agile --depth normal "user authentication improvements"
```

**Boundaries**:
- **Will**: 将模糊想法转化为具体规格，协调多个角色和MCP服务器
- **Will Not**: 在探索阶段没有适当需求发现的情况下做出实施决策

---

### /sc:design

**Description**: 设计系统架构、API和组件接口，生成全面的规格说明

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:design [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | architecture, api, component, database | 设计类型 |
| `--format` | diagram, spec, code | 输出格式 |

**Behavioral Flow**:
1. **Analyze**: 检查目标需求和现有系统上下文
2. **Plan**: 根据类型和格式定义设计方法
3. **Design**: 创建符合行业最佳实践的全面规格
4. **Validate**: 确保设计满足需求和可维护性标准
5. **Document**: 生成清晰的设计文档

**Examples**:

系统架构设计
```bash
/sc:design --type architecture --format diagram user-management-system
```
---
API规格设计
```bash
/sc:design --type api --format spec payment-api
```
---
组件接口设计
```bash
/sc:design --type component --format code notification-service
```
---
数据库模式设计
```bash
/sc:design --type database --format diagram e-commerce-db
```

---

### /sc:estimate

**Description**: 为任务、功能或项目提供智能开发估算

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:estimate [options] "[target]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | time, effort, complexity | 估算类型 |
| `--unit` | hours, days, weeks | 时间单位 |
| `--breakdown` | - | 启用详细分解 |

**Examples**:

时间估算
```bash
/sc:estimate --type time --unit days "authentication system"
```
---
复杂度分析
```bash
/sc:estimate --type complexity --breakdown "API refactoring"
```

---

### /sc:workflow

**Description**: 从PRD和功能需求生成结构化实施工作流

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:workflow [options] "[feature-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | systematic, agile, enterprise | 工作流策略 |
| `--depth` | shallow, normal, deep | 工作流深度 |
| `--parallel` | - | 启用并行执行 |

**Examples**:

系统化工作流
```bash
/sc:workflow --strategy systematic "payment integration"
```
---
敏捷迭代工作流
```bash
/sc:workflow --strategy agile --depth deep "user onboarding"
```

---

## Development (开发)

### /sc:implement

**Description**: 智能角色激活和MCP集成的功能代码实现

**Category**: workflow | **Complexity**: standard

**Syntax**:
```bash
/sc:implement [options] "[feature-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | component, api, service, feature | 实现类型 |
| `--framework` | react, vue, express, etc. | 框架选择 |
| `--safe` | - | 启用安全模式 |
| `--with-tests` | - | 包含测试生成 |

**MCP Servers**: context7, sequential, magic, playwright

**Personas**: architect, frontend, backend, security, qa-specialist

**Behavioral Flow**:
1. **Analyze**: 检查实现需求，检测技术上下文
2. **Plan**: 选择方法，激活相关角色
3. **Generate**: 使用框架特定最佳实践创建代码
4. **Validate**: 应用安全和质量验证
5. **Integrate**: 更新文档，提供测试建议

**Examples**:

React组件实现
```bash
/sc:implement --type component --framework react "user profile component"
```
---
API服务实现（安全模式+测试）
```bash
/sc:implement --type api --safe --with-tests "user authentication API"
```
---
全栈功能
```bash
/sc:implement --type feature --with-tests "payment processing system"
```
---
Vue框架组件
```bash
/sc:implement --type component --framework vue "dashboard widget"
```
---
Express后端服务
```bash
/sc:implement --type service --framework express --safe "file upload service"
```
---
React安全组件（含测试）
```bash
/sc:implement --type component --framework react --safe --with-tests "admin panel"
```
---
Next.js页面实现
```bash
/sc:implement --type feature --framework nextjs "user settings page"
```
---
纯API实现（无测试）
```bash
/sc:implement --type api "notification endpoint"
```

---

### /sc:build

**Description**: 智能错误处理和优化的构建、编译和打包项目

**Category**: utility | **Complexity**: enhanced

**Syntax**:
```bash
/sc:build [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | dev, prod, test | 构建类型 |
| `--clean` | - | 清理构建 |
| `--optimize` | - | 启用优化 |
| `--verbose` | - | 详细输出 |

**Examples**:

开发构建
```bash
/sc:build --type dev
```
---
生产构建
```bash
/sc:build --type prod --clean --optimize
```
---
详细构建
```bash
/sc:build --verbose
```

---

### /sc:improve

**Description**: 系统化改进代码质量、性能和可维护性

**Category**: workflow | **Complexity**: standard

**Syntax**:
```bash
/sc:improve [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | quality, performance, maintainability, style | 改进类型 |
| `--safe` | - | 安全模式（保守改进） |
| `--interactive` | - | 交互式改进 |
| `--preview` | - | 预览模式（显示变更） |
| `--validate` | - | 启用验证 |

**MCP Servers**: sequential, context7

**Personas**: architect, performance, quality, security

**Examples**:

质量改进
```bash
/sc:improve --type quality src/auth
```
---
性能优化（安全模式）
```bash
/sc:improve --type performance --safe api/
```
---
交互式风格改进
```bash
/sc:improve --type style --interactive components/
```
---
可维护性改进（预览）
```bash
/sc:improve --type maintainability --preview src/utils
```
---
质量改进（验证+交互）
```bash
/sc:improve --type quality --validate --interactive src/services
```
---
安全性能优化（预览）
```bash
/sc:improve --type performance --safe --preview database/
```
---
全面质量审查
```bash
/sc:improve --type quality --validate --safe src/
```
---
风格统一（安全+预览）
```bash
/sc:improve --type style --safe --preview --validate components/
```

---

### /sc:cleanup

**Description**: 系统化清理代码、移除死代码、优化项目结构

**Category**: workflow | **Complexity**: standard

**Syntax**:
```bash
/sc:cleanup [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | code, imports, files, all | 清理类型 |
| `--safe` | - | 安全模式（保守清理） |
| `--aggressive` | - | 激进模式（彻底清理） |
| `--interactive` | - | 交互式清理 |
| `--preview` | - | 预览模式（显示变更） |

**MCP Servers**: sequential, context7

**Personas**: architect, quality, security

**Examples**:

安全代码清理
```bash
/sc:cleanup --type code --safe src/
```
---
导入清理
```bash
/sc:cleanup --type imports
```
---
全面交互式清理
```bash
/sc:cleanup --type all --interactive
```
---
激进文件清理（预览）
```bash
/sc:cleanup --type files --aggressive --preview
```
---
安全代码清理（预览）
```bash
/sc:cleanup --type code --safe --preview src/legacy
```
---
交互式导入清理
```bash
/sc:cleanup --type imports --interactive
```
---
全面激进清理
```bash
/sc:cleanup --type all --aggressive
```
---
安全全面清理（预览+交互）
```bash
/sc:cleanup --type all --safe --preview --interactive
```

---

### /sc:git

**Description**: 智能提交消息和工作流优化的Git操作

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:git [options] "[operation]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--smart-commit` | - | 智能提交消息生成 |
| `--interactive` | - | 交互式Git操作 |

**Examples**:

智能提交
```bash
/sc:git --smart-commit
```
---
创建功能分支
```bash
/sc:git "feature/user-auth"
```
---
交互式操作
```bash
/sc:git --interactive
```

---

## Testing & Quality (测试与质量)

### /sc:test

**Description**: 执行测试并进行覆盖率分析和自动化质量报告

**Category**: utility | **Complexity**: enhanced

**Syntax**:
```bash
/sc:test [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | unit, integration, e2e, all | 测试类型 |
| `--coverage` | - | 启用覆盖率分析 |
| `--watch` | - | 监视模式 |
| `--fix` | - | 自动修复简单失败 |

**MCP Servers**: playwright (for e2e)

**Personas**: qa-specialist

**Behavioral Flow**:
1. **Discover**: 使用运行器模式分类可用测试
2. **Configure**: 设置测试环境和执行参数
3. **Execute**: 运行测试并实时监控
4. **Analyze**: 生成覆盖率报告和失败诊断
5. **Report**: 提供可操作建议和质量指标

**Examples**:

基本测试执行
```bash
/sc:test
```
---
单元测试覆盖率分析
```bash
/sc:test --type unit --coverage src/components
```
---
端到端浏览器测试
```bash
/sc:test --type e2e
```
---
开发监视模式（自动修复）
```bash
/sc:test --watch --fix
```
---
集成测试
```bash
/sc:test --type integration
```
---
全面测试（含覆盖率）
```bash
/sc:test --type all --coverage
```
---
单元测试监视模式
```bash
/sc:test --type unit --watch
```
---
E2E测试（自动修复）
```bash
/sc:test --type e2e --fix
```
---
覆盖率监视模式
```bash
/sc:test --coverage --watch
```

---

### /sc:analyze

**Description**: 跨质量、安全、性能和架构领域的全面代码分析

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:analyze [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--focus` | quality, security, performance, architecture | 分析焦点 |
| `--depth` | quick, deep | 分析深度 |
| `--format` | text, json, report | 输出格式 |

**Behavioral Flow**:
1. **Discover**: 使用语言检测和项目分析分类源文件
2. **Scan**: 应用特定领域分析技术
3. **Evaluate**: 生成带严重性评级的优先发现
4. **Recommend**: 创建可操作建议
5. **Report**: 呈现全面分析报告

**Examples**:

全面项目分析
```bash
/sc:analyze
```
---
聚焦安全评估（深度）
```bash
/sc:analyze --focus security --depth deep src/auth
```
---
性能优化分析（报告格式）
```bash
/sc:analyze --focus performance --format report
```
---
快速质量检查
```bash
/sc:analyze --focus quality --depth quick src/components
```
---
架构深度分析（JSON输出）
```bash
/sc:analyze --focus architecture --depth deep --format json
```
---
安全快速扫描
```bash
/sc:analyze --focus security --depth quick
```
---
性能深度分析
```bash
/sc:analyze --focus performance --depth deep api/
```
---
质量报告（深度）
```bash
/sc:analyze --focus quality --depth deep --format report src/
```

---

### /sc:troubleshoot

**Description**: 诊断和解决代码、构建、部署和系统行为中的问题

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:troubleshoot [options] "[issue-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | bug, build, performance, deployment | 问题类型 |
| `--trace` | - | 启用追踪 |
| `--fix` | - | 自动修复 |

**Examples**:

Bug诊断
```bash
/sc:troubleshoot --type bug "login form not submitting"
```
---
构建问题
```bash
/sc:troubleshoot --type build --trace "build failing on CI"
```
---
性能问题
```bash
/sc:troubleshoot --type performance --fix "API response slow"
```

---

### /sc:reflect

**Description**: 使用Serena MCP分析能力进行任务反思和验证

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:reflect [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | task, session, completion | 反思类型 |
| `--analyze` | - | 启用深度分析 |
| `--validate` | - | 启用验证 |

**Examples**:

任务反思
```bash
/sc:reflect --type task --analyze
```
---
会话回顾
```bash
/sc:reflect --type session
```
---
完成验证
```bash
/sc:reflect --type completion --validate
```

---

## Documentation (文档)

### /sc:document

**Description**: 为组件、函数、API和功能生成聚焦文档

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:document [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | inline, external, api, guide | 文档类型 |
| `--style` | brief, detailed | 文档风格 |

**Examples**:

内联文档
```bash
/sc:document --type inline src/utils.ts
```
---
API文档
```bash
/sc:document --type api --style detailed api/
```
---
用户指南
```bash
/sc:document --type guide --style brief
```

---

### /sc:explain

**Description**: 提供代码、概念和系统行为的清晰解释

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:explain [options] "[target]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--level` | basic, intermediate, advanced | 解释级别 |
| `--format` | text, examples, interactive | 解释格式 |
| `--context` | [domain] | 上下文领域 |

**Examples**:

基础解释
```bash
/sc:explain --level basic src/auth/middleware.ts
```
---
高级详细解释
```bash
/sc:explain --level advanced --format examples "JWT authentication flow"
```
---
交互式解释
```bash
/sc:explain --format interactive "database optimization"
```

---

### /sc:index

**Description**: 生成全面的项目文档和知识库

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:index [options] [target]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | docs, api, structure, readme | 索引类型 |
| `--format` | md, json, yaml | 输出格式 |

**Examples**:

文档索引
```bash
/sc:index --type docs
```
---
API索引
```bash
/sc:index --type api --format json api/
```
---
项目结构索引
```bash
/sc:index --type structure --format yaml
```

---

## Research & Analysis (研究与分析)

### /sc:research

**Description**: 自适应规划和智能搜索的深度网络研究

**Category**: command | **Complexity**: advanced

**Syntax**:
```bash
/sc:research [options] "[query]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--depth` | quick, standard, deep, exhaustive | 研究深度 |
| `--strategy` | planning, intent, unified | 规划策略 |

**MCP Servers**: tavily, sequential, playwright, serena

**Personas**: deep-research-agent

**Research Depth Levels**:
| Depth | Sources | Hops | Time | Best For |
|-------|---------|------|------|----------|
| Quick | 5-10 | 1 | ~2min | 快速事实查询 |
| Standard | 10-20 | 2-3 | ~5min | 一般研究（默认） |
| Deep | 20-40 | 3-4 | ~8min | 全面分析 |
| Exhaustive | 40+ | 5 | ~10min | 学术级研究 |

**Behavioral Flow**:
1. **Understand** (5-10%): 评估查询复杂性和模糊性
2. **Plan** (10-15%): 选择规划策略，识别并行机会
3. **TodoWrite** (5%): 创建自适应任务层次
4. **Execute** (50-60%): 并行搜索、智能提取、多跳探索
5. **Track** (持续): 监控进度，更新置信度
6. **Validate** (10-15%): 验证证据链，检查来源可信度

**Examples**:

基础研究（默认深度）
```bash
/sc:research "latest developments in quantum computing 2024"
```
---
深度竞品分析
```bash
/sc:research --depth deep "competitive analysis of AI coding assistants"
```
---
统一策略研究
```bash
/sc:research --strategy unified "best practices for distributed systems"
```
---
快速事实查询
```bash
/sc:research --depth quick "current React version"
```
---
学术级深度研究
```bash
/sc:research --depth exhaustive "machine learning optimization techniques"
```
---
意图规划研究
```bash
/sc:research --strategy intent "cloud architecture patterns"
```
---
深度+规划组合
```bash
/sc:research --depth deep --strategy planning "microservices security best practices"
```
---
标准研究（显式指定）
```bash
/sc:research --depth standard "database scaling strategies"
```

**Output**: 报告保存到 `claudedocs/research_[topic]_[timestamp].md`

---

### /sc:business-panel

**Description**: 9位著名商业思想家的多专家商业战略分析

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:business-panel [options] "[topic]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--mode` | discussion, debate, socratic | 分析模式 |
| `--experts` | [name1,name2,...] | 专家选择 |

**Available Experts**:
- Christensen (颠覆性创新)
- Porter (竞争战略)
- Drucker (管理)
- Godin (营销)
- Kim & Mauborgne (蓝海战略)
- Collins (卓越)
- Taleb (风险)
- Meadows (系统思维)
- Doumont (沟通)

**Examples**:

市场进入战略分析
```bash
/sc:business-panel --mode discussion "market entry strategy"
```
---
辩论模式
```bash
/sc:business-panel --mode debate --experts porter,godin "pricing strategy"
```
---
苏格拉底式探索
```bash
/sc:business-panel --mode socratic "digital transformation"
```

---

### /sc:spec-panel

**Description**: 著名软件工程专家的多专家规格审查和改进

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:spec-panel [options] "[specification]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--mode` | discussion, critique, socratic | 审查模式 |
| `--experts` | [name1,name2,...] | 专家选择 |
| `--focus` | requirements, architecture, testing, compliance | 审查焦点 |
| `--iterations` | [N] | 迭代次数 |
| `--format` | standard, structured, detailed | 输出格式 |

**Examples**:

需求规格审查
```bash
/sc:spec-panel --focus requirements "API specification"
```
---
架构批评模式
```bash
/sc:spec-panel --mode critique --focus architecture "microservices design"
```
---
详细迭代审查
```bash
/sc:spec-panel --iterations 3 --format detailed "security policy"
```
---
苏格拉底式测试审查
```bash
/sc:spec-panel --mode socratic --focus testing "test coverage strategy"
```
---
合规性讨论审查
```bash
/sc:spec-panel --mode discussion --focus compliance "GDPR requirements"
```
---
指定专家架构审查
```bash
/sc:spec-panel --experts fowler,beck --focus architecture "domain-driven design"
```
---
多轮结构化需求审查
```bash
/sc:spec-panel --iterations 5 --format structured --focus requirements "user stories"
```
---
批评模式测试审查（详细）
```bash
/sc:spec-panel --mode critique --focus testing --format detailed "integration tests"
```
---
全面规格审查
```bash
/sc:spec-panel --mode discussion --focus requirements --iterations 3 --format detailed "system specification"
```

---

## Project Management (项目管理)

### /sc:pm

**Description**: 项目经理代理 - 协调所有子代理并无缝管理工作流的默认编排代理

**Category**: orchestration | **Complexity**: meta

**Syntax**:
```bash
/sc:pm [options] "[request]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | brainstorm, direct, wave | 执行策略 |
| `--verbose` | - | 详细输出 |

**MCP Servers**: sequential, context7, magic, playwright, morphllm, serena, tavily, chrome-devtools

**Personas**: pm-agent

**Auto-Activation Triggers**:
- 会话开始（强制）
- 所有用户请求（默认入口）
- 状态问题（"进度"、"现状"）
- 模糊请求（"想要"、"实现"）
- 多领域任务
- 复杂项目

**Session Lifecycle**:

1. **Session Start Protocol**:
```yaml
Context Restoration:
  - list_memories() → 检查现有状态
  - read_memory("pm_context") → 恢复整体上下文
  - read_memory("current_plan") → 当前工作
  - read_memory("last_session") → 上次工作
  - read_memory("next_actions") → 下一步行动
```

2. **During Work (PDCA Cycle)**:
```yaml
Plan (仮説):
  - write_memory("plan", goal_statement)
  - Create docs/temp/hypothesis-YYYY-MM-DD.md

Do (実験):
  - TodoWrite for task tracking
  - write_memory("checkpoint", progress) every 30min

Check (評価):
  - think_about_task_adherence()
  - Assess against goals

Act (改善):
  - Success → docs/patterns/[pattern-name].md
  - Failure → docs/mistakes/mistake-YYYY-MM-DD.md
```

**Examples**:

默认用法（无需命令，直接描述需求，PM Agent自动处理编排）
```bash
"Need to add payment processing to the app"
```
---
显式策略选择（使用wave策略）
```bash
/sc:pm --strategy wave "Improve application security"
```
---
头脑风暴模式 (PM Agent激活头脑风暴模式)
```bash
"Maybe we could improve the user experience?"
```

---

### /sc:task

**Description**: 智能工作流管理和委托的复杂任务执行

**Category**: orchestration | **Complexity**: advanced

**Syntax**:
```bash
/sc:task [options] "[task-description]"
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | systematic, agile, enterprise | 任务策略 |
| `--parallel` | - | 启用并行执行 |
| `--delegate` | - | 启用代理委托 |

**Examples**:

系统化任务执行
```bash
/sc:task --strategy systematic "implement authentication"
```
---
并行任务执行
```bash
/sc:task --parallel --delegate "refactor API endpoints"
```

---

### /sc:spawn

**Description**: 智能分解和委托的元系统任务编排

**Category**: special | **Complexity**: high

**Syntax**:
```bash
/sc:spawn [complex-task] [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--strategy` | sequential, parallel, adaptive | 协调策略 |
| `--depth` | normal, deep | 分解深度 |

**Behavioral Flow**:
1. **Analyze**: 解析复杂操作需求，评估跨领域范围
2. **Decompose**: 分解为协调的子任务层次
3. **Orchestrate**: 使用最优策略执行任务
4. **Monitor**: 跟踪任务层次进度
5. **Integrate**: 聚合结果，提供编排摘要

**Task Hierarchy**:
```
Epic → Story → Task → Subtask
```

**Examples**:

复杂功能实现
```bash
/sc:spawn "implement user authentication system"
```
分解: Database design → Backend API → Frontend UI → Testing

---
大规模系统操作
```bash
/sc:spawn --strategy adaptive --depth deep "migrate legacy monolith to microservices"
```
---
跨领域基础设施
```bash
/sc:spawn "establish CI/CD pipeline with security scanning"
```

---

### /sc:select-tool

**Description**: 基于复杂度评分和操作分析的智能MCP工具选择

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:select-tool [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--analyze` | - | 分析当前上下文 |
| `--explain` | - | 解释工具选择 |

**Examples**:

分析工具选择
```bash
/sc:select-tool --analyze
```
---
解释工具选择理由
```bash
/sc:select-tool --explain
```

---

### /sc:index-repo

**Description**: 用于上下文优化的仓库索引（94% token减少：58K → 3K）

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:index-repo [path]
```

**Examples**:

索引当前仓库
```bash
/sc:index-repo .
```
---
索引特定目录
```bash
/sc:index-repo src/
```

---

## Session Management (会话管理)

### /sc:load

**Description**: 与Serena MCP集成的会话生命周期管理，用于项目上下文加载

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:load [target] [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | project, config, deps, checkpoint | 加载类型 |
| `--refresh` | - | 刷新缓存 |
| `--analyze` | - | 启用分析 |

**Examples**:

加载项目上下文
```bash
/sc:load --type project src/
```
---
加载检查点
```bash
/sc:load --type checkpoint "auth-feature"
```
---
刷新并分析
```bash
/sc:load --refresh --analyze
```

---

### /sc:save

**Description**: 与Serena MCP集成的会话生命周期管理，用于会话上下文持久化

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:save [name] [options]
```

**Options**:
| Flag | Values | Description |
|------|--------|-------------|
| `--type` | session, learnings, context, all | 保存类型 |
| `--summarize` | - | 生成摘要 |
| `--checkpoint` | - | 创建检查点 |

**Examples**:

保存会话
```bash
/sc:save --type session "auth-complete"
```
---
保存学习
```bash
/sc:save --type learnings --summarize
```
---
创建检查点
```bash
/sc:save --checkpoint "midpoint"
```

---

### /sc:agent

**Description**: SC Agent - 会话控制器，编排调查、实现和审查的完整工作流

**Category**: orchestration | **Complexity**: advanced

**Note**: 此代理在会话开始时自动启动，无需手动调用。

**Startup Behavior**:
1. `git status --porcelain` → 报告 `📊 Git: clean|X files|not a repo`
2. 提醒用户: `💡 Use /context to confirm token budget.`
3. 报告核心服务状态: confidence check, deep research, repository index

**Task Protocol**:
1. **Clarify scope** - 确认成功标准、阻碍和约束
2. **Plan investigation** - 使用并行工具调用
3. **Iterate until confident** - 追踪置信度直到 ≥0.90
4. **Implementation wave** - 准备编辑作为单一检查点摘要
5. **Self-review and reflexion** - 调用 `@self-review` 验证结果

**Helper Skills**:
- `@confidence-check` - 预实现分数检查（需要≥0.90）
- `@deep-research` - 网络/MCP研究
- `@repo-index` - 仓库结构和文件清单
- `@self-review` - 后实现验证

**Examples**:

Agent在会话开始时自动启动，用户描述任务后Agent接管完整工作流
```bash
# 无需手动调用，自动激活
```

---

## Utilities (工具)

### /sc:help

**Description**: 列出所有可用的/sc命令及其功能

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:help [command-name]
```

**Examples**:

显示所有命令帮助
```bash
/sc:help
```
---
特定命令帮助
```bash
/sc:help implement
```

---

### /sc:recommend

**Description**: 超智能命令推荐引擎

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc:recommend
```

**Examples**:

获取命令推荐
```bash
/sc:recommend
```

---

### /sc:sc

**Description**: SuperClaude命令调度器 - 显示所有可用命令

**Category**: utility | **Complexity**: basic

**Syntax**:
```bash
/sc
```

**Examples**:

显示所有命令
```bash
/sc
```

---

## MCP Server Integration

### Available Servers

| Server | Purpose | API Key | Auto-Activation Triggers |
|--------|---------|---------|-------------------------|
| **context7** | 官方库文档 | No | 导入语句、框架关键字 |
| **sequential** | 多步推理 | No | `--think`、调试、复杂分析 |
| **magic** | UI组件生成 | Yes | `component`、`UI`、前端请求 |
| **playwright** | 浏览器自动化 | No | `test`、`e2e`、`browser` |
| **morphllm** | 代码转换 | Yes | 多文件编辑、重构 |
| **serena** | 语义代码理解 | No | 大型项目、会话管理 |
| **tavily** | 网络搜索 | Yes (free tier) | `/sc:research`、`latest` |
| **chrome-devtools** | 性能分析 | No | `performance`、`debug` |

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

MCP服务器在 `~/.claude.json` 中配置：

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

### 1. 命令选择指南

| 场景 | 推荐命令 | 理由 |
|------|----------|------|
| 新项目启动 | `/sc:brainstorm` | 结构化需求发现 |
| 功能实现 | `/sc:implement` | 智能角色协调 |
| 代码审查 | `/sc:analyze` | 多维度分析 |
| 测试执行 | `/sc:test` | 覆盖率和质量报告 |
| 深度调研 | `/sc:research` | 自适应多源搜索 |
| 日常任务 | `/sc:pm` | 自动编排（默认） |

### 2. Flag组合模式

```bash
# 深度安全分析
/sc:analyze --focus security --depth deep

# 全面测试
/sc:test --type all --coverage

# 安全实现
/sc:implement "feature" --safe --with-tests

# 详细研究
/sc:research "topic" --depth exhaustive --strategy unified
```

### 3. 工作流模式

**新功能开发**:
```bash
/sc:brainstorm "feature idea" --strategy systematic
/sc:design "feature" --type architecture
/sc:workflow "implementation plan"
/sc:implement "feature" --with-tests
/sc:test --coverage
/sc:document --type api
```

**Bug修复**:
```bash
/sc:troubleshoot "bug description" --trace
/sc:analyze --focus quality --depth deep
/sc:implement "fix" --safe
/sc:test --type regression
```

**代码优化**:
```bash
/sc:analyze --focus performance
/sc:improve --type performance --safe
/sc:cleanup --type all --interactive
/sc:test --coverage
```

### 4. Token效率

| 任务复杂度 | Token预算 | 推荐方法 |
|-----------|----------|----------|
| 简单（拼写错误） | 200 | 直接修复 |
| 中等（Bug修复） | 1,000 | 置信度检查 |
| 复杂（新功能） | 2,500 | 完整工作流 |

**置信度检查ROI**: 花费100-200 tokens 可节省 5,000-50,000 tokens

---

## Quick Reference Card

### 核心命令

```bash
# 发现与规划
/sc:brainstorm "idea"        # 结构化头脑风暴
/sc:design "system"          # 架构设计
/sc:workflow "task"          # 工作流规划

# 开发
/sc:implement "feature"      # 代码实现
/sc:improve path/            # 代码改进
/sc:test --coverage          # 测试执行

# 研究
/sc:research "topic"         # 网络研究
/sc:analyze path/            # 代码分析

# 会话管理
/sc:save "checkpoint"        # 保存会话
/sc:load "session"           # 加载会话
/sc                          # 列出所有命令
```

### 常用Flags

```bash
--think         # 启用顺序推理
--think-hard    # 启用深度分析
--c7            # 强制Context7激活
--no-mcp        # 禁用MCP服务器
--all-mcp       # 启用所有MCP服务器
--coverage      # 包含测试覆盖率
--depth quick   # 研究深度控制
--safe          # 安全模式
--with-tests    # 包含测试
--interactive   # 交互式模式
```

---

**License**: MIT

**Repository**: [github.com/SuperClaude-Org/SuperClaude_Framework](https://github.com/SuperClaude-Org/SuperClaude_Framework)
