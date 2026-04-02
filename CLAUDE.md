# 瑞全企業股份有限公司 — 官網專案

## 專案概述
為瑞全企業股份有限公司（Raychuan Enterprise Co., Ltd.）製作的靜態公司網站，用於取代舊網站並部署至 GitHub Pages，連結現有域名。

- **產業**：精密塑膠射出製造（汽機車零件為主）
- **現有域名**：www.raychuan.com.tw
- **部署目標**：GitHub Pages + 自訂域名（CNAME）
- **UI 參考**：https://daiei-ironworks.co.jp（日式工業企業風格）

## 技術規格
- 純靜態網站，單一 `index.html` 檔案
- 所有 CSS 嵌入於 HTML `<style>` 標籤內
- 無外部框架，最小化 JavaScript
- 字型：Google Fonts（Noto Serif TC、Noto Sans TC）

## 檔案結構
```
公司網站製作/
├── index.html       # 主要（唯一）HTML 檔案
└── images/          # 所有圖片（中文檔名）
```

## 圖片對照表
HTML 內的圖片路徑對應實際檔名如下：

| 用途 | 實際檔名 |
|------|----------|
| Hero 背景 | `機械手自動噴漆.JPG` |
| About 空拍圖 | `公司空拍圖 面積大小.png` → HTML 需寫 `%20` |
| CCD 視覺檢測 | `CCD視覺輔助檢測異常.jpg` |
| 全廠 CCTV | `射出機全場即時高清監控.JPG` |
| 機械手噴漆 | `機械手自動噴漆.JPG` |
| 機械手研磨 | `機械手自動研磨.JPG` |
| 機械手組裝 | `機械手自動組裝零件.JPG` |
| 台車治具 | `台車容器自行製作開發.JPG` |
| 手機上傳介面 | `手機上傳介面的截圖.png` |
| 巡檢儀表板 | `巡檢記錄表單畫面.png` |
| 數據看板 | `數據看板截圖.png` |
| 跑步機外蓋（白） | `跑步機外蓋 2.jpg` → HTML 需寫 `%20` |

> 其餘產品圖片檔名與中文名稱相符，直接使用即可。

## 設計規範
### 色彩系統
```css
--navy:      #0d2340   /* 主色（深海軍藍） */
--navy-mid:  #1a3a5c
--blue:      #1e5fa8
--blue-light:#2e7bc4
--gold:      #c9a84c   /* 強調色 */
--accent:    #e8292a   /* 警示紅 */
--gray-light:#f4f6f9
```

### 字型
- 標題：`Noto Serif TC`（serif）
- 內文：`Noto Sans TC`（sans-serif）

## 公司資訊
- **電話**：04-8652418
- **Email**：ray.chuan@msa.hinet.net
- **地址**：彰化縣埔鹽鄉員鹿路三段122號
- **統編**：23403862
- **創立**：1976 年（2025 年為 49 年）
- **認證**：ISO-9001
- **廠區**：15,423 m²（4,665 坪）
- **最大機台**：3200T（中部地區最大）

## 注意事項
- 圖片檔名含中文與空格，HTML 的 `src` 屬性中空格必須寫為 `%20`
- 副檔名大小寫混用（`.jpg` / `.JPG`），需與實際檔名一致（大小寫敏感，部署後會出錯）
- 所有 JavaScript 放在 `</body>` 前，不可放入 `<footer>` 標籤內
- 年份數字（49年）需與 About badge、Hero stats 保持一致
