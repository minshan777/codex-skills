# PR 测试准备

读取 PR 或提测任务，核实最新改动后，一次准备：

- 大白话改动说明。
- 中文冒烟用例 Excel。
- 一条可手动操作的部署验证用例。

**使用**：提供 PR 或任务链接，说“帮我准备测试这个 PR”，或使用 `$qa-pr-test-prep`。

**安装**：将本目录和同仓库的 [`qa-smoke-cases`](../qa-smoke-cases/) 一起放入 `~/.codex/skills/`；Excel 生成需要环境提供 Spreadsheets 技能。

仅准备测试，不执行用例、不修改产品数据，也不向任务或 PR 发评论。
