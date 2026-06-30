# 臺灣大專校院永續排名追蹤平台｜Version 4.7 Final

這是重新整理後的 GitHub Pages 發布包，使用固定且乾淨的標準結構。

```text
/
├── index.html
├── the/
│   ├── index.html
│   └── the_data.xlsm
└── qs/
    ├── index.html
    └── qs_data.xlsm
```

## 正式網址

- Portal：`https://<帳號>.github.io/<repository>/`
- THE：`https://<帳號>.github.io/<repository>/the/index.html`
- QS：`https://<帳號>.github.io/<repository>/qs/index.html`

## 更新資料

請直接覆蓋：
- `the/the_data.xlsm`
- `qs/qs_data.xlsm`

請不要改檔名。

## v4.1 更新

- THE 與 QS 的各校資料總表新增「學校」欄位凍結效果，水平瀏覽後方欄位時仍可看到學校名稱。

## v4.2 更新

- 修正 QS 頁面 JavaScript 排序語法錯誤，避免頁面內容無法顯示。

## v4.3 更新

- 修正各校資料總表凍結欄位：THE 凍結第 3 欄「學校」，QS 凍結第 4 欄「學校」，不再誤凍結排名欄位。

## v4.4 更新

- QS 頁面改為優先讀取內嵌資料，降低 GitHub Pages、Excel 讀取或外部套件載入造成空白頁的風險。
- 若 Chart.js 暫時無法載入，資料表與 KPI 仍會顯示。

## v4.5 更新

- QS 背景調整為與 THE 相同的星球、orbit 與星群密度風格。
- QS 年度區間副標字級與 THE 對齊。
- THE 各校資料總表強化「國立高雄科技大學」醒目高亮效果。

## v4.6 更新

- QS 年度區間副標字級與 THE 對齊。
- QS 背景增加 orbit 星球與忽明忽暗星點層，視覺更接近 THE。

## v4.7 更新

- 修正 THE 各校資料總表凍結欄位：改為凍結第 3 欄「學校」。
- QS 各校資料總表刪除最後一欄「更新時間」。
