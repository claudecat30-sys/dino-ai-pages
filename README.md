# 常態開啟的獨立頁面

這個儲存庫用來放需要長期公開的小型靜態頁面。每個頁面一個資料夾,彼此獨立,用 GitHub Pages 發布。根目錄刻意不放入口頁。

## 頁面清單

| 資料夾 | 內容 | 加入日期 | 網址 |
|---|---|---|---|
| `newmath-intro/` | DINO AI 新課綱數學 · 特色介紹(中英文切換、預錄語音) | 2026-11-16 | `https://claudecat30-sys.github.io/dino-ai-pages/newmath-intro/` |
| `science-intro/` | DINO AI 課綱自然科學小學堂 · 特色說明(中文、預錄語音) | 2026-11-16 | `https://claudecat30-sys.github.io/dino-ai-pages/science-intro/` |

## 發布設定

1. 儲存庫設為公開。
2. Settings → Pages:來源選 `main` 分支、根目錄(`/`)。
3. 推上去後一兩分鐘內上線。

`.nojekyll` 讓 Pages 原樣發布檔案,不要刪。`.gitattributes` 讓 git 不更動檔案的換行與音檔內容,也不要刪。

## 新增頁面的規則

- 一個頁面一個資料夾,入口檔名固定為 `index.html`。
- 資料夾名稱用英文小寫加連字號。它就是網址的一部分,上線後不要改名,否則已發出去的連結會失效。
- 頁面用到的圖片、音檔都放在自己的資料夾裡,以相對路徑引用,不要引用其他儲存庫或其他資料夾的檔案。
- 這個儲存庫是公開的:原始檔、錄音工具、API 金鑰都不要放進來。
- 整個儲存庫建議維持在 1 GB 以內(GitHub Pages 的建議上限)。
- 新增後在上面的清單補一列。

## newmath-intro

- `index.html`:頁面本體。右上角的按鈕切換中文與英文,也可以用網址參數指定語言:`?lang=zh`、`?lang=en`。
- `audio/`:224 句預錄語音(mp3)與索引 `index.js`。`index.html` 和 `audio/` 必須在同一層。
- 語音:中文為 Azure `zh-TW-HsiaoChenNeural`(學生為 `zh-TW-YunJheNeural`,音調加高 18%),英文為 `en-US-SaraNeural`(學生為 `en-US-DustinMultilingualNeural`,音調加高 12%)。找不到音檔的句子會退回瀏覽器內建語音。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:頁面會在第一次觸碰畫面時解鎖音訊(頁面裡標記為 `iOS-voice-fix-v2` 的區塊)。**尚未在實機上測試。**
- 音檔沒有逐句人工試聽。

## science-intro

- `index.html`:頁面本體,只有中文。分「動畫版」與「閱讀版」兩個分頁。
- `audio/`:93 句預錄語音(mp3)與索引 `index.js`。`index.html` 和 `audio/` 必須在同一層。
- 語音:DINO 老師與閱讀版朗讀為 Azure `zh-TW-HsiaoChenNeural`,小明為 `zh-TW-YunJheNeural`(語速加快 4%、音調加高 18%)。找不到音檔的句子會退回瀏覽器內建語音。
- 動畫版每句對話是一個完整音檔,字幕依播放進度換段。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:頁面會在第一次觸碰畫面時解鎖音訊(頁面裡標記為 `iOS-voice-fix-v2` 的區塊)。**尚未在實機上測試。**
- 音檔沒有逐句人工試聽。
