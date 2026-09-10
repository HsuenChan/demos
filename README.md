# demos

放個人作品用的前端 demo 頁面。每個資料夾是一個獨立的 demo，都是**單一 HTML 檔、不需要任何建置流程**，用瀏覽器直接打開就能跑。

## 資料夾

### `tw-canyoning-tabs/`

溪降路線資料庫的介面 demo。三欄式版面：左側路線清單、中間地形圖、右側路線檔案面板。

| 檔案 | 用處 |
|---|---|
| `index.html` | 完整的 demo。單檔自包含，照片與地形資料都已內嵌，不需要外部資源 |

**畫面上有什麼**

- **右側面板七個分頁** — 快速資訊、時間規劃、天氣水情、進場路線、代表照片、風險注意、原始路線圖。面板左緣可以拖曳調整寬度。
- **可縮放的地形圖** — 縮到底可以看到整個紐西蘭；拉近會接上等高線地形圖，並標出各路線的 GPS 點位（停車點、渡溪點、入溪點等），點上直接寫名稱與海拔。
- **五條已建檔路線** — Cross Creek、Wilson Creek、Mather Creek（Haast Pass）、Whio Creek（Fiordland Tutoko valley）、Bartrum Creek（Westland Waitaha Valley）。清單裡的台灣路線是尚未建檔的佔位資料。
- **地形資料涵蓋三個區域** — Haast Pass、Tutoko / Milford、Waitaha Valley；縮到最小可看見整個紐西蘭，三個區域各以紅框標示。

**資料來源**

- 路線資訊與 GPS 座標：[KiwiCanyons](https://www.kiwicanyons.org/)，topo by Daniel Clearwater
- 地形高程：NASA SRTM 1 arcsec DEM（Haast Pass）與 AWS Terrarium 補洞高程（Fiordland、Waitaha）
- 海岸線向量：[Natural Earth](https://www.naturalearthdata.com/)（公有領域）
- **「天氣水情」分頁是示範資料，不是實際觀測值。** 正式版預計串接 NIWA 與 West Coast Regional Council 的水位／雨量 API。

## 怎麼開

雙擊 HTML 檔，或在終端機執行：

```bash
open tw-canyoning-tabs/index.html
```

## 貢獻

這是公開 repo，歡迎 fork 之後發 Pull Request。
