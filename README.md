# Launchpad｜實習申請工作台

把下一個機會，變成清楚的下一步。

**[開啟網站](https://seankohjs.github.io/internship-tracker/)** · [規格書](SPEC.md) · [修改紀錄](CHANGELOG.md)

## 功能

- 新增、編輯、移除與復原職缺。
- 五種申請狀態、搜尋、組合篩選與排序。
- 待投遞職缺的七日內截止及逾期提醒。
- 履歷、求職信準備清單。
- 個人資料儲存在目前瀏覽器，支援 JSON 匯出與經驗證的合併匯入。
- 獨立的虛構展示模式，支援桌面與手機操作。

## 單一檔案

應用程式全部位於 `index.html`，內含 HTML、CSS、JavaScript 與 SVG 圖示。不使用外部套件、字型 CDN、後端、分析追蹤或 API。

可以直接開啟 `index.html`；為取得一致的瀏覽器儲存行為，建議使用 GitHub Pages 或本機 HTTP 伺服器：

```sh
python3 -m http.server 8000
```

接著開啟 `http://localhost:8000`。

## 資料與備份

第一次開啟提供六筆虛構展示資料；切換「開始我的追蹤」後使用個人清單。資料僅存在瀏覽器的 `launchpad.applications.v1` localStorage，GitHub 儲存庫不包含使用者的申請紀錄。更換瀏覽器、裝置或清除網站資料前，請匯出 JSON。

匯入支援 schemaVersion 1、最多 1,000 筆／2 MB。相同 ID 會更新，其餘資料保留。僅接受 HTTP(S) 職缺網址；使用者輸入以文字呈現。

## GitHub Pages

本專案由儲存庫預設分支 `codex/launchpad` 的根目錄發布，`.nojekyll` 讓單一 HTML 直接作為靜態網頁提供。

## AI 協作與驗證

依使用者選定的主題先建立規格，再由 AI 編寫程式並以真實瀏覽器操作驗證。功能測試包含新增／編輯、儲存、狀態更新、刪除／復原、篩選、匯出／匯入、無效輸入與手機版。實際改進見 [CHANGELOG.md](CHANGELOG.md)。
