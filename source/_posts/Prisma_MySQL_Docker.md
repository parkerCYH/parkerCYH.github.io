---
title: Prisma, MySQL, Docker
date: 2023-04-15 10:30:00
---

## Prisma-MySQL-Workshop

### 必要條件

- Docker
- Insomnia
- MySQL Workbench

---

### 安裝 MySQL with Docker

#### 建立 Docker Image

```bash
docker build -t mysql-docker .
```

#### 啟動 Container

```bash
docker run --name mysql-container -p 3307:3306 -d mysql-docker
```

> 這個 Container 將會運行在 3307 端口

---

### 開啟 MySQL 日誌

```sql
SET GLOBAL general_log = 'ON';
```

#### 檢查日誌路徑

```sql
SHOW VARIABLES LIKE 'general_log%';
```

---

### 安裝套件

```bash
yarn install
```

### 設定環境變數檔

請參考 `.env.example` 進行設置。

---

### 匯入 Insomnia JSON

### 資料庫遷移

```bash
yarn migrate
```

### 啟動專案

```bash
yarn dev
```

### 啟動 Prisma Studio

```bash
yarn studio
```

---

### 標籤

#prisma #mysql #docker
