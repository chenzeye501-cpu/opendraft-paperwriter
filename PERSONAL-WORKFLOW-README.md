# Codex Personal Workflow Pack（中文）

本仓库分支新增个人工作流总管 Skill，目标是复用已有能力、审计缺口并保持任务可续接。

## 当前 Skill
- `.codex/skills/gihe-paper/SKILL.md`：已有 GIHE 论文流程，支持“写、改、查”等中文指令。
- `.codex/skills/personal-workflow-router/SKILL.md`：新增总管，负责先审计，再路由到已有项目或 Skill，避免重复建设。
- 股票研究项目：另见 https://github.com/chenzeye501-cpu/stock-lab ，以其 `AGENTS.md` 和 README 为准。

## 建议快捷指令
- `盘点现有能力`
- `继续`
- `检查进度`
- `查漏补缺`
- `执行下一步`
- `最终检查`

## 安全原则
优先复用；不猜测本地文件或 Skill 的安装状态；未运行测试不声称通过；不将演示行情当真实行情；高影响写入、删除、对外发送、提交或合并前先确认。

## 安装提醒
此 Skill 已提交到本仓库的 `codex/personal-workflow-router` 分支，尚未合并到 `master`。要在本机使用，需要将其放入 Codex 实际识别的 Skills 目录，或在本地工作区使用该仓库分支。不同 Codex 环境的技能发现路径可能不同；先检查环境，不要覆盖现有配置。
