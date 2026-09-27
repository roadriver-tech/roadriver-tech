# 如何参与本仓库

## 提交规范

提交信息遵循 Conventional Commits 格式：

```bash
git commit -m "<type>: <description>"
```

| 类型 | 说明 |
|------|------|
| `feat` | 新功能 |
| `fix` | 修复 bug |
| `docs` | 文档更新 |
| `test` | 测试相关 |
| `refactor` | 代码重构 |
| `chore` | 构建/工具 |

### 提交纪律

- 提交信息不超过 72 字符，一次提交只做一件事
- 提交前 `git diff` 确认变更内容，不提交不完整的更改
- 验证通过再提交；提交即推送，并回报 GitHub 提交链接

## Skill

本仓库把高频工作流封装为 Skill，位于 `.agents/skills/` 目录：

| Skill | 用途 | 触发词 |
|-------|------|--------|
| [git-commit](.agents/skills/git-commit/SKILL.md) | 规范提交 | 「提交」、「commit」 |

每个 `SKILL.md` 包含 frontmatter（`name`、`description`）与正文（触发词、规则、工作流）。Agent 按触发词匹配并执行对应 Skill。

### 新建 Skill

```bash
mkdir -p .agents/skills/<name>
# 创建 .agents/skills/<name>/SKILL.md
```

### 修改与删除 Skill

直接编辑对应文件或删除目录，随仓库提交变更即可。

## 人机协作原则

1. 最小干预：仅在用户明确请求时操作，不主动创建文件，优先编辑现有文件
2. 原子提交：每次提交独立完整，验证后再提交
3. 验证优先：修改后运行构建或校验，确保更改符合预期
4. 安全第一：不创建可能被恶意使用的代码，发现漏洞即报告

## 许可

贡献的内容按 [CC BY 4.0](LICENSE) 授权。
