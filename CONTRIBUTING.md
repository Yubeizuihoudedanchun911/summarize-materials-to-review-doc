# Contributing

感谢你改进 `summarize-materials-to-review-doc`。本仓库用于维护可复用的 Skill 规则，不用于存放真实述职材料或生成结果。

## 可以贡献什么

- 更准确的触发条件和输入要求
- 更清晰的证据整理、叙事压缩或排版方法
- 可复用的交付检查规则
- 对现有说明中的歧义、遗漏或错误进行修正

## 内容边界

- 不得提交真实姓名、绩效信息、内部链接、未公开指标、客户数据、访问凭证或其他敏感内容。
- 示例必须匿名化，并使用虚构的项目、组织和数据。
- 不要提交实际生成的 DOCX、PDF、演示文稿或原始材料目录。
- 保持 `SKILL.md` 简洁；详细规则放在 `references/`，避免重复维护同一内容。

## 开发流程

1. 从 `main` 创建 `codex/<short-description>` 分支。
2. 仅修改与本次目标相关的文件。
3. 运行校验并检查完整差异。
4. 提交 Pull Request，说明改动目的、影响范围和验证结果。

建议的本地检查：

```bash
python ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py .
git diff --check
git status -sb
```

## Pull Request 要求

Pull Request 应说明：

- 改了什么，以及为什么修改
- 是否改变 Skill 的触发条件或输出合同
- 使用了哪些检查或真实场景进行验证
- 是否包含需要维护者重点确认的取舍

提交前再次确认差异中不包含个人材料、公司内部信息或本地生成文件。
