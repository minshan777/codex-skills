# Codex Skills

个人 Codex 技能。

| 技能 | 用途 | 示例触发词 |
| --- | --- | --- |
| [english-bug-report](english-bug-report/) | 编写或翻译英文 Bug 报告 | 帮我写成英文 Bug 报告 |
| [asana-file-bug](asana-file-bug/) | 撰写英文 Bug 报告并提交到 Asana，设置负责人和字段、内嵌截图 | 帮我在 work session 提 bug |
| [qa-pr-test-prep](qa-pr-test-prep/) | 改动说明、冒烟 Excel 和一条手动部署验证用例 | 帮我准备测试这个 PR |
| [qa-smoke-cases](qa-smoke-cases/) | 编写中文冒烟用例 Excel | 输出冒烟用例 |
| [qa-test-cases](qa-test-cases/) | 编写或调整中文功能测试用例 Excel | 编写测试用例 |
| [qa-test-assets](qa-test-assets/) | 生成图片、视频、音频等测试输入并打包 | 生成测试资源 |

## 安装与使用

将需要的技能目录放入 `~/.codex/skills/`，在 Codex 中使用对应触发词，或通过 `$技能名` 指定调用。每个目录的 README 提供简要说明，`SKILL.md` 定义具体规则。

`asana-file-bug` 需要同时安装 `english-bug-report`，并在可操作的浏览器或原生应用中登录有编辑权限的 Asana 账号；仅要求写报告或查重时不会创建任务。详细说明见 [asana-file-bug/README.md](asana-file-bug/README.md)。

`qa-pr-test-prep` 需要同时安装 `qa-smoke-cases`；生成 Excel 需要环境提供 Spreadsheets 技能。生成具体视觉图片时，`qa-test-assets` 使用环境提供的 imagegen 技能及工具。

这些技能用于报告编写、Bug 提交、测试准备和素材生成，不自动执行产品测试。
