# Gemini Argon 写作

把话写清楚，也留住作者自己的口吻。

一套从 Gemini Argon 文本样例与编辑反馈中提炼的中文写作 Skill，适合起稿、润色、长文分析、产品内容和日常沟通。当前内容版本为 v4。

## 可以用来做什么

- **润色改稿**：保留原稿里具体、有劲的句子，修掉空话、绕弯和没有依据的推断。
- **长文分析**：沿着读者的疑问往下推，让上一段的结论带出下一段的问题；支线材料服从主问题，不凑通用点评。
- **评审与反驳**：有证据就直接下判断，把分歧落在条件、代价和方案上。
- **复杂沟通**：根据对象切换语气，支持婉拒、关心、叙事与轻幽默。

纪实内容守住材料；通用创作可以使用典型场景和类比。真实人物、产品参数、实测结果与承诺，都不能为了文气顺畅而补造；交代口径与边界时自然融进正面陈述，不留审稿批注腔。

## 安装到 Codex

把本仓库下载或克隆到本机 Skills 目录，文件夹命名为 `gemini-natural-writing`。macOS / Linux 可执行：

```bash
git clone https://github.com/shaoxiang880-jpg/gemini-argon-writing.git ~/.codex/skills/gemini-natural-writing
```

如果本机已有这个目录，请先保留自己的修改，再更新文件。安装后的目录里应直接包含 `SKILL.md`、`agents/` 和 `references/`。

显示名称是 **Gemini Argon 写作**，调用标识为 `gemini-natural-writing`。

## 怎么用

直接提出任务：

```text
用 Gemini Argon 写作润色下面这篇稿子。
保留技术信息和作者口吻，只修空话、重复、绕弯和没有依据的推断。

正文：
……
```

也可以明确调用：

```text
用 $gemini-natural-writing 写一篇分析文章。
读者：……
要回答的问题：……
已知材料：……
```

通用对话模型可以复制 [prompt.txt](prompt.txt)，在末尾填入任务和材料，无需安装。

## 看一个简短例子

已知：周三能给提纲，周五才能给完整稿。

**原话**

> 周三给不了，请不要再催了。

**改写**

> 知道你想周三先推进。我这边周三能给提纲，完整稿要到周五。要是急着定方向，咱们可以先看提纲。

这里保留了真实限制和已经确认的安排，没有另编理由。

## 文件说明

| 文件 | 用途 |
| --- | --- |
| [SKILL.md](SKILL.md) | 完整写作规则与任务选择 |
| [agents/openai.yaml](agents/openai.yaml) | 显示名称与默认调用提示 |
| [references/examples.md](references/examples.md) | 短稿、婉拒、叙事等场景示例 |
| [references/longform.md](references/longform.md) | 长文推进方法与完整示例 |
| [prompt.txt](prompt.txt) | 可直接复制的简短提示词 |

这套 Skill 提炼的是可观察的写法，不包含 Gemini 的内部提示词或模型参数。
