# hermes-agent-soul

[自用] Hermes Agent 的共用 persona 與 workflow-plus skill。

- `SOUL.md` — 全域人格，Hermes 會自動載入為身份預設。
- `skills/workflow-plus/SKILL.md` — 通用工作紀律，含任務模式、危險操作限制、memory 記憶工具觸發、tool 定義與使用、browser fallback 瀏覽器操作提示。

## 安裝

```bash
cp SOUL.md ~/.hermes/SOUL.md
cp -r skills/workflow-plus ~/.hermes/skills/workflow-plus
```

## 啟動

```bash
hermes --yolo --tui
```

## 依賴

- **codegraph**：用於程式碼查詢，於專案內 `codegraph init` 使用。
- **plugged.in**：跨 PC 記憶與知識庫，並代理 `chrome-devtools` 工具。

## 補充

- 預設：Hermes built-in browser tools 或 `browser_exec`
- 備援：`mcp__pluggedin__chrome_devtools__*`，由 `pluggedin` MCP 代理
- WSL -> Windows：優先 chrome-devtools MCP 備援
