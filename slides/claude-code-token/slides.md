---
layout: cover
background: https://cover.sli.dev?title=claude-code-token
title: Claude Code 省 Token 心法
author: Terry Lin
transition: slide-left
mdc: true
---

# 用少少的錢做最多的事
# Claude Code 省 Token 的
# 心得分享

Terry Lin

---
layout: intro
---

# 為什麼要談這個？

因為 Claude Code 很強，但也很貴。

每天的 Quota 有上限，如果中午就用光，下午就沒事做了。

因此如何善用 Token 發揮最大價值，就變得很重要了。

---
layout: center
class: text-center
---

# 心法一：讓餘額一目瞭然 👀

隨時掌握 Quota，就像隨時知道錢包剩多少

---

# 怎麼查餘額？

- 🤔 **偶爾查**
  - 不確定的時候用 Prompt 跟 AI 問一下。
- 👀 **順便看**
  - Terminal 的 Status Line 會顯示，養成餘光掃描的習慣。
- 🚨 **抬頭看**
  - 裝個 Mac Menu Bar App，直接掛在螢幕頂端。

> 🛠️ 相關 scripts 與 tools 皆可在 `skills/IT` 與 `IT-Tools` 目錄中取得

---
layout: center
class: text-center
---

# 心法二：Context 的收納與整理術 📦

像整理房間一樣，常保輕盈與乾淨

---

空間可視化：/context 📏

### 使用指令
- `/context`
  - 將目前的 Context 用量視覺化為彩色方格。

---

# 1. 只有必要的才帶 🎒

### 🔍 Tool Search
- 不要當 MCP 囤積狂。
- 開啟 `ENABLE_TOOL_SEARCH`，讓 Agent 自己搜、自己載。

### 🥷 Sub-agents
- 大任務派分身。
- 主 Agent 指揮，分身做完就消失，不佔記憶體。

---

# 2. 該丟的就丟 �

### 🗑️ 指令斷捨離
- `/clear`: 直接失憶，重新做人 (最省錢)。
- `/compact`: 壓縮回憶 (折衷)。

### 🥪 漸進式餵食
- `CLAUDE.md` 也別一次塞滿。
- 用 `@reference` 連結，需要時再讀。

---
layout: center
class: text-center
---

# 心法三：殺雞不要用牛刀 🔪

把好鋼用在刀刃上，不要這也要 Opus 那也要 Opus

---

# 模型怎麼選？

- 🧠 **Claude Opus 4.5 (大腦擔當)**
  - **價格 5 倍**。Plan Mode 專用。負責把路徑想清楚，邏輯最強。
- ⚡️ **Claude Sonnet 4.5 (手腳擔當)**
  - **價格 3 倍**。Act Mode 專用。寫 Code 又快又好，CP 值最高。
- 🏃 **Claude Haiku 4.5 (速度擔當)**
  - **價格 1 倍**。效率之王。適合快速迭代、單一任務與大規模數據處理。

---
layout: center
class: text-center
---

# 心法四：苗頭不對，馬上撤退 🛑

拒絕「Token 焚化爐」

---

# 什麼是「鬼打牆」？

Claude 寫 Code ➡️ 報錯 💥 ➡️ Claude 修正 ➡️ 又報錯 💥 ➡️ Claude 再修正...

### 怎麼解？

- **Plan Mode 先想再做**：強迫它先寫計畫，不要急著 Coding。
- **One-shot Prompting**：背景、需求、限制，一次講完。
- **ESC 快速中斷**：發現走錯方向，按一下 ESC 立刻停止，比等它跑完再糾正省多了！

---
layout: cover
---

# 最後總結

- 👀 **讓餘額一目瞭然**：隨時知道還剩多少
- 📦 **Context 收納與整理**：保持輕盈與乾淨
- 🔪 **殺雞不要用牛刀**：把好鋼用在對的刀刃上
- 🛑 **苗頭不對，馬上撤退**：發現不對就停手

> 🔄 **記得常保工具更新**：`cch update && claude update`

---
layout: center
class: text-center
---

# 下回預告

# Claude Code 社群好物
## 那些你可能錯過的必看開源專案推薦

就像玩神裝 RPG，大神都怎麼配裝？
下次分享一些好用的開源工具配置！