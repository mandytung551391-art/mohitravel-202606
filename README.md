# MOHI TRAVEL 網站規格文檔

## 📋 專案概述

**專案名稱**: MOHI TRAVEL - 旅遊世界  
**版本**: 1.0.0  
**建立日期**: 2026-06-22  
**使用技術**: Bootstrap 5.3.0 + HTML5 + CSS3  
**本地運行**: 無需伺服器，直接用瀏覽器開啟 HTML 檔案

---

## 📂 目錄結構

```
website/
├── index.html          # 首頁
├── README.md           # 本規格文檔
├── css/                # 樣式檔案夾
│   ├── bootstrap.min.css
│   ├── style.css       # 自訂樣式
│   ├── icons.css       # 圖標樣式
│   └── [其他 Bootstrap CSS 檔案]
├── js/                 # JavaScript 檔案夾
│   ├── bootstrap.bundle.min.js
│   └── [其他 Bootstrap JS 檔案]
└── images/             # 圖片檔案夾
    ├── TURKEY.jpg
    ├── MOROCCO.jpg
    ├── IRAN.jpg
    ├── ARB.jpg
    ├── ANNA.jpg
    └── [其他本地圖片]
```

---

## 📄 檔案說明

### HTML 檔案
- **index.html**: 首頁，包含導航、輪播圖、關於我們、產品介紹、頁尾等區域

### CSS 檔案結構

#### 1. **css/bootstrap.min.css** (第三方)
   - Bootstrap 5.3.0 框架
   - 提供響應式佈局和基礎元件

#### 2. **css/icons.css** (自訂)
   - Font Awesome 6.4.0 圖標庫引用
   - 統一管理所有圖標資源
   - **修改圖標庫時只需修改此檔案**

#### 3. **css/style.css** (自訂)
   - 所有自訂樣式定義
   - 顏色配置、排版、動畫效果
   - 模組化樣式，方便維護

### JavaScript 檔案
- **js/bootstrap.bundle.min.js**: Bootstrap 5 官方 JS，提供互動功能

### 圖片檔案
所有圖片存放於 `images/` 資料夾，包括：
- **輪播圖**: TURKEY.jpg、MOROCCO.jpg 等旅遊國家景觀圖
- **關於我們圖**: pexels-rayn-l-1656184-3163677.jpg
- **產品卡片圖**: 各國美食圖片

---

## 🎨 CSS 樣式說明

### 主要顏色配置
```css
主藍色: #2c5aa0          /* 標題、文字 */
棕色: #8B4513             /* 品牌色 */
淺灰: #f8f9fa             /* 背景色 */
```

### 主要樣式模組

#### 導航欄 (navbar)
- 固定背景色白色
- 粘性定位 (sticky-top)
- 標誌顏色：棕色

#### 輪播圖 (carousel)
- 高度：500px
- 自動播放，含指示器和控制按鈕

#### 產品卡片 (product-card)
- 圓角邊框 (border-radius: 15px)
- 懸停動畫效果
- 六種國家特定漸層背景色

#### 頁尾 (footer)
- 綠色漸層背景
- 包含社群連結、公司資訊、版權宣告

---

## 📱 頁面結構

### 1. 導航菜單
- 品牌：MOHI TRAVEL
- 導航連結：首頁、關於我們、旅遊國度、聯絡我們、登入

### 2. 輪播圖區域 (id: home)
- 5 張旅遊國家圖片
- 自動循環播放
- 支援手動翻頁

### 3. 關於我們區域 (id: about)
- 左圖右文佈局
- 公司簡介文字

### 4. 產品介紹區域 (id: products)
- 6 張卡片 (col-lg-4 = 三欄排列)
- 每張卡片含：圖片、國家名稱、描述文字
- 國家：土耳其、阿曼、摩洛哥、伊朗、埃及、沙地阿拉伯

### 5. 頁尾 (id: contact)
- 社群連結 (Facebook、Instagram、YouTube)
- 公司資訊 (電話、地址、郵箱)
- 版權宣告

---

## 🚀 使用方式

### 開啟網站
1. 直接用瀏覽器開啟 `index.html`
2. 或使用 VS Code 的 Live Server 擴充功能

### 本地預覽
- 所有資源均為本地檔案
- 無需網路連線
- 支援所有現代瀏覽器 (Chrome、Firefox、Edge 等)

---

## ✏️ 維護指南

### 修改樣式
1. 開啟 `css/style.css`
2. 修改相應的 CSS 規則
3. 刷新瀏覽器查看變更

### 修改圖片
1. 將新圖片放入 `images/` 資料夾
2. 在 `index.html` 中更新圖片路徑
3. 例如：`<img src="images/new-image.jpg">`

### 修改內容文字
1. 開啟 `index.html`
2. 查找相應區域的文字
3. 直接修改內容

### 修改導航連結
1. 在 `index.html` 中找到 `<nav>` 元素
2. 修改或新增 `<a class="nav-link">` 連結

---

## 📝 新增頁面指南

### 建立新頁面步驟

1. **建立新 HTML 檔案** (例如: `about.html`)
   ```html
   <!DOCTYPE html>
   <html lang="zh-TW">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>頁面標題</title>
       <!-- 引用相同的 CSS 檔案 -->
       <link href="css/bootstrap.min.css" rel="stylesheet">
       <link rel="stylesheet" href="css/icons.css">
       <link rel="stylesheet" href="css/style.css">
   </head>
   <body>
       <!-- 頁面內容 -->
       <script src="js/bootstrap.bundle.min.js"></script>
   </body>
   </html>
   ```

2. **複用導航菜單** - 保持一致的導航結構

3. **使用相同的 CSS** - 確保視覺風格統一

---

## 🔧 技術細節

### Bootstrap 版本
- Bootstrap 5.3.0
- 使用 minified 版本以提高載入速度
- 包含所有響應式功能

### Font Awesome 版本
- Font Awesome 6.4.0
- 通過 CDN 引用
- 支援 600+ 圖標

### 響應式設計
- 移動優先設計
- Breakpoints:
  - xs: <576px
  - sm: ≥576px
  - md: ≥768px
  - lg: ≥992px
  - xl: ≥1200px
  - xxl: ≥1400px

---

## 📊 SEO 和可訪問性

### Meta 標籤
- 字符編碼：UTF-8
- 視窗設置：響應式設計

### 影像 Alt 文本
- 所有圖片均有適當的 Alt 文本
- 便於視覺障礙使用者

### 語言設置
- HTML lang 屬性：zh-TW (繁體中文)

---

## 🐛 常見問題解決

### 圖片無法加載
- 檢查 `images/` 資料夾是否存在
- 確認圖片檔案名稱拼寫正確
- 檢查路徑是否正確 (相對於 HTML 檔案位置)

### 樣式未生效
- 清除瀏覽器快取 (Ctrl+Shift+Delete)
- 檢查 CSS 檔案路徑是否正確
- 確認 CSS 檔案未損壞

### Bootstrap 組件不工作
- 確認 `js/bootstrap.bundle.min.js` 已正確引用
- 檢查瀏覽器控制台是否有 JS 錯誤
- 刷新頁面重新載入

---

## 📞 聯絡資訊

**公司名稱**: MOHI TRAVEL  
**電話**: 02-25513-9100  
**地址**: 台北市忠孝東路四段188號9樓  
**郵箱**: Mandy.Tung551391@Gmail.Com

---

## 📅 版本歷史

| 版本 | 日期 | 變更內容 |
|-----|------|---------|
| 1.0.0 | 2026-06-22 | 初版發佈 |

---

## 📚 相關資源連結

- [Bootstrap 官方文檔](https://getbootstrap.com/docs/)
- [Font Awesome 圖標庫](https://fontawesome.com/)
- [MDN Web 文檔](https://developer.mozilla.org/)

---

**最後更新**: 2026-06-22  
**維護人員**: [您的名稱]  
**狀態**: 活躍維護中
## 對外公開網址 
https://mandytung551391-art.github.io/mohitravel-202606/

## github
https://github.com/mandytung551391-art/mohitravel-202606

## ssh 
git@github.com:mandytung551391-art/mohitravel-202606.git