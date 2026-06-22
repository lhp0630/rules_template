# AI 规则模板

一个全面的 AI 编码助手规则模板，支持 **Cursor AI** 和 **Claude Code** 上下文工程。

## 概述

该模板提供了一个基于软件工程最佳实践和文档驱动开发的结构化框架，用于 AI 辅助开发。它帮助 AI 编码助手理解项目上下文、遵循约定并保持代码质量。

## 功能特性

- **Cursor AI 支持**：`.cursor/rules/` 目录，使用 `.mdc` 文件按需加载
- **Claude Code 支持**：上下文工程工作流，使用 PRP（产品需求提示）
- **记忆库**：在 `docs/` 和 `tasks/` 中的持久化文档系统
- **敏捷工作流**：基于软件工程原则和最佳实践
- **自动文档**：更改后自动更新文档

## 快速开始

### Cursor AI

1. 将 `.cursor/rules/` 复制到项目根目录
2. 使用 Cursor AI 开始编码

### Claude Code

1. 将 `.claude/` 目录和 `CLAUDE.md` 复制到项目根目录
2. 从 [Anthropic](https://docs.anthropic.com/en/docs/claude-code) 安装 Claude Code
3. 使用 PRP 工作流：
   - 在 `INITIAL.md` 中编写需求
   - 运行 `/generate-prp INITIAL.md`
   - 运行 `/execute-prp PRPs/your-feature-name.md`

## 目录结构

```
project/
├── .cursor/rules/      # Cursor AI 规则
├── .claude/            # Claude Code 配置
├── CLAUDE.md           # Claude Code 全局规则
├── AGENTS.md           # MiMoCode 规则
├── MEMORY.md           # 记忆文档系统
├── docs/               # 文档
│   ├── architecture.md
│   ├── technical.md
│   └── product_requirement_docs.md
├── tasks/              # 任务管理
│   ├── active_context.md
│   └── tasks_plan.md
├── PRPs/               # 产品需求提示
├── examples/           # 代码示例
└── src/                # 源代码
```

## 规则文件

### Cursor AI

```
.cursor/rules/
├── rules.mdc           # 核心规则
├── plan.mdc            # 规划工作流
├── implement.mdc       # 实现工作流
├── debug.mdc           # 调试工作流
├── memory.mdc          # 文档系统
└── directory-structure.mdc
```

### 记忆系统

`MEMORY.md` 提供了一个全面的持久化项目记忆文档系统：

- **核心文件**（必需）：产品需求、架构、技术规范、任务计划、活跃上下文、错误文档、经验教训
- **上下文文件**（可选）：文献调研、RFC
- **工作流**：PLAN/ACT 模式用于读写记忆文件
- **自动更新**：更改后自动更新文档

### Claude Code

```
.claude/
├── commands/
│   ├── generate-prp.md
│   └── execute-prp.md
└── settings.local.json
```

## 核心原则

1. **上下文工程**：为 AI 助手提供全面的上下文
2. **验证循环**：通过可执行测试进行自纠正工作流
3. **文档驱动**：通过结构化文档实现持久化记忆
4. **模块化设计**：关注点分离和增量开发

## 贡献

请参阅 [CONTRIBUTING.md](CONTRIBUTING.md) 了解贡献指南。

## 致谢

本项目受以下项目启发并参考：
- [rules_template](https://github.com/Bhartendu-Kumar/rules_template) 作者：Bhartendu Kumar
- [context-engineering-intro](https://github.com/coleam00/context-engineering-intro) 作者：Cole McMahan

## 许可证

MIT