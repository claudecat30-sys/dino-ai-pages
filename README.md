# 常態開啟的獨立頁面

這個儲存庫用來放需要長期公開的小型靜態頁面。每個頁面一個資料夾,彼此獨立,用 GitHub Pages 發布。根目錄刻意不放入口頁。

## 頁面清單

| 資料夾 | 內容 | 加入日期 | 網址 |
|---|---|---|---|
| `newmath-intro/` | DINO AI 新課綱數學 · 特色介紹(中英文切換、預錄語音) | 2026-11-16 | `https://claudecat30-sys.github.io/dino-ai-pages/newmath-intro/` |
| `science-intro/` | DINO AI 課綱自然科學小學堂 · 特色說明(中英文切換、預錄語音) | 2026-11-16 | `https://claudecat30-sys.github.io/dino-ai-pages/science-intro/` |
| `zhuyin-intro/` | 迪諾玩注音看世界(中英雙語版) · 功能介紹(繁體、台灣讀音、預錄語音) | 2026-11-17 | `https://claudecat30-sys.github.io/dino-ai-pages/zhuyin-intro/` |
| `pinyin-intro/` | 迪诺玩拼音看世界(中英双语版) · 功能介绍(簡體、大陸讀音、預錄語音) | 2026-11-17 | `https://claudecat30-sys.github.io/dino-ai-pages/pinyin-intro/` |
| `basic-geometry-intro/` | DINO AI 數學 · 基礎幾何 · 功能介紹(繁體 `index.html`、简体 `cn.html`,預錄語音) | 2026-11-18 | `https://claudecat30-sys.github.io/dino-ai-pages/basic-geometry-intro/` |
| `word-hunt-intro/` | 迪諾文字大尋寶 · 特色介紹(繁體、简体、英文、日文共六頁,預錄語音) | 2026-11-25 | `https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/` |
| `sis-teacher-manual-sc/` | See It and Say It 教师手册(简中英,共 12 级;需登入;预录语音尚未上传) | 2026-11-26 | `https://claudecat30-sys.github.io/dino-ai-pages/sis-teacher-manual-sc/` |

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

### 連結

| 用途 | 連結 |
|---|---|
| 中文頁(線上觀看) | https://claudecat30-sys.github.io/dino-ai-pages/science-intro/ |
| 英文頁(線上觀看) | https://claudecat30-sys.github.io/dino-ai-pages/science-intro/en.html |
| 中文頁,直接開閱讀版 | https://claudecat30-sys.github.io/dino-ai-pages/science-intro/#read |
| 英文頁,直接開閱讀版 | https://claudecat30-sys.github.io/dino-ai-pages/science-intro/en.html#read |
| 檔案清單(在 GitHub 上瀏覽) | https://github.com/claudecat30-sys/dino-ai-pages/tree/main/science-intro |
| 下載(整個儲存庫的 ZIP,約 58 MB) | https://github.com/claudecat30-sys/dino-ai-pages/archive/refs/heads/main.zip |
| 儲存庫首頁 | https://github.com/claudecat30-sys/dino-ai-pages |

下載說明:GitHub 沒有只下載單一資料夾的官方連結,ZIP 會包含這個儲存庫的所有頁面。解壓縮後取出 `science-intro` 資料夾即可,裡面的 `index.html`、`en.html`、`audio/` 要保持在同一層。用 git 的人可以執行 `git clone https://github.com/claudecat30-sys/dino-ai-pages.git`。

- `index.html`:中文頁。`en.html`:英文頁(網址 `.../science-intro/en.html`)。兩頁各分「動畫版」與「閱讀版」兩個分頁。
- 語言切換:動畫版在底部控制列、閱讀版在上方分頁按鈕列各有一個切換按鈕,連到另一個語言的頁面,並帶著目前的分頁與幕次(網址後面的 `#read`、`#s5`)。兩個檔名不要改,否則按鈕會失效。
- `audio/`:186 句預錄語音(mp3,中文 93、英文 93)與索引 `index.js`,兩頁共用。兩個 html 和 `audio/` 必須在同一層。
- 語音:中文的 DINO 老師與閱讀版朗讀為 Azure `zh-TW-HsiaoChenNeural`,小明為 `zh-TW-YunJheNeural`(語速加快 4%、音調加高 18%);英文為 `en-US-SaraNeural`(語速放慢 20%),小明為 `en-US-DustinMultilingualNeural`(語速放慢 8%、音調加高 12%)。英文頁的「中文翻譯」朗讀沿用中文音檔。找不到音檔的句子會退回瀏覽器內建語音。
- 動畫版每句對話是一個完整音檔,字幕依播放進度換段。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:頁面會在第一次觸碰畫面時解鎖音訊(頁面裡標記為 `iOS-voice-fix-v2` 的區塊)。**尚未在實機上測試。**
- 音檔沒有逐句人工試聽。

## zhuyin-intro、pinyin-intro

- 每個資料夾有 `index.html`(約 94 KB,只有文字與程式)、`img/`(94 張圖片,約 6.6 MB)、`audio/`(123 段 mp3,約 6 MB)。三者必須在同一層。兩個資料夾互不相依。
- 頁面本體先開,圖片捲到才載入,語音播到哪一段才載入那一段(動畫版會預先載入下一段)。
- 圖片檔名是內容的雜湊值、語音檔名是段落編號(`T00`、`Q000`、`S00`…),由專案的輸出工具產生,不要手動改名。
- 每頁分「閱讀版」與「動畫版」兩個分頁,右上角切換。閱讀版點說明文字或對話就會朗讀,再點一次停止。
- 語音:每頁 123 段預錄 mp3(標題 18、對話 87、說明 18),全部用 Azure 語音服務預先錄好。`zhuyin-intro` 為 `zh-TW-HsiaoChenNeural`(台灣讀音),`pinyin-intro` 為 `zh-CN-XiaoxiaoNeural`(大陸讀音);迪諾老師用原音高,小安用同一個聲音把音高調高 15 個百分點。
- **頁面不使用瀏覽器內建語音**:錄音放不出來時只會無聲地照時間往下走。
- 動畫版一個人講的一整段是一個音檔,字幕依播放進度換行。
- 多音字逐處指定讀音(注音版依《國語一字多音審訂表》按當下用法判斷);注音符號與拼音字母照畫面顯示、錄音唸對應的音。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:頁面會在第一次觸碰畫面時解鎖音訊。**尚未在實機上測試。**
- 語音由使用者試聽過兩版(2026-11-17)。

## basic-geometry-intro

- `index.html`:繁體中文頁。`cn.html`:简体中文頁(網址 `.../basic-geometry-intro/cn.html`)。這兩頁沒有英文版,也不用登入。
- `audio/`:預錄語音 282 個音檔(`tw` 台灣讀音、`cn` 大陸讀音)與索引 `index_tw.js`、`index_cn.js`。頁面和 `audio/` 必須在同一層。
- 語音:台灣老師 Azure `zh-TW-HsiaoChenNeural`(速度 -10%、音調 +3%)、學生 `zh-TW-YunJheNeural`(音調 +18%);大陸老師 `zh-CN-XiaoxiaoNeural`(速度 -10%)、學生 `zh-CN-YunxiaNeural`。只播預錄音檔,找不到音檔的句子不會出聲,不會退回瀏覽器內建語音。
- 简体頁的用語已改成大陸習慣說法。
- 課程本體在另一個儲存庫:`https://github.com/claudecat30-sys/basic-geometry`。
- iPhone / iPad:第一次觸碰畫面時解鎖音訊。**尚未在實機上測試。**
- 音檔沒有逐句人工試聽。

## word-hunt-intro

### 連結

| 頁面語言(翻譯語言) | 檔案 | 線上觀看 |
|---|---|---|
| 繁體中文(英文翻譯) | `index.html` | https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/ |
| 简体中文(英文翻譯) | `cn.html` | https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/cn.html |
| 英文(繁體中文翻譯) | `en.html` | https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/en.html |
| 英文(简体中文翻譯) | `en-cn.html` | https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/en-cn.html |
| 日文(繁體中文翻譯) | `ja.html` | https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/ja.html |
| 日文(简体中文翻譯) | `ja-cn.html` | https://claudecat30-sys.github.io/dino-ai-pages/word-hunt-intro/ja-cn.html |

每個網址後面加 `#read` 會直接開閱讀版。

- 六個頁面介紹的是「迪諾文字大尋寶」四個版本:繁體英文、簡體英文、繁體日文、簡體日文。繁體版 3,814 字、簡體版 3,691 字,所以繁體頁面寫「三千八百多個字」、簡體頁面寫「三千六百多個字」。
- 每頁分「動畫版」與「閱讀版」,可以開關翻譯字幕。六頁之間沒有互相連結的按鈕,檔名不要改,否則已發出去的連結會失效。
- `img/`:170 張圖片(約 14 MB)。`audio/`:507 個預錄語音 mp3(約 17.9 MB)。檔名是內容的雜湊值,六頁共用,由專案的輸出工具產生,不要手動改名。六個 html 和 `img/`、`audio/` 必須在同一層。
- 語音全部用 Azure 語音服務預先錄好。段落標題(旁白)和莉莉的台詞用女老師的聲音,迪諾的台詞用男生的聲音:

  | 語言 | 旁白、莉莉(女) | 迪諾(男) |
  |---|---|---|
  | 繁體中文(台灣讀音) | `zh-TW-HsiaoChenNeural`(速度 -10%、音調 +3%) | `zh-TW-YunJheNeural`(-6%) |
  | 简体中文(大陸讀音) | `zh-CN-XiaoxiaoNeural`(速度 -10%、音調 +3%) | `zh-CN-YunxiaNeural`(-6%) |
  | 英文 | `en-US-AmberNeural`(-5%) | `en-US-BrandonNeural`(-5%) |
  | 日文 | `ja-JP-NanamiNeural`(-10%) | `ja-JP-KeitaNeural`(-8%) |

- 動畫版每句台詞是一個完整音檔,字幕依播放進度換段。翻譯字幕旁的喇叭會用翻譯語言唸那一句。
- 多音字指定讀音:繁體依《國語一字多音審訂表》與課程已審訂的注音(連接詞「和」唸 ㄏㄢˋ),簡體依課程已審訂的拼音。日文容易唸錯的漢字改成假名後錄音,畫面文字不變。
- **頁面不使用瀏覽器內建語音**:只播預錄音檔,頁面裡沒有系統語音的程式。錄音放不出來時那一句會安靜地照時間往下走。
- 頁面沒有對外連結,也不依賴其他網站或儲存庫。
- iPhone / iPad:**尚未在實機上測試。**
- 音檔沒有逐句人工試聽;句尾一聲下墜沒有量測。

## sis-teacher-manual-sc

- `index.html`:手冊本體(简体中文,可切換英文)。`d/`:12 級的教案內容。`p/`:12 級的原書頁面圖。三者必須在同一層。
- 開啟時先顯示登入畫面。頁面原始碼只存帳號密碼的 SHA-256 雜湊值,不含明文;勾選「记住帐号密码」會在該瀏覽器保留 180 天。這只是前端門檻:`d/`、`p/` 的內容在這個公開儲存庫裡仍可直接讀取。
- **預錄語音(`audio/`)尚未上傳**:全部約 1.8 GB,超過本儲存庫 1 GB 的上限,因此線上版的朗讀按鈕目前沒有聲音。
