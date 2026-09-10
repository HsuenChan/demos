# demos

放個人作品用的前端 demo 頁面。每個資料夾是一個獨立的 demo，**不需要任何建置流程**，用瀏覽器直接打開就能跑。

## 資料夾

### `tw-canyoning-tabs/`

溪降路線資料庫的介面 demo。三欄式版面：左側路線清單、中間地形圖、右側路線檔案面板。

| 檔案 | 用處 |
|---|---|
| `index.html` | 完整的 demo。約 110 KB，底圖圖磚由外部服務即時載入，需要網路 |
| `photos/` | 路線照片。主圖寬 1200、另附縮圖，以 `loading="lazy"` 在需要時才載入 |

**畫面上有什麼**

- **右側面板七個分頁** — 快速資訊、時間規劃、天氣水情、進場路線、代表照片、風險注意、原始路線圖。面板左緣可以拖曳調整寬度。
- **真實地圖底圖** — Leaflet + 三種可切換底圖：地形圖（OpenTopoMap，含等高線與地名）、衛星影像（Esri）、街道圖（OSM）。各路線的 GPS 點位（停車點、渡溪點、入溪點等）直接標在圖上，點上寫名稱與海拔。
- **六條路線** — Cross Creek、Wilson Creek（Haast Pass）、Whio Creek（Fiordland Tutoko valley）、Bartrum Creek（Westland Waitaha Valley）、Mather Creek（Haast Pass）、Major Mayhem（Dart Valley）。
- **四個區域** — Haast Pass、Tutoko / Milford、Waitaha Valley、Dart Valley；選路線會自動縮放到該路線的座標範圍（Major Mayhem 的官方 topo 未提供座標，因此沒有標點）。

**資料來源**

- 路線資訊與 GPS 座標：[KiwiCanyons](https://www.kiwicanyons.org/)，topo by Daniel Clearwater、Will Hamilton；分級定義見 [KiwiCanyons Grading](https://www.kiwicanyons.org/our-canyons/grading/)
- 照片：來自 [KiwiCanyons](https://www.kiwicanyons.org/)；Wilson Creek 部分照片的拍攝者標於各圖說（Rod Sturm、Chuckys、Ira），其餘原始檔未附拍攝者資訊
- 底圖圖磚：[OpenTopoMap](https://opentopomap.org/)（CC-BY-SA，資料來自 OpenStreetMap 與 SRTM）、Esri World Imagery、[OpenStreetMap](https://www.openstreetmap.org/copyright)
- **「天氣水情」分頁是示範資料，不是實際觀測值。** 正式版預計串接 NIWA 與 West Coast Regional Council 的水位／雨量 API。

## 怎麼開

雙擊 HTML 檔，或在終端機執行：

```bash
open tw-canyoning-tabs/index.html
```

## 貢獻

這是公開 repo，歡迎 fork 之後發 Pull Request。
