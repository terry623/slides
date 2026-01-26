---
layout: cover
background: https://cover.sli.dev?title=claude-code-token
title: Claude Code 省 Token 心法
author: Terry Lin
transition: slide-left
mdc: true
---

# Claude Code 省 Token 的五大心法

拒絕錢包破洞，從這裡開始 💸

---
layout: intro
---

# 為什麼要談這個？

因為 Claude Code 很強，但也很貴。

每天的 Quota 有上限，如果中午就用光，下午就沒事做了。

因此規劃好一天的 Token 使用進度，就變得很重要。

---
layout: default
---

# 心法一：讓餘額一目瞭然

- 🤔 **偶爾查**
  - 不確定的時候用 Prompt 跟 AI 問一下。
- 👀 **順便看**
  - Terminal 的 Status Line 會顯示，養成餘光掃描的習慣。
- 🚨 **抬頭看**
  - 裝個 Mac Menu Bar App，直接掛在螢幕頂端。

> 🛠️ 相關 scripts 與 tools 皆可在 `skills/IT` 與 `IT-Tools` 目錄中取得

---
layout: two-cols
layoutClass: gap-8
---

# 心法二：工具不一次梭哈

MCP 工具雖然好用，但不要當「囤積狂」。

### ❌ 舊思維：塞爆行李箱
不管用不用，先把所有 MCP Server 加上去。
**結果**：還沒開始做事，Context Window 就先被工具定義吃飽了。

### ✅ 新解法：Tool Search
讓 Agent 自己帶個「搜尋引擎」。
只有它覺得「需要用 Sentry」時，才去把工具載進來。

> 記得開啟 `ENABLE_TOOL_SEARCH`

---

# Sub-agents (影分身之術)

遇到像「重寫整個登入系統」這種超大任務：

- 🤖 **主線程 Agent**
  - 保持清醒，負責指揮
- ⬇️ **派工**
- 👾 **Sub-agent (分身)**
  - 去髒活累活，做完回報結果，記憶體用完就丟。
  - ✅ **最佳作用**：尋找資訊，並將少量總結回傳給主對話線程。
  - ❌ **最大誤用**：嘗試讓 Sub-agent 直接進行實際的 Implementation。

> **別把主線程的腦袋撐爆！** 🤯

---
layout: center
class: text-center
---

# 心法三：大腦要定期排毒 🧠

保持乾淨，不要囤積垃圾資訊。

---

# 怎麼排毒？

### 指令清理術

- `/context`
  - 將目前的 Context 用量視覺化為彩色方格。
- `/clear`
  - 直接失憶，重新做人. 最省錢，激推！👍
- `/compact`
  - 把回憶壓縮成摘要。折衷方案。

### 餵食的藝術

> **漸進式揭露**
>
> 不要像倒垃圾一樣把整個專案文件丟給它。
> 像擠牙膏，做到哪給到哪。

---
layout: default
---

# 心法四：殺雞不要用牛刀 🔪

把好鋼用在刀刃上，不要這也要 Opus 那也要 Opus。

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

# 心法五：苗頭不對，馬上撤退 🛑

拒絕「Token 焚化爐」

---

# 什麼是「鬼打牆」？

Claude 寫 Code ➡️ 報錯 💥 ➡️ Claude 修正 ➡️ 又報錯 💥 ➡️ Claude 再修正...

> **這就是 Token 焚化爐 🔥**

### 怎麼解？

- **Plan Mode 先想再做**：強迫它先寫計畫，不要急著 Coding。
- **One-shot Prompting**：背景、需求、限制，一次講完。
- **主動喊卡**：發現它開始瞎忙，馬上 Stop。重開 Session 比期待它變聰明更實際。

---
layout: cover
background: https://cover.sli.dev?title=Summary
title: 總結
---

# 最後總結

- 👀 **錢包不要藏**：監控是基礎
- 🔍 **工具聰明用**：開啟 Tool Search，善用 Sub-agents
- 🧹 **大腦要排毒**：該 /clear 就 /clear
- 🔪 **分工要明確**：把好鋼用在刀刃上
- 🛑 **拒絕鬼打牆**：苗頭不對立刻停

---
layout: center
class: text-center
---

# 下回預告

# Claude Code 社群好物，那些你可能錯過的必看開源專案推薦

就像玩神裝 RPG，大神都怎麼配裝？
下次分享一些好用的開源工具配置！