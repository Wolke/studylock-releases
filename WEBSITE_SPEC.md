# 學霸鎖（StudyLock）APK 下載網站 — 規劃文件（Agent 交接用）

> 目標：做一個**單頁式官方下載網站**，讓家長直接下載 APK 側載安裝（不經 Play 商店）。
> 本文件自包含，所有素材路徑、文案、下載連結、校驗碼都在文件內。

---

## 1. 核心資訊（直接使用，勿改）

| 項目 | 值 |
|---|---|
| App 名稱 | 學霸鎖（英文：StudyLock） |
| 一句話標語 | 答對數學題，贏得使用時間！ |
| **APK 下載連結（永久指向最新版）** | `https://github.com/Wolke/studylock-releases/releases/latest/download/StudyLock.apk` |
| 目前版本 | v1.0（1.0 MB） |
| SHA-256 | `a1e783b1c6258e06f59bbf5b0b3a34909ad768b45fd04f5d6c3bd58d331bc3f2` |
| 隱私權政策 | `網站內的 privacy.html 頁面（見本 repo privacy.html）` |
| 系統需求 | Android 8.0（API 26）以上 |
| 主色 | Indigo `#283593`（配色可參考 feature graphic） |

## 2. 素材（本機路徑）

目錄：`本 repo 的 assets/ 資料夾`

| 檔案 | 用途 |
|---|---|
| `play_icon_512.png` | Logo / favicon 來源（512×512） |
| `feature_graphic.png` | Hero 區背景或主視覺（1024×500） |
| `screenshot_home.png` | 截圖①：主畫面（倒數計時） |
| `screenshot_lock.png` | 截圖②：鎖定答題畫面 |
| `screenshot_scratchpad.png` | 截圖③：手寫計算板 |

## 3. 頁面結構（單頁，由上到下）

1. **Hero**：icon + 「學霸鎖」+ 標語 + 大型下載按鈕（顯示版本號與檔案大小）+ 「Android 8.0+」徽章
2. **這是什麼**：3 句話介紹（文案見第 4 節）
3. **功能特色**：6 個卡片（⏱ 計時鎖定、✍️ 手寫計算板、🎟 快速通關券、📚 1–6 年級出題、👨‍👩‍👧 家長 PIN 設定、🔊 趣味音效）
4. **截圖展示**：3 張截圖（手機框裝飾，橫向捲動或並排）
5. **📲 安裝教學**（重要！側載步驟，見第 5 節，做成步驟卡片）
6. **FAQ**（見第 6 節，手風琴摺疊）
7. **隱私與安全**：不聯網、零資料蒐集、無廣告 + SHA-256 校驗碼（等寬字體+複製按鈕）
8. **Footer**：隱私權政策連結、聯絡方式（GitHub issues：`https://github.com/Wolke/studylock-releases/issues`）、© 2026

## 4. 文案（複製使用）

**介紹段**：
```
學霸鎖是一款結合「螢幕時間管理」與「數學練習」的家長監護 App。
設定好使用時間後開始倒數，時間到會顯示鎖定畫面——孩子答對數學題目，就能獲得更多使用時間。
完全離線運作、零資料蒐集、無廣告無內購，家長可放心使用。
```

**功能卡片文字**：
- ⏱ 計時鎖定 — 時間用完自動鎖定，答對題目才能繼續使用
- ✍️ 手寫計算板 — 鎖定畫面內建打草稿區，直式計算好方便
- 🎟 快速通關券 — 連續答對指定題數獲得通關券，可直接解鎖一次
- 📚 依年級出題 — 1–6 年級加減乘除，難度自動搭配
- 👨‍👩‍👧 家長設定 — PIN 密碼保護，可調整時間、年級與音效
- 🔊 趣味音效 — 答對、答錯、獲得通關券都有專屬音效（可關閉）

## 5. 安裝教學（側載步驟）

```
1. 用 Android 手機瀏覽器點「下載 APK」
2. 下載完成後開啟檔案，若出現「基於安全考量，不允許安裝不明應用程式」
   → 點「設定」→ 允許「Chrome（或你的瀏覽器）」安裝應用程式
3. 回到安裝畫面，點「安裝」
4. 若 Google Play 安全防護（Play Protect）跳出警告
   → 點「更多詳細資訊」→「仍要安裝」
5. 開啟學霸鎖，依照畫面完成家長設定（PIN、年級、使用時間）即可！
```
> 網站需加註：本 App 僅從本官方頁面發佈，請勿從其他來源下載。

## 6. FAQ 內容

- **Q：為什麼不是從 Google Play 下載？** A：目前以官網直接發佈，APK 由開發者簽章，可用下方 SHA-256 驗證檔案完整性。
- **Q：會蒐集小孩的資料嗎？** A：完全不會。App 無網路權限、所有設定僅存手機本機，詳見隱私權政策。
- **Q：忘記家長 PIN 怎麼辦？** A：解除安裝後重新安裝即可重設（所有設定會清空）。
- **Q：孩子把 App 移除怎麼辦？** A：建議在手機設定中啟用「應用程式鎖」或使用裝置的家長監護功能防止移除。
- **Q：支援哪些 Android 版本？** A：Android 8.0 以上。
- **Q：怎麼更新？** A：回到本頁下載最新版 APK 直接覆蓋安裝（不需移除舊版）。

## 7. 技術需求

- **靜態單頁網站**（純 HTML/CSS/JS 或任何靜態產生器皆可），無後端
- RWD 手機優先（訪客多半用手機開）
- SEO：title「學霸鎖 — 答對數學題，贏得使用時間｜官方 APK 下載」、meta description、Open Graph 標籤（og:image 用 feature_graphic.png）
- 下載按鈕直接連到第 1 節的 GitHub Releases 連結（不要把 APK 放進網站 repo）
- 語言：繁體中文為主（可選配 EN 切換）
- 部署：建議 GitHub Pages（可直接放在 `Wolke/studylock-releases` repo 開 Pages，或新開 repo）；Netlify/Vercel/Cloudflare Pages 亦可
- 效能：截圖請壓縮（WebP 佳），整頁 < 2MB

## 8. 之後發新版時（給維護者）

1. `versionCode`+1 → `./gradlew :app:assembleRelease`
2. `gh release create v1.X app-release.apk#StudyLock.apk -R Wolke/studylock-releases --title "學霸鎖 v1.X" --notes "更新內容 + 新 SHA-256"`
3. 網站上的「最新版」連結不用改（latest 自動指向），只需更新版本號與 SHA-256 文字
