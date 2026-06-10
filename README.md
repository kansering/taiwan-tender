# 🏛️ 台灣標案查詢系統

> 純前端、零後端、一個 HTML 檔案，部署到 GitHub Pages 即可使用。

## 線上展示

```
https://你的帳號.github.io/taiwan-tender/
```

---

## 功能

### 📊 總覽儀表板
- 今日招標數、決標數、得標廠商數、無法決標數即時統計
- 本週最新招標列表
- 本週最新決標列表
- 最新得標廠商列表

### 📋 招標 / ✅ 決標
- 左側篩選面板：近期時間（今日 / 本週 / 1~4 週前）、招標方式、標的分類
- 關鍵字搜尋（案名、案號、機關、廠商）
- Table 檢視：採購機關、案名、招標方式、決標方式、分類、金額、截止日、公告日
- 分頁瀏覽 + 跳頁

### 💰 底價分析
- 依機關搜尋歷史決標記錄
- 統計：底價/預算平均比率、決標/底價比率
- 橫條圖視覺化 + 明細表格
- 24 個熱門機關快捷入口

### 🏢 廠商分析
- 依廠商名稱搜尋所有得標記錄
- 主要得標機關 Top 8
- 常見競爭對手分析
- 近期得標記錄列表
- 18 個熱門廠商快捷入口

### 標案詳情 Panel
- 點任何一筆標案從右側滑出詳情
- 完整欄位：採購資訊、金額（含預算/底價/決標金額）、機關聯絡資訊、投標廠商清單
- 直連政府採購網原始公告、投標須知下載

---

## 資料來源

| 項目 | 說明 |
|------|------|
| API | `pcc-api.openfun.app`（g0v 社群維護，CORS 開放） |
| 原始資料 | 行政院公共工程委員會 `web.pcc.gov.tw` |
| 授權 | 遵循公共工程委員會著作權聲明，查詢參考用途 |

---

## 部署到 GitHub Pages

**步驟一：建立 Repository**

```
GitHub → New repository → 名稱如 taiwan-tender → Create
```

**步驟二：上傳檔案**

把 `index.html` 和 `README.md` 上傳到 repo 根目錄。

**步驟三：開啟 Pages**

```
Settings → Pages → Source → Deploy from a branch → main / root → Save
```

**步驟四：等待約 1 分鐘**

網址格式：`https://你的帳號.github.io/taiwan-tender/`

---

## 本地開發

```bash
# 用 Python 起本地伺服器
python3 -m http.server 8080

# 開啟瀏覽器
open http://localhost:8080
```

---

## 技術架構

```
純前端 HTML/CSS/JS（單一檔案）
         │
         ▼
pcc-api.openfun.app（開放 API）
         │
         ▼
行政院公共工程委員會（原始資料）
```

- 無框架、無套件依賴、無建置流程
- 資料快取在 sessionStorage，切換日期不重複請求
- RWD 支援，手機可用

---

## 授權

MIT License — 自由使用、修改、部署。  
資料版權屬行政院公共工程委員會，使用時請遵循其[著作權聲明](https://web.pcc.gov.tw/pis/main/pis/client/pssa/right.do)。
