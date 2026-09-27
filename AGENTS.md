# AGENTS.md

## 相关文档

| 文档 | 用途 |
|------|------|
| [README](README.md) | 项目概述、目录结构 |
| [CONTRIBUTING](CONTRIBUTING.md) | 提交规范、Skill 使用和维护 |
| [CHANGELOG](CHANGELOG.md) | 变更日志 |

### Skill 索引

| Skill | 用途 | 路径 |
|-------|------|------|
| [git-commit](.agents/skills/git-commit/SKILL.md) | 规范提交 | `.agents/skills/git-commit/SKILL.md` |

## 快速索引

| 任务 | 操作位置 |
|------|---------|
| 提交变更 | Skill：`git-commit` |
| 新增文档 | 更新 `README.md` 目录与本文档的相关文档表 |
| 新增工作流 | `.agents/skills/<name>/SKILL.md`，并在本文档补索引 |

## 我的工作原则

### 最小干预

- 仅在用户明确请求时操作
- 不主动创建文件（除非必要）
- 优先编辑现有文件
- 目录变更需与作者商议：作者对目录使用有严格规范，能不更改尽量不更改

### 原子提交

- 每次提交独立完整，不提交不完整的更改
- 验证后再提交

### 验证优先

- 修改后运行构建或校验
- 确保更改符合预期

### 安全第一

- 不创建可能被恶意使用的代码
- 检测安全漏洞并报告
- 遵循 OWASP 最佳实践

## 输出规范

### 内容格式

- 不使用 emoji（除非用户明确请求）
- 输出简洁，适合 CLI 显示
- 正式文档格式克制：标题最多三级，列表与表格仅在必要时使用，术语全文一致

### 文件引用

- 使用 `code` 格式表示文件路径
- 每个引用独立，不合并
- 可选包含行号信息

### 代码示例

- 使用 fenced code blocks 并标注语言
- 保持简洁

## Git 提交规范

遵循 Conventional Commits 格式，详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

| 类型 | 说明 | 示例 |
|------|------|------|
| `feat` | 新功能 | `feat: add user authentication` |
| `fix` | 修复 bug | `fix: resolve null pointer exception` |
| `docs` | 文档更新 | `docs: update README` |
| `test` | 测试相关 | `test: add unit tests for api` |
| `refactor` | 代码重构 | `refactor: simplify logic` |
| `chore` | 构建/工具 | `chore: update dependencies` |

## 如何维护 AGENTS.md

| 类型 | 写在哪里 |
|------|---------|
| 详细说明、工作流步骤 | `.agents/skills/` 中的 Skill 文件 |
| 给链接、导航索引 | AGENTS.md |

更新时机：新增文档、新增任务类型、重要规则变化时更新；README/Skill 已有的内容不重复。
