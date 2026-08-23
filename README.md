# Off The Clock

Sandy Liu 的生活版單頁。單一 HTML,無外部相依 — 字型、頭像、favicon 都內嵌。

## 檔案
- `index.html` — 整頁
- `og.png` — 分享預覽卡,1200×630
- `apple-touch-icon.png` — iOS 加到主畫面的圖示,180×180

三個檔案平放在 repo 根目錄,不需要建置步驟。

## GitHub Pages
Settings → Pages → Source 選 `Deploy from a branch`,Branch 選 `main` / `(root)`,
存檔後幾分鐘內會出現在:

    https://sandyliu3056.github.io/Off-The-Clock/

## 換網址要改的地方
`index.html` 開頭有四處寫死上面那個網址:`<link rel="canonical">`、`og:url`、
`og:image`、`twitter:image`。之後若掛自訂網域,四處一起改,否則分享預覽會抓錯圖。

## 內容
馬爾地夫配色(白沙底、深海藍文字、背景有陽光與海面漸層)。十一張手繪貼紙、
頁尾有柯基與雙色布偶貓在散步。頁首右上連回工作作品集 sandyliuportfolio.com。
