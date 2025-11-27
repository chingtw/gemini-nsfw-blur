# 🛡️ Gemini NSFW Blur - Smart Privacy Shield

![Demo](https://drive.google.com/uc?export=view&id=16eDFY3igOma9daPzQH4jfAPmCzZ16moD "Demo")

這是一個專為 **Google Gemini** 網頁版設計的瀏覽器擴充功能（Chrome / Edge）。

它能自動將側邊欄的 **My Stuff (我的內容)** 以及內頁的 **圖片卡 (Library Cards)** 加上高質感的模糊濾鏡與 NSFW 警示遮罩。採用「長按解鎖」機制，防止滑鼠誤觸，保護你的隱私，避免敏感圖片直接暴露在螢幕上。

## ✨ 主要功能

* **⏳ 長按解鎖 (Hold to View)**：
    * 為了防止誤觸，採用 **5 秒延遲解鎖** 機制。
    * 滑鼠懸停時，底部會出現 **藍色讀取條**，讀取完畢後自動解除模糊並顯示內容。
    * 若中途移開滑鼠，進度條會歸零並保持遮蔽狀態。
* **📂 側邊欄智慧折疊**：
    * 側邊欄 (`my-stuff-recents-preview`) 預設強制折疊為 **50px** 高度，保持介面整潔。
    * 長按解鎖後，會自動向下展開完整內容。
* **🖼️ 全面圖片防護**：
    * 支援主畫面與列表中的 `library-item-card` 圖片卡模糊。
    * **智慧排除機制**：若圖片卡位於側邊欄內，會自動取消雙重遮罩，避免視覺衝突。
* **🎨 精緻視覺設計**：
    * **通用配色**：採用半透明深灰底色搭配白色 Eye-Slash 圖示與 "NSFW TO VIEW" 字樣。
    * **柔化邊界**：結合圓角 (Border Radius) 與內陰影 (Inset Shadow)，完美融入介面。
    * **輕量化**：純 CSS 實現所有動畫與邏輯，不佔用記憶體與運算資源。

## 📂 檔案結構

專案資料夾應包含以下檔案：

* `manifest.json` - 擴充功能的設定檔（定義權限與目標網站）。
* `style.css` - 核心樣式表（包含折疊、模糊、長按延遲邏輯）。
* `icon.png` - 擴充功能圖示 (建議 128x128)。
* `README.md` - 專案說明文件。

## 🚀 安裝教學

由於此擴充功能為個人開發工具，請使用瀏覽器的「開發人員模式」進行安裝：

1.  **準備檔案**：
    * 將 `manifest.json`, `style.css` 放入一個資料夾（例如命名為 `gemini-nsfw-blur`）。
    * 確保資料夾內有產生的 `icon.png` 圖示檔。
2.  **開啟擴充功能管理頁面**：
    * **Chrome**: 在網址列輸入 `chrome://extensions` 並按下 Enter。
    * **Edge**: 在網址列輸入 `edge://extensions` 並按下 Enter。
3.  **啟用開發模式**：
    * 開啟頁面右上角的 **「開發人員模式」 (Developer mode)** 開關。
4.  **載入擴充功能**：
    * 點擊左上角的 **「載入未封裝項目」 (Load unpacked)** 按鈕。
    * 選擇你的 `gemini-nsfw-blur` 資料夾。
5.  **完成！**
    * 回到 [gemini.google.com](https://gemini.google.com) 並重新整理頁面 (F5)，即可看到效果。

## 🛠️ 自定義調整

如果你想調整參數（例如覺得 5 秒太久），可以開啟 `style.css` 修改：

* **調整等待時間**：搜尋 `5s`，將所有出現的 `5s` 改為你想要的秒數（例如 `2s`）。
* **調整模糊程度**：修改 `backdrop-filter: blur(5px);` 中的數值。
* **調整遮罩顏色**：修改 `background-color: rgba(10, 10, 10, 0.6);`。
* **調整進度條顏色**：修改 `background-color: #3586FE;`。

## 📜 License
此專案僅供個人學習與使用。
