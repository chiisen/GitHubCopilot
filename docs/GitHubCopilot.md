## GitHub Copilot Chat 中「#」與「@」指令完整說明

### 指令：上下文與程式碼區段引用

「#」用於讓 Copilot Chat 精確引用專案中的特定內容，進而聚焦於你想討論、解釋或修改的區域。它可用於：

- 指定檔案：`#MyFile.cs`
- 指定檔案特定行數：`#MyFile.cs:66-72`
- 指定類別、方法、函式等：`#AddItemToBasket`
- 同時引用多個檔案或符號：`#MyFile.cs #MyFile2.cs`

**支援的聊天變數**（依 IDE 可能略有不同）：

| 變數         | 說明                           |
|--------------|--------------------------------|
| `#block`     | 當前程式碼區塊                 |
| `#class`     | 當前類別                       |
| `#comment`   | 當前註解                       |
| `#file`      | 當前檔案內容                   |
| `#function`  | 當前函式或方法                 |
| `#line`      | 當前程式碼行                   |
| `#path`      | 檔案路徑                       |
| `#project`   | 專案上下文                     |
| `#selection` | 當前選取的文字                 |
| `#sym`       | 當前符號                       |

**範例**：

- `解釋 #MyFile.cs:66-72 這段程式碼的作用`
- `#BasketService.cs 中的測試在哪裡？`
- `#TestCalculator 測試方法如何確保正確執行？`
- `#BasketService 和 #OrderService 類別有何不同？`

---

### **@ 指令：範圍、資源與專家參與者引用**

「@」用於指定查詢的範圍、資源來源，或引入特定的「聊天參與者」來協助回答問題。常見用途如下：

- `@workspace`：引用目前 IDE 開啟的整個工作區（專案、所有檔案與設定），讓 Copilot Chat 能針對整個專案搜尋與回答。
- `@github`：針對 Copilot Enterprise，用於引用整個 GitHub 存放庫內容，並可啟用 Web 搜尋（需管理員啟用）。
- `@project`：讓 Copilot 以整個專案為上下文，考慮所有檔案。
- 其他參與者（如特定插件或自定義專家）

**範例**：

- `此 @workspace 中是否有 delete basket 方法？`
- `在我的 @workspace 中，#AddItemToBasket 在哪裡？`
- `@github 搜尋所有與 payment 相關的 class`
- `@project 幫我產生專案文件`

---

### **組合用法**

你可以結合「#」與「@」來精確指定查詢範圍與內容，例如：

- `請在 @workspace 中解釋 #BasketService.cs 的 #AddItemToBasket 方法`
- `@github 幫我檢查 #api/routes/payment.js 的安全性`

---

### **補充說明**

- 「#」與「@」指令可在 Copilot Chat 視窗、VS Code、Visual Studio 等多種 IDE 使用，依環境支援的變數與參與者略有差異。
- 若要查看所有可用的聊天變數與參與者，建議於聊天框分別輸入「#」或「@」以獲得即時建議。
- 這些指令能大幅提升 Copilot Chat 的精準度與效率，特別適合大型專案、多人協作或需快速定位程式碼時使用。

---

