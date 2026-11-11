# Asana 提 Bug 技能

将中文问题描述和截图整理成英文 Bug 报告，并在 Asana 指定分类的 **To Fix** 列表中创建任务、分配研发人员、填写字段和插入截图。具体执行规则见 [SKILL.md](./SKILL.md)。

## 安装

将本仓库中的以下两个目录一起放入 `~/.codex/skills/`，保持同级：

```text
~/.codex/skills/
├── asana-file-bug/
│   └── SKILL.md
└── english-bug-report/
    └── SKILL.md
```

依赖 [english-bug-report](../english-bug-report)，用于撰写英文标题及 Steps / Expected / Actual。提交时需要可操作的浏览器或原生应用界面，以及已登录且有编辑权限的 Asana 账号。

## 如何使用

明确说“帮我提 bug”或指定 `$asana-file-bug`，并提供复现步骤、实际结果、预期结果和相关截图。分类可以沿用当前对话；无法确定时会询问。

示例：

> 帮我在 work session 提 bug：当前停留在 Tools，从顶部会话切换器点击 New Session 后仍停留在 Tools，预期重置会话并跳转到 Chat。截图见附件。

仅要求“写英文 bug”或“查一下是否有人提过”，不会创建 Asana 任务。

## 提交流程

1. 根据已有证据生成英文报告，不编造复现过程或根因。
2. 打开指定分类，在 To Fix 列表末尾点击新增任务，再打开右侧详细资料。
3. 填写标题、负责人、Priority、Status、Issue Type、Feature Module 和 Creator。
4. 描述中填写除标题外的报告内容，并内嵌与该问题相关的截图。
5. 保存后核对任务内容、字段、分类和图片，返回任务链接、负责人、优先级及状态。

## 研发分配

按实际出问题的功能分配，而不是只看步骤中出现的页面：

| 功能范围 | 负责人 |
| --- | --- |
| Director、Shot、Scene、Timeline、故事编辑及导出 | Bellina Lu |
| Chat Mode / General Agent 对话及生成 | mok zhou |
| 导航栏、侧栏、新会话路由、Agent / Tools 导航 | Bleen Wang |
| Find in chat、Use in Chat、资产到工具等快捷跳转 | Bleen Wang |

未约定归属的功能会根据项目现有信息确认，不随意指派。

## 默认字段

| 字段 | 规则 |
| --- | --- |
| 项目 | QA Bug Tracker |
| Feature Module | 用户指定分类，例如 Work session |
| Status / 列表分组 | To Fix，除非用户另有要求 |
| Priority | 根据影响和是否存在替代操作选择 P0–P3 |
| Issue Type | 通常为 Function Bug，也可按问题选择 UX、UI / 文案等已有类型 |
| Creator | Minshan Cheng |

[Work session 列表](https://app.asana.com/1/1206647353644946/project/1213171864208739/list/1220317576115179)。

## 执行约定

- 明确要求提 bug 即授权创建任务和上传该问题的相关截图。
- 截图应嵌入描述，不能用本地文件路径代替。
- 保存结果不确定时先检查已有任务，避免重复创建。
- 没有截图时可提交有依据的文字报告；登录或上传受阻时会说明未完成部分。
- 不自动添加评论、通知同事或修改无关任务。
