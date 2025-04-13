Create by claude

我已經根據您的要求修改了網頁，現在它可以處理以逗號分隔的單字，並從括號中提取答案。主要變更如下：

1. **匯入格式更新**：
   - 調整了提示信息，明確說明需要以逗號分隔，答案放在括號中
   - 更新了示例：`焦る（あせる）, 慌てる（あわてる）, 疑う（うたがう）`

2. **解析邏輯改進**：
   - 使用正則表達式匹配括號內容作為答案
   - 格式為：主詞（答案）
   - 例如：從 `焦る（あせる）` 中提取 `焦る` 作為題目，`あせる` 作為答案

3. **界面文字調整**：
   - 將測驗模式的選項從「單字→解釋」修改為「詞→讀音」
   - 將「解釋→單字」修改為「讀音→詞」
   - 錯誤信息中的「無解釋」改為「無答案」

使用方法保持不變：
1. 在文本框中輸入您的單字表，格式為：`焦る（あせる）, 慌てる（あわてる）, 疑う（うたがう）`
2. 點擊「匯入單字」按鈕
3. 系統會自動切換到測驗頁面，開始測驗
4. 默認顯示日文單詞，點擊「查看答案」顯示讀音
5. 點擊「下一個」繼續測驗

這個頁面仍然是完全靜態的，所有功能通過JavaScript實現，不需要後端支持。


補充:
可以使用以下的prompt，讓AI生成題目與答案，您也可以對此prompt進行微調，並將其輸入此工具已產生字卡。

   ```
   請設計50道日文單字記憶題目，並依照以下格式輸出，以逗號分隔每道題目：
   
   "題目(答案),題目(答案),題目(答案),..."
   
   每個題目需使用不同的N3程度日文單字。
   請提供50組符合此格式的題目，以便於單字記憶。
   ```

