# 臺灣大專校院永續排名追蹤平台｜Version 2.0

正式版專案結構：

```text
/
├── index.html          # Portal 入口首頁
├── the/
│   ├── index.html      # THE Impact Rankings
│   └── the_data.xlsm   # THE 資料
└── qs/
    ├── index.html      # QS Sustainability Rankings
    └── qs_data.xlsm    # QS 資料
```

## GitHub Pages

- Portal: `https://<帳號>.github.io/<repository>/`
- THE: `https://<帳號>.github.io/<repository>/the/`
- QS: `https://<帳號>.github.io/<repository>/qs/`

## Version 2.0 調整

- Portal 不顯示年度區間，避免每年手動修改。
- THE / QS 年度區間由資料自動判斷。
- Footer 改為 `Powered by 校務大數據分析組`。
- Last Updated 由 JavaScript 自動顯示當日日期。
- THE / QS 背景統一：星點減少、流星頻率提高、增加多顆 orbit 星球。
- THE Top Chart 固定粉紫色，顯示臺灣 Top 15 大學 (THE)。
- QS Top Chart 固定馬卡龍黃色，顯示臺灣 Top 15 大學 (QS)，並依基準年度顯示。
- QS 刪除 Top 年度篩選。

## 更新資料

- THE：覆蓋 `the/the_data.xlsm`
- QS：覆蓋 `qs/qs_data.xlsm`

請維持檔名不變。
