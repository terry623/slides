---
author: Terry Lin
theme: default
background: https://cover.sli.dev?title=claude-code-token
title: Claude Code 省 Token 的五大心法
drawings:
  persist: false
transition: slide-left
---

# Claude Code 省 Token 的五大心法

---

心法一：讓餘額一目瞭然

善用可視化工具，不用刻意查帳

「去日本鄉下玩時，如果你把錢包放在容易拿的地方，餘額一眼就能掃到，心裡自然就有底，不用神經兮兮地一直數錢。」

把檢查變直覺：

重點不是要你一直「盯著」，而是把數據放在抬頭就能看見的地方。

---

監控三招 (由輕鬆到精確)：

想確認時再查：真的不確定時，再用 Skill 指令查詢 (推薦推廣 skills/IT Repo)。

操作時順便看：Terminal 的 Status Line (狀態列) 本來就有，養成「餘光掃描」的習慣。

隨時都想知道：推薦裝個 Mac Menu Bar App (如 BarRaider)，餘額直接顯示在頂端，瞄一眼就好。

---

心法二：工具聰明用

解決 MCP 工具太肥的問題

問題在哪？

舊版機制像「塞爆行李箱」：每加一個 MCP Server，不管用不用，大量定義先塞進去再說。

結果：還沒開始做事，Token 就先被吃掉一大半。

---

解法：工具搜尋 (Tool Search)：

原理：Agent 變聰明了，它只帶一個「搜尋器」。

流程：當它覺得「我現在需要檢查 Sentry」時→ 才去搜尋並載入那個工具。

設定：記得去設定開啟 ENABLE_TOOL_SEARCH。

---

大絕招：子代理 (Sub-agents)：

遇到像「重寫整個登入系統」這種超大任務。

開個分身 (Sub-agent) 去做，做完回來回報，別把主線程的記憶體撐爆。

---

心法三：記憶斷捨離

保持大腦乾淨，不要囤積垃圾

黃金原則：一事一結 (One Task, One Session)

一個會話只解決一個任務，解決完就果斷重開，不要留戀。

---

清理指令：

/clear：直接清空大腦，重新開始（最省錢，推薦）。

/compact：把回憶壓縮成摘要（折衷方案）。

餵資料的藝術：漸進式揭露

Claude.md 或專案文件，不要一次全塞給它。

像擠牙膏一樣，做到哪裡，給相關的背景就好。

---

心法四：找對人做對事

殺雞焉用牛刀，把好鋼用在刀刃上

分工合作：

大腦擔當 (Plan Mode)：用 Claude 3.5 Opus。它最聰明，負責把路徑想清楚。

手腳擔當 (Act Mode)：用 Claude 3.5 Sonnet。它寫 Code 快又比較便宜。

打雜擔當：簡單雜事用便宜小模型 (如 Haiku)。

---

心法五：拒絕鬼打牆

避免陷入「修改 -> 報錯」的地獄輪迴

什麼是鬼打牆？

Claude 寫程式 -> 報錯 -> Claude 修正 -> 又報錯 -> Claude 再修正...

這就是「Token 焚化爐」，通常是因為一開始就搞錯方向。

---

如何避免？

先想再做 (Plan Mode)：強迫它先寫計畫，不要急著寫 Code。

一次講清楚 (One-shot Prompting)：

背景、需求、限制，在第一個 Prompt 就全部講完。

不要像擠牙膏一樣你一句我一句，多餘的對話都是錢。

---

主動喊卡：

一旦發現 Claude 開始鬼打牆，馬上按停止。

糾正它，或者重開一個 Session，不要期待它會自己變聰明。

---

總結

- 省 Token 就是省錢，更是省時間

- 讓餘額一目瞭然：監控是基礎。

- 工具聰明用：開啟 Tool Search。

- 記憶斷捨離：善用 /clear。

- 找對人做對事：Opus 想，Sonnet 做。

- 拒絕鬼打牆：苗頭不對立刻停。

隨時保持工具的更新！

祝大家的 Claude Code 之路，錢包不再破洞！
指令：cch update && claude update

---

下回預告：

Claude Code 開源工具分享

- 就像玩電動的時候，通常會去看網路上的大神，配自己的裝備這樣。分享一些配到自己的專案之中