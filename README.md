# 企業投資架構與營所稅風險決策地圖 — Netlify 部署包

## 資料夾內容
- `index.html`：網頁主檔（事務所名稱、LOGO、LINE、門檻參數都在檔案下方的 `CONFIG` / `RULES`）
- `assets/tailwind.css`：已預先編譯的樣式
- `assets/alpine.min.js`：互動功能程式庫（Alpine.js 3.14.1）
- `netlify.toml`：Netlify 設定

## 部署方式（最簡單）
1. 開啟 https://app.netlify.com/drop
2. 把整個 `netlify-site` 資料夾（或 `netlify-site.zip`）拖進網頁
3. 完成後可在 Site settings 修改網址名稱或綁定自有網域

## 修改內容後
- 只改 `CONFIG`、`RULES` 內的文字或數字：直接重新上傳即可。
- 若新增了**原本沒用過的 Tailwind class**，樣式不會生效（因為 CSS 已預先編譯）。
  這時請暫時把 `index.html` 內的
  `<link rel="stylesheet" href="assets/tailwind.css" />`
  換成 `<script src="https://cdn.tailwindcss.com"></script>`，或請工程師重新編譯。
