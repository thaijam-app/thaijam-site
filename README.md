# thaijam-site

ThaiJam 泰記的官方網站。**https://thaijam.app**

由這個 repo 的 GitHub Pages 發布（來源：`main` 分支根目錄）。

---

## ⚠️ 這個 repo 只放首頁

**隱私權政策與支援頁不在這裡**，它們在 `thaijam-app/thaijam-privacy`
（網址 `privacy.thaijam.app`）：

| 頁面 | 網址 | 來源 repo |
|---|---|---|
| 首頁 | `thaijam.app` | **這裡** |
| 支援與常見問題 | `privacy.thaijam.app/support/` | `thaijam-privacy` |
| 隱私權政策（iOS） | `privacy.thaijam.app/privacy-policy/` | `thaijam-privacy` |
| 隱私權政策（Android） | `privacy.thaijam.app/privacy-policy-android/` | `thaijam-privacy` |

分成兩個 repo 是因為**一個 repo 只能有一個 `CNAME`**，而那兩個網址
已經送進 App Store / Play Console 了 —— 搬過來會讓已經送出的網址失效。

首頁底部連到那三頁用的是**絕對網址**，改動時要一起看。

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

## 本機預覽

純靜態，直接開檔案就好：

```bash
open index.html
```

不需要 Jekyll（有 `.nojekyll`），也沒有任何外部資源或建置步驟。
