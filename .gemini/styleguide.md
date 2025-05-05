# Company X JavaScript Style Guide

## 主要原則

- **可讀性**：程式碼應易於所有團隊成員理解。
- **可維護性**：程式碼應易於修改與擴充。
- **一致性**：全專案遵循統一風格，提升協作效率並減少錯誤。
- **效能**：在可讀性優先的前提下，程式碼應盡可能高效。

## 特定規則

- 行寬上限：100 字元。
- 縮排：每層 2 個空格。
- 匯入/引用順序：內建模組 → 第三方套件 → 專案本地模組，且各組內請依字母排序。
- 命名慣例：
    - 變數與函式：`camelCase`
    - 常數：`UPPER_CASE`
    - 類別與建構式：`PascalCase`
    - 檔案與模組：`kebab-case` 或 `snake_case`
- 註解與文件字串：
    - 所有函式與類別需有 JSDoc 註解。
    - 註解需簡潔明確，說明「為什麼」這麼寫。
- 型別註記：建議使用 TypeScript 或 JSDoc 進行型別註記。
- 錯誤處理：
    - 儘量避免捕捉過於寬泛的錯誤（如 `catch (e)` 無特定處理）。
    - 例外處理需給出明確錯誤訊息。
    - 謹慎使用 `throw`，僅於無法恢復或預期外錯誤時使用。
- Logging：
    - 請使用成熟的日誌函式庫（如 Winston、Pino），避免直接使用 `console.log`。
    - 根據情境選擇適當等級（debug、info、warn、error）。
- 工具：
    - 格式化：建議使用 Prettier。
    - Linter：建議使用 ESLint。

## 進階規則

- 函式內盡量使用衛述句 (Guard Clauses) 提早 `return`，減少巢狀結構。
- 使用 `async/await` 時，在 `await` 呼叫外立即使用 `try...catch` 處理可能發生的錯誤；使用 Promise 時，確實處理 `.catch()`。
- 將魔術數字 (magic numbers) 定義為 `const` 常數，避免直接寫在程式碼中。
- 避免全域變數，盡量使用區域變數（`let`、`const`）。
- 優先使用 `const`，僅在需要重新賦值時使用 `let`。
- 建議使用箭頭函式（arrow function），除非有明確理由需使用傳統函式。
- 模組請使用 ES6 `import/export` 語法。
