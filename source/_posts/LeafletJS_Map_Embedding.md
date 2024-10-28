---
title: LeafletJS 網頁嵌入地圖
date: 2021-05-09 10:30:00
---

## Leaflet

Leaflet 是一個開源的 JavaScript 庫，用於構建 Web 地圖應用。

---

## Start Up

### 將 CSS、JS 加入到 `<head>`

```html
<link
  rel="stylesheet"
  href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
  integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
  crossorigin=""
/>
<!-- Make sure you put this AFTER Leaflet's CSS -->
<script
  src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
  integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
  crossorigin=""
></script>
```

---

### 在 `<body>` 中加入地圖元素

```html
<div id="mapId"></div>
```

---

### CSS 調整地圖尺寸

```css
#mapId {
  height: 180px;
}
```

---

### 初始化地圖

在 JavaScript 中將 `mapId` 元素初始化，定義地圖座標與縮放值。

```javascript
var myMap = L.map("mapId").setView([51.505, -0.09], 13);
```

---

## 參考資料

[LeafletJS 入門教學](https://leafletjs.com/)
