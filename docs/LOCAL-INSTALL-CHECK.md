# Windows 本地 Skill 盘点与接入检查

本流程只做盘点，不自动复制、覆盖或删除文件。

## 1. 先检查本机有哪些 Skill

在 Windows PowerShell 中运行：

``
powershell
$roots = @(
  "$HOME\.codex\skills",
  "$HOME\.agents\skills",
  "$PWD\.codex\skills",
  "$PWD\.agents\skills",
  "D:\GIHE-Paper-System"
) | Where-Object { Test-Path $_ }

$roots | ForEach-Object {
  Write-Output "`n### ROOT: $_"
  Get-ChildItem -Path $_ -Filter "SKILL.md" -File -Recurse -ErrorAction SilentlyContinue |
    Select-Object -ExpandProperty FullName
}
```

这只是常见目录的只读检查，不代表每种 Codex 安装都使用相同目录。以你当前 Codex 客户端/CLI 的官方设置和实际扫描结果为准。

## 2. 检查论文工作区

预期本地工作区：`D:\GIHE-Paper-System\`

先确认目录是否存在、里面有哪些项目；不要为了匹配这个路径而搬动已有文件。
论文仓库已有 `.codex/skills/gihe-paper/SKILL.md`，不要创建重复的论文 Skill。

## 3. 安全接入流程

1. 查看本地 Git 状态，确认没有未提交修改被覆盖。
2. 拉取并检查分支 `codex/personal-workflow-router`。
3. 比较本地 Skill 目录中是否已经有同名 `personal-workflow-router`。
4. 若同名文件已存在，先比较差异，不直接覆盖。
5. 复制/安装前向用户报告目标路径与将新增的文件。
6. 安装后让 Codex 明确列出识别到的 Skill，并实际测试“盘点现有能力”。
7. 测试失败时回滚本次新增文件，不改动其他 Skill。

## 4. 当前已知 GitHub 项目

- 论文项目：https://github.com/chenzeye501-cpu/opendraft-paperwriter
- 股票项目：https://github.com/chenzeye501-cpu/stock-lab

GitHub 仓库可访问不代表本地代码已克隆，也不代表远程执行环境已安装依赖。
