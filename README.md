# 家庭血壓紀錄

純前端的血壓紀錄工具，放在 GitHub Pages 就能用手機或電腦打開。

## 功能

- 記錄收縮壓、舒張壓、脈搏（選填）、量測時間、備註
- 多位使用者切換（預設「爸爸」「媽媽」，可改名、新增，至少保留兩位）
- 應用程式內顯示血壓趨勢曲線（7 天 / 30 天 / 90 天 / 全部）
- 匯出 Excel：每位使用者一個工作表，加上統計摘要
- 匯出 PPT 簡報：封面、統計摘要、趨勢曲線圖（可在 PowerPoint 內編輯）、量測明細
- 備份 / 還原（JSON）

## 部署到 GitHub Pages

1. 登入 GitHub，按右上角「+」→「New repository」，名稱例如 `bp-tracker`，選 Public，建立。
2. 在新 repo 頁面按「Add file」→「Upload files」，把 `index.html` 和 `README.md` 拖進去，按「Commit changes」。
3. 進入 repo 的「Settings」→ 左側「Pages」。
4. 「Source」選「Deploy from a branch」，Branch 選 `main`、資料夾選 `/ (root)`，按 Save。
5. 約 1–2 分鐘後，網址會出現在同一頁：`https://你的帳號.github.io/bp-tracker/`

手機可以用瀏覽器的「加入主畫面」，就會像 App 一樣有圖示。

## 資料存放說明

- 資料存在**各自裝置的瀏覽器**（localStorage），不會上傳到 GitHub，別人看不到你的血壓。
- 相對地，不同裝置之間的資料不會自動同步。換裝置時用「備份資料」下載 JSON，再到新裝置按「還原備份」。
- 清除瀏覽器資料或使用無痕模式會導致資料遺失，請定期備份。

## 使用的套件（CDN 載入）

- Chart.js 4.4.1 — 曲線圖
- SheetJS 0.18.5 — Excel 匯出
- PptxGenJS 3.12.0 — PowerPoint 匯出

## 血壓分級（AHA 標準，僅供參考）

| 分級 | 收縮壓 | | 舒張壓 |
|---|---|---|---|
| 正常 | < 120 | 且 | < 80 |
| 血壓偏高 | 120–129 | 且 | < 80 |
| 高血壓第一期 | 130–139 | 或 | 80–89 |
| 高血壓第二期 | ≥ 140 | 或 | ≥ 90 |
| 高血壓危象 | > 180 | 或 | > 120 |
