# 常態開啟的獨立頁面

這個儲存庫用來放需要長期公開的小型靜態頁面。每個頁面一個資料夾,彼此獨立,用 GitHub Pages 發布。根目錄刻意不放入口頁。

## 頁面清單

| 資料夾 | 內容 | 加入日期 | 網址 |
|---|---|---|---|
| `newmath-intro/` | DINO AI 新課綱數學 · 特色介紹(中英文切換、預錄語音) | 2026-11-16 | `https://claudecat30-sys.github.io/dino-ai-pages/newmath-intro/` |
| `science-intro/` | DINO AI 課綱自然科學小學堂 · 特色說明(中英文切換、預錄語音) | 2026-11-16 | `https://claudecat30-sys.github.io/dino-ai-pages/science-intro/` |
| `zhuyin-intro/` | 迪諾玩注音看世界(中英雙語版) · 功能介紹(繁體、台灣讀音、預錄語音) | 2026-11-17 | `https://claudecat30-sys.github.io/dino-ai-pages/zhuyin-intro/` |
| `pinyin-intro/` | 迪诺玩拼音看世界(中英双语版) · 功能介绍(簡體、大陸讀音、預錄語音) | 2026-11-17 | `https://claudecat30-sys.github.io/dino-ai-pages/pinyin-intro/` |

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

- `index.html`:中文頁。`en.html`:英文頁(網址 `.../science-intro/en.html`)。兩頁各分「動畫版」與「閱讀版」兩個分頁。
- 語言切換:動畫版在底部控制列、閱讀版在上方分頁按鈕列各有一個切換按鈕,連到另一個語言的頁面,並帶著目前的分頁與幕次(網址後面的 `#read`、`#s5`)。兩個檔名不要改,否則按鈕會失效。
- `audio/`:186 句預錄語音(mp3,中文 93、英文 93)與索引 `index.js`,兩頁共用。兩個 html 和 `audio/` 必須在同一層。
- 語音:中文的 DINO 老師與閱讀版朗讀為 Azure `zh-TW-HsiaoChenNeural`,小明為 `zh-TW-YunJheNeural`(語速加快 4%、音調加高 18%);英文為 `en-US-SaraNeural`(語速放慢 20%),小明為 `en-US-DustinMultilingualNeural`(語速放慢 8%、音調加高 12%)。英文頁的「中文翻譯」朗讀沿用中文音檔。找不到音檔的句子會退回瀏覽器內建語音。
- 動畫版每句對話是一個完整音檔,字幕依播放進度換段。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:頁面會在第一次觸碰畫面時解鎖音訊(頁面裡標記為 `iOS-voice-fix-v2` 的區塊)。**尚未在實機上測試。**
- 音檔沒有逐句人工試聽。

## zhuyin-intro、pinyin-intro

- 各只有一個檔案 `index.html`:圖片與語音全部內嵌(每個約 17 MB),沒有 `audio/` 資料夾。兩個資料夾互不相依。
- 每頁分「閱讀版」與「動畫版」兩個分頁,右上角切換。閱讀版點說明文字或對話就會朗讀,再點一次停止。
- 語音:每頁 123 段預錄 mp3(標題 18、對話 87、說明 18),全部用 Azure 語音服務預先錄好。`zhuyin-intro` 為 `zh-TW-HsiaoChenNeural`(台灣讀音),`pinyin-intro` 為 `zh-CN-XiaoxiaoNeural`(大陸讀音);迪諾老師用原音高,小安用同一個聲音把音高調高 15 個百分點。
- **頁面不使用瀏覽器內建語音**:錄音放不出來時只會無聲地照時間往下走。
- 動畫版一個人講的一整段是一個音檔,字幕依播放進度換行。
- 多音字逐處指定讀音(注音版依《國語一字多音審訂表》按當下用法判斷);注音符號與拼音字母照畫面顯示、錄音唸對應的音。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:頁面會在第一次觸碰畫面時解鎖音訊。**尚未在實機上測試。**
- 語音由使用者試聽過兩版(2026-11-17)。
