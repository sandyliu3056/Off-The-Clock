# Off The Clock

Sandy Liu 的生活版單頁。單一 HTML。字型、頭像、favicon 都內嵌;唯一的外部請求是 Spotify 的官方 embed。

## 檔案
- `index.html` — 整頁
- `og.png` — 分享預覽卡,1200×630
- `apple-touch-icon.png` — iOS 加到主畫面的圖示,180×180

三個檔案平放在根目錄,不需要建置步驟,也不需要 vercel.json。

## 佈署
Vercel:整個資料夾拖進專案,或 `vercel --prod`。目前線上位置:

    https://off-the-clock-blush.vercel.app/

GitHub Pages(備援):三個檔案放進 repo 根目錄,Settings → Pages → Source
選 `Deploy from a branch`,Branch 選 `main` / `(root)`。

## 換網址要改的地方
`index.html` 開頭有四處寫死上面那個網址:`<link rel="canonical">`、`og:url`、
`og:image`、`twitter:image`。之後若掛自訂網域,四處一起改,否則分享預覽會抓錯圖。
作品集頁首右上那顆「Off the clock →」也指向這個網址,要一起改。

## 內容
「On repeat」那張卡是 Spotify 官方 embed(California feat. Warren Hue),
不是自架音檔 — 商業歌曲不能自己放上去。要換歌就改 iframe 網址最後那段 track ID。

馬爾地夫配色(白沙底、深海藍文字、背景有陽光與海面漸層)。十一張手繪貼紙、
頁尾有柯基與雙色布偶貓在散步。頁首右上連回工作作品集 sandyliuportfolio.com。

小裝飾(都在 `index.html` 裡,沒有新增外部請求):

- 「Off the clock」那條橫幅右邊是即時時間:新北的星期、日期、時刻與時區
  (`NEW TAIPEI MON 24 AUG 03:46 GMT+8`)。訪客不在同一個時區時,左邊會多一段
  他自己的時間(`YOURS 20:46 GMT+1`),手機版收起來免得那條擠爆。
  時區寫死 `Asia/Taipei`,不跟著訪客跑;「現在幾點」則來自訪客電腦的系統時鐘,
  再由 `Intl` 換算成台北時間 — 只用瀏覽器內建的 API,沒有網路請求。
  不想要就刪掉 ribbon 裡的 `<span class="now">` 和上面那支小 `<script>`。
- hero 右下角一枚貝殼、貼紙紙右下一顆海星,`.doodle` 那兩個 SVG,700px 以下自動收起來。
- 頁尾海岸帶多了一艘遠方帆船(`.shore-boat`)和兩隻海鷗(`.shore-gulls`),
  跟其他海岸元素一樣不吃滑鼠事件;`prefers-reduced-motion` 會關掉它們的漂移。
- 兩顆 chip(地點、IG)前面各加了一個 13px 的線稿小圖示。
