# Firebase Google 登入

`index.html` 已連接 Firebase 專案 `daymark-efc26` 的 Web App，使用 Firebase Authentication Google provider 進行登入與登出。Google provider 已在 Firebase Console 啟用，支援聯絡地址使用專案所有者指定的地址，GitHub Pages 網域 `yellow-blip.github.io` 已列入 Authentication 授權網域。

登入功能只處理身份驗證；行程與任務仍是頁面內的範例資料，尚未保存到 Firestore，也沒有以登入狀態限制資料存取。Firebase Web App config 是前端公開設定；請在 Google Cloud/Firebase 將 API key 限制為允許的網站來源，並在未來加入資料庫時設定 Firestore Security Rules。

若本機測試，請以 HTTP 開發伺服器開啟網站，並在 Firebase Authentication 的授權網域加入 `localhost`。不要用 `file://` 開啟，因為 Firebase 模組需要 HTTPS 或 localhost origin。
