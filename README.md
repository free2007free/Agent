# Agent — 個人助理

一個以 Claude Code 設定檔形式存在的個人助理，專注於 **Email 管理**、**行事曆管理**與**任務提醒**。

## 內容

- `CLAUDE.md` — 助理的核心人設、職責、安全規則與操作備忘
- `.claude/settings.json` — Gmail 與 Google Calendar 工具權限（讀取類免確認、寄送/變更類需確認）
- `.claude/commands/` — 快捷指令
  - `/inbox` — 整理並摘要收件匣
  - `/reply` — 草擬回覆（只建草稿，不直接寄出）
  - `/cleanup` — 分類／標記收件匣
  - `/remind` — 設定一次性或週期性提醒
  - `/agenda` — 查詢今天／本週行程
  - `/schedule` — 建立行事曆活動（建立前先確認）

## 使用方式

在這個 repo 開啟 Claude Code session，即可用上述 slash command，或直接用自然語言請助理幫忙處理 Email 與提醒。
