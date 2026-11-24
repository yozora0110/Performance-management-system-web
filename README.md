# 成發表演曲目管理系統 Web

純前端 HTML / CSS / JavaScript，無需安裝套件。開啟 index.html 即可操作；建議使用現代 Chrome 或 Edge。

## 功能
總覽、Battle 專區、表演者精確姓名查詢、團體模糊查詢、原定人數篩選、TXT / CSV 匯入預覽、曲目 CRUD、匯出、深淺色主題、響應式版面、LocalStorage 本機儲存。

v1.3 使用新的本機儲存鍵，首次開啟必定空白，不讀取舊版曲目。自行匯入後仍會保存資料，可在匯入頁清空。已移除示範資料與載入按鈕。更新前請先匯出舊版需要保留的曲目。

## 匯入
使用 UTF-8（可含 BOM）。TXT 每行 `團體-曲目/原定人數/姓名、姓名`，第一個連字號為團體與曲目分隔符。CSV 支援四欄（團體名稱、曲目名稱、原定人數、報名名單），可有欄名或依固定順序無欄名，支援雙引號及引號內逗號。姓名以頓號、逗號、分號或換行分隔，同曲目重複姓名會去除。匯入可選擇取代或追加資料，格式錯誤時不允許確認。

## 部署 GitHub Pages
1. 建立公開 repository，例如 Performance-management-system-web。
2. 將本資料夾內檔案上傳到 repository 根目錄，確定 index.html 位於根目錄。
3. Settings → Pages → Build and deployment → Deploy from a branch。
4. 選 main 與 / (root)，按 Save。
5. 在 Pages 查看部署網址與狀態。

## 限制
資料存在目前瀏覽器與網站來源，不跨裝置同步；清除網站資料可能遺失，請定期匯出備份。公開 repository 不要放真實名單。TXT 格式不適用於含保留分隔符的欄位，請改用 CSV。CSV 匯出拒絕疑似試算表公式的文字欄位。未包含後端、帳號或多人同步。

## v1.2 歌曲分類
支援幹部舞、大群歌、老人舞，舊資料預設未分類。各頁可依類型篩選，編輯可修改類型。TXT 可在名單後追加 `/幹部舞`；CSV 可新增第五欄 `歌曲類型`。舊格式仍支援，可在匯入時指定預設類型；匯出保留分類。追加匯入不會自動合併重複曲目。

### 網頁版線上體驗

[點此前往成發表演曲目管理系統 Web 版本](https://yozora0110.github.io/Performance-management-system-web/)
