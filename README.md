# TripPlan

個人旅行行程集，部署於 GitHub Pages。

線上網址：https://allen880612.github.io/TripPlan/

## 目前收錄

| 行程 | 日期 | 路徑 |
| --- | --- | --- |
| 福岡自由行 | 2026/7/22–26（5 天 4 夜） | [/fukuoka/](./fukuoka/) |
| 首爾散步手帖 | 2026（6 天 5 夜） | [/korea/](./korea/) |

## 目錄結構

```
/
├── index.html          # 首頁（行程索引）
├── korea/index.html    # 首爾行程
├── fukuoka/index.html  # 福岡行程
└── .github/workflows/deploy.yml
```

## 新增行程

1. 建立新資料夾，例如 `osaka/`
2. 放入 `index.html`（整份單檔、內嵌 CSS/JS 即可）
3. 更新根目錄 `index.html`，在 `.trip-list` 區塊補上新的 `<a class="trip-card">` 卡片
4. commit & push 到 `main`，GitHub Actions 會自動部署

## 部署

推到 `main` 分支後，`.github/workflows/deploy.yml` 會透過 `actions/deploy-pages` 自動部署。

首次啟用需要到 repo 的 **Settings → Pages**，把 **Source** 設為 **GitHub Actions**。
