# 廠長信箱（Factory Director's Mailbox）

匿名意見收集網頁。外框（橫幅、匿名說明、頁尾）是 `index.html`，中間嵌入 Microsoft Forms；
留言只存在公司 Microsoft 365 的 Forms 裡，本 repo 不存任何留言。

- 網址：https://scmcweb.github.io/factory-director-mailbox/
- 英文版：https://scmcweb.github.io/factory-director-mailbox/?lang=en
- 沒帶 `?lang=` 時依瀏覽器語言自動選中文或英文。

## 運作方式

```
員工（手機／外網／公司電腦）
  -> index.html（GitHub Pages，純靜態頁）
       -> 內嵌 Microsoft Forms（任何人都可以回應、不需登入）
            -> 回應存在表單擁有者的 Microsoft 365
```

## 常見維護

- **換表單**：在 Forms 按「收集回應」→「內嵌」(`</>`)，把 `src="..."` 的網址貼到 `index.html` 的 `CONFIG.formUrl.zh`。
  `en` 留空即沿用同一份多語言表單；外框會自動帶 `&lang=zh-TW` / `&lang=en-US` 切換 Forms 語言。
- **改外框文字**：改 `index.html` 裡的 `TEXT.zh` / `TEXT.en`。
- **上線**：commit 並 push 到 `main`，GitHub Pages 約 1 分鐘內自動更新。

本專案獨立於 SCMC Web，不共用程式或部署流程。
