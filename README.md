# thaijam-site

ThaiJam 泰記的官方網站。**https://thaijam.app**

由這個 repo 的 GitHub Pages 發布（來源：`main` 分支根目錄）。

---

## 網站內容

主網站包含首頁、支援頁與 Spotify 設定教學。原本送進 App Store 的
`privacy.thaijam.app/support/` 會繼續保留；隱私權政策仍由
`thaijam-app/thaijam-privacy` 發布：

| 頁面 | 網址 | 來源 repo |
|---|---|---|
| 首頁 | `thaijam.app` | **這裡** |
| 支援與常見問題 | `thaijam.app/support/` | **這裡** |
| Spotify 設定教學 | `thaijam.app/support/spotify-setup/` | **這裡** |
| 原支援網址（App Store 使用中） | `privacy.thaijam.app/support/` | `thaijam-privacy` |
| 隱私權政策（iOS） | `privacy.thaijam.app/privacy-policy/` | `thaijam-privacy` |
| 隱私權政策（Android） | `privacy.thaijam.app/privacy-policy-android/` | `thaijam-privacy` |

分成兩個 repo 是因為**一個 repo 只能有一個 `CNAME`**。原支援網址已送進
App Store，因此在 App Store 改用新網址以前不能移除。

首頁底部的支援與 Spotify 連結使用主網域；隱私權政策仍使用完整的
`privacy.thaijam.app` 網址。

---

## 改了要確認什麼

1. 推上去之後**打開 https://thaijam.app 確認真的變了**。
   GitHub Pages 建置失敗時會保留上一次成功的版本 —— 網站看起來活著，
   但內容是舊的。這個坑在 `thaijam-privacy` 踩過一次，線上停在五天前的版本
   而沒有人發現。
2. 頁面上的數字（教材筆數、發音數、句型數）要跟 `ThaiJam` repo 的
   `ThaiStudyApp/Resources/` 對得上。**查不到出處的數字不要寫** ——
   初版曾經想寫「21,654 詞的斷詞字典」，追下去發現那是程式碼註解裡的
   一句分析，不是實際打包的檔案。
3. ⚠️ **不要寫「真人發音」。** 音檔是 `Scripts/generate_audio.py` 用
   Microsoft Edge TTS 的泰語神經語音（`th-TH-PremwadeeNeural`）生成的，
   不是人錄的。初版寫成「1,727 個真人發音」，那是不實宣稱 ——
   App 自己在 `SettingsView.swift` 就明寫「不是真人錄音」，網站不能比 App 誇大。

## 泰式紋樣

`index.html` 內嵌三個 SVG 路徑（กนก 火焰紋、ดอกบัวตูม 蓮花苞、ช่อฟ้า 屋脊飾），
座標**直接取自 App 的 `ThaiStudyApp/Support/ThaiOrnament.swift`**（同樣是 100×100 座標系）。

用 App 自己的紋樣而不是現成素材有兩個理由：網站與 App 是同一套設計語言；
而且那份 Swift 檔的檔頭寫過為什麼不用 AI 生成的插畫 ——
生圖模型畫泰文書寫系統很不可靠，在一個教泰文的 App 旁邊出現「看起來像泰文
但不是字」的裝飾，是直接打臉專業度。

## 本機預覽

純靜態，直接開檔案就好：

```bash
open index.html
```

不需要 Jekyll（有 `.nojekyll`），也沒有任何外部資源或建置步驟。
