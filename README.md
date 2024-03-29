# project-Teaching-Material
針對台東高中網頁學習所準備教材，裡面包含兩個小項目：guess number,，Dice Dash，使用Html，CSS，JS所完成。

## project 1 guess number
這個猜數字遊戲是為高中學生設計的網頁學習教材，它使用了以下的技術：
![image](https://github.com/kcwc1029/project-Teaching-Material/blob/main/image001.png)
- HTML：使用 HTML5（Hypertext Markup Language）標記語言來建立網頁的結構和內容。HTML提供了各種元素，如標題、段落、按鈕和輸入框，用於建立網頁的外觀和佈局。
- CSS：使用 CSS3（Cascading Style Sheets）設定網頁的樣式和外觀。CSS提供了許多樣式屬性，例如顏色、字體、邊框和背景，用於美化和設計網頁元素的外觀。
- JavaScript：使用 JavaScript 編寫遊戲的邏輯和互動功能。JavaScript 是一種用於網頁交互的程式語言，可以操作網頁元素、處理事件、執行數學計算等。在這個猜數字遊戲中，JavaScript 主要用於生成隨機數字、處理使用者的輸入、顯示回饋訊息、更新分數和紀錄最高分數等。
- 互動事件：使用 JavaScript 監聽按鈕點擊事件和輸入框的輸入事件，以捕捉使用者的操作。當學生點擊 "Check" 按鈕時，JavaScript 會獲取學生輸入的數字並進行相應的處理和回饋。同樣地，當學生點擊 "Again!" 按鈕時，JavaScript 會重置遊戲並重新生成一個隨機數字。
- 動態元素：使用 JavaScript 控制 HTML 元素的內容和樣式。遊戲中的元素，如回饋訊息、分數、最高分數和隨機數字等，都是通過 JavaScript 動態更新的。當學生猜測正確數字時，JavaScript 會修改相應的元素內容和樣式，例如顯示正確數字、變更背景顏色等。
- 隨機數字生成：使用 JavaScript 的 Math 物件和相應的函式生成介於 1 到 100 之間的隨機數字。Math.random() 函式生成 0 到 1 之間的隨機小數，然後通過乘法和加法運算獲得所需的隨機數字範圍。
![image](https://github.com/kcwc1029/project-Teaching-Material/blob/main/image002.png)
![image](https://github.com/kcwc1029/project-Teaching-Material/blob/main/image003.png)

這個教材通過結合 HTML、CSS 和 JavaScript，讓高中學生能夠學習和瞭解網頁開發的基礎概念和技術。通過實際編寫遊戲的程式碼，學生可以體驗到如何使用不同的語言和技術來創建互動性和可視化效果。此教材旨在培養學生的邏輯思維、問題解決能力和創造力，同時提供一個有趣且互動的學習環境。

---

## project 2 Dice Dash
### 遊戲玩法:
當玩家擲骰子時，遊戲的玩法如下：

遊戲開始時，兩位玩家的分數都為 0。
玩家輪流進行回合。
每個回合中，玩家可以點擊 "Roll dice" 按鈕來擲骰子。
擲骰子會隨機生成介於 1 到 6 的數字。
如果擲出的數字不是 1，則該數字會被加到玩家的目前分數中。
玩家可以選擇繼續擲骰子來增加目前分數，或者按下 "Hold" 按鈕來將目前分數加到總分中並結束回合。
如果玩家擲出的數字是 1，則目前分數將被重設為 0，並換另一位玩家進行回合。
遊戲的勝利條件是當一位玩家的總分達到或超過 20 時，該玩家獲勝。
當遊戲結束時，將宣布獲勝的玩家。
此外，遊戲還提供以下功能按鈕：

"New game"：開始一局新的遊戲，重新初始化分數和遊戲狀態。
"Roll dice"：擲骰子，隨機生成數字並進行遊戲操作。
"Hold"：將目前分數加到總分中並結束回合。
玩家需要謹慎考慮每次擲骰子的機會，以及何時保留目前的分數並將其加到總分中。適時的決策和風險管理是獲勝的關鍵策略。

### 針對專案中JavaScript 部分主要實現:
![image](https://github.com/kcwc1029/project-Teaching-Material/blob/main/image004.png)
- 選取元素：使用 document.querySelector 和 document.getElementById 方法選取 HTML 元素。這些選取器允許我們透過 CSS 選擇器的語法來找到特定的元素，並將它們存儲在變數中供後續使用。
- 遊戲初始化：init 函數用於初始化遊戲的起始條件，包括重置分數、設置玩家和遊戲狀態等。
- 切換玩家：switchPlayer 函數用於切換玩家。當玩家擲骰子得到 1 時，該函數將清零當前分數並將控制權交給下一個玩家。
![image](https://github.com/kcwc1029/project-Teaching-Material/blob/main/image005.png)
- 擲骰子功能：btnRoll 的點擊事件監聽器處理擲骰子的功能。它生成一個隨機數字表示骰子的點數，並將該數字顯示在介面上。如果骰子點數不為 1，則將點數加到當前分數中；如果當前分數超過 20，則將該玩家的得分增加 1。
- "Hold" 按鈕功能：btnHold 的點擊事件監聽器處理 "Hold" 按鈕的功能。它將當前分數添加到玩家總分中，並檢查是否達到獲勝條件。如果玩家總分達到或超過 20，則該玩家獲勝並結束遊戲；否則切換到下一個玩家。
- "New game" 按鈕功能：btnNew 的點擊事件監聽器處理 "New game" 按鈕的功能。它調用 init 函數重置遊戲的起始條件，準備開始一場新遊戲。
- 變數與狀態追蹤：使用變數來追蹤遊戲中的不同狀態，例如玩家的得分、當前分數、當前玩家、遊戲進行狀態等。這些變數在遊戲進程中被更新和使用。
