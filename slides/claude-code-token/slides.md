---
layout: cover
background: https://cover.sli.dev?title=claude-code-token
title: Claude Code 省 Tokens 的心得分享
author: Terry Lin
transition: slide-left
mdc: true
---

# 用少少的錢做最多的事
# Claude Code 省 Tokens 的
# 心得分享

Terry Lin

---
layout: intro
---

# 為什麼要談這個？

因為 Claude Code 很強，但也很貴。

每天的 Quota 有上限，如果中午就用光，下午就沒事做了。

因此如何善用 Tokens 發揮最大價值，就變得很重要了。

---
layout: center
class: text-center
---

# 心法 1：讓餘額一目瞭然

隨時掌握 Quota，就像隨時知道錢包剩多少

---

# 怎麼查餘額？

- **偶爾查**
  - 不確定時，直接用 Prompt 問 AI。
- **順便瞄**
  - Terminal Status Line 常駐顯示，養成餘光掃瞄習慣。
- **抬頭看**
  - 裝個 Mac Menu Bar App，直接掛在螢幕頂端。

> 相關資源可於 `skills/IT`、`IT-Tools/scripts` 與 `IT-Tools/quota-tracker` 取得

---
layout: center
class: text-center
---

# 心法 2：Context 收納整理術

像整理房間一樣，常保空間輕盈乾淨

---

空間可視化：/context

### 使用指令
- `/context`
  - 將目前的 Context 用量視覺化為彩色方格。

---

# 1. 只有必要的才帶

### Tool Search (`ENABLE_TOOL_SEARCH`)
- **新版預設支援**：MCP 超過 Context **10%** 時會自動開啟。
- **可強制開啟**：也可以透過設定強制一定要開 (`true`)，極致省流。

### Sub-agents
- **適合調查與驗證**：把探索、檢查或確認的工作交給分身，主線保持乾淨。
- **用完即丟**：主 Agent 指揮，分身做完就消失，不佔 Context。

---

# 2. 該丟的就丟

### 指令斷捨離
- `/clear`: 直接失憶，重新做人 (最省錢)。
- `/compact`: 主動壓縮對話，只留下重要資訊。

### 漸進式餵食
- **持續優化 `CLAUDE.md`**：它是專案的重要資產，請持續優化它。
- **別一次塞滿**：善用 `@reference` 連結，需要時再讀。

---
layout: center
class: text-center
---

# 心法 3：殺雞不要用牛刀

把好鋼用在刀刃上

---

# 模型怎麼選？

- **Claude Opus 4.5 (大腦擔當)**
  - **價格 5 倍**。Plan Mode 專用。負責把路徑想清楚，邏輯最強。
- **Claude Sonnet 4.5 (手腳擔當)**
  - **價格 3 倍**。Act Mode 專用。寫 Code 又快又好，主力輸出。
- **Claude Haiku 4.5 (速度擔當)**
  - **價格 1 倍**。效率之王。適合快速迭代、單一任務與大規模數據處理。

---
layout: center
class: text-center
---

# 心法 4：苗頭不對，馬上撤退

拒絕成為「Token 焚化爐」

---

# 什麼是「鬼打牆」？

寫 Code -> 報錯 -> 修正 -> 又報錯 -> 無限迴圈

### 怎麼解？

- **Plan Mode 先想再做**：強迫它先寫計畫，不要急著 Coding。
- **One-shot Prompting**：背景、需求、限制，一次講完。
- **維護 `CLAUDE.md`**：保持文件正確，就像給 AI 準確的地圖，能少繞很多彎路。
- **ESC 快速中斷**：發現走錯方向，按一下 ESC 立刻停止，比等它跑完再糾正省多了！

---
layout: cover
---

# 最後總結

- **讓餘額一目瞭然**：像盯著錢包一樣盯著 Quota
- **Context 收納術**：只帶必要的，該丟的就丟
- **殺雞不用牛刀**：選對模型，省錢又高效
- **苗頭不對即撤**：拒絕陷入 Debug 的無限迴圈

> **記得常保工具更新**：`cch update && claude update`

---
layout: center
class: text-center
---

# 下回預告

# Claude Code 社群好物
## 那些你可能錯過的必看開源專案推薦

就像玩 RPG 遊戲一樣，看看大神都怎麼配裝？
