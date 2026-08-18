# summarize-materials-to-review-doc

把分散的工作材料、指定大纲和文档模板，整理成证据清楚、叙事完整、适合评审阅读的晋升或述职文件。

## 适用场景

- 晋升答辩、年度述职、阶段复盘等材料整理
- 从周报、项目文档、指标记录和个人总结中提炼核心事实
- 在不改变既定大纲的前提下压缩篇幅、强化挑战与决策过程
- 按既有模板生成 Markdown、DOCX 或在线文档交付稿

## 输入与输出

建议同时提供以下三类输入：

1. 原始材料集合：项目记录、周报、复盘、指标和可引用事实。
2. 文档大纲：必须保留的章节顺序与叙事结构。
3. 模板及约束：版式、页数、密级、目标职级和交付格式。

默认输出包括证据清单、内容映射、精炼正文和交付前检查结果。涉及在线文档、上传或权限修改时，仍需遵守目标系统的授权与安全要求。

## 安装

克隆到个人 Skill 目录：

```bash
git clone https://github.com/Yubeizuihoudedanchun911/summarize-materials-to-review-doc.git ~/.codex/skills/summarize-materials-to-review-doc
```

也可以克隆到独立目录，再链接到项目的 `.codex/skills/` 下。

## 使用

在任务中显式调用：

```text
使用 $summarize-materials-to-review-doc，基于 materials/ 中的原始材料，
按照 outline.md 的大纲和 template.docx 的版式，生成 9 页以内的晋升述职稿。
```

Skill 会按以下顺序工作：

1. 建立事实与证据清单，区分已验证事实、合理推断和待补信息。
2. 将证据映射到既定大纲，保留原有章节和叙事主线。
3. 围绕背景、挑战、判断、方案、结果和复盘组织内容。
4. 压缩重复背景，保留核心语句，并降低模板化、空泛的表达。
5. 按模板完成版式、图片、表格和页数检查，再输出交付稿。

详细执行规则见 [SKILL.md](SKILL.md)。

## 仓库结构

```text
.
├── SKILL.md                     # Skill 入口和执行流程
├── agents/openai.yaml           # Codex UI 元数据
└── references/
    ├── input-and-evidence.md     # 输入盘点与证据边界
    ├── narrative-and-layout.md   # 叙事压缩与排版规则
    └── delivery-qa.md            # 交付前质量检查
```

## 隐私与安全

不要把真实晋升材料、个人绩效、内部链接、未公开指标、访问凭证或公司敏感信息提交到仓库、Issue 或 Pull Request。示例必须匿名化，并使用虚构数据。更多要求见 [SECURITY.md](SECURITY.md)。

## 验证

修改 Skill 后，运行标准校验：

```bash
python ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py .
git diff --check
```

## 贡献

贡献方式见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

本项目采用 [MIT License](LICENSE)。
