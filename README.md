# GitHubCopilot
GitHub Copilot 進階實戰開發【由 GitHub 與 OpenAI 共同開發的 AI 程式設計助手，透過人工智慧技術，為開發者帶來高效率且智慧化的程式開發體驗】  

# Licensing (可以看一下免費版的使用限制)
[Licensing](./docs/Licensing.md)  

# (GitHub Copilot 【自訂指令與行為設定】)類似 Cline 的 .clinerules 功能
[codeGeneration](./docs/codeGeneration.md)  
Rules 的設定可以參考 VSCode 的 Cline Rules 套件  
Cline Rules 套件中文說明文件網址: https://github.com/henryalps/vscode-clinerules/blob/HEAD/README-cn.md  

# GitHub Copilot "@" 與 "#" 前綴指令有很多重複，到底差異在哪？
- @ 前綴就像是 Copilot 的「行動召喚」，用來指揮它幹活，比如 @edit、@explain、@test 等，這些是功能性指令，會讓 Copilot 幫你改程式碼、解釋邏輯、甚至寫測試。

- # 前綴則像是「話題標籤」，用來告訴 Copilot 你在聊什麼，比如 #python、#bug、#question，這些是分類標籤，幫助 Copilot 知道你的問題屬於哪個領域，但不會讓它直接動手。

簡單來說：

@：叫 Copilot 幹活（功能指令）  
#：告訴 Copilot 你在聊啥（分類標籤）  
兩者搭配使用，能讓 Copilot 更懂你，效率更高！

## 舉例說明
`#terminalLastCommand` 和 `@terminal` 看起來像雙胞胎，怎麼分清楚？

這兩個指令在 GitHub Copilot Chat 的用途完全不同：

- `@terminal`  
這是功能性指令，等於對 Copilot 說：「幫我寫個指令吧！」例如：  
@terminal 如何啟動 Flask？  
Copilot 會告訴你該在終端機輸入什麼，還會貼心解釋用途。

- `#terminalLastCommand`  
這是標籤指令，等於對 Copilot 說：「剛剛那行指令是啥意思？」例如：  
#terminalLastCommand 這個指令有什麼作用？  
Copilot 會幫你分析剛剛執行的那行指令，讓你秒懂。

總結：

@terminal：讓 Copilot 幫你寫或解釋指令。  
#terminalLastCommand：讓 Copilot 解釋你剛剛執行的指令。  
一個是「主動幫忙」，一個是「回頭解釋」，各司其職，互不搶戲！