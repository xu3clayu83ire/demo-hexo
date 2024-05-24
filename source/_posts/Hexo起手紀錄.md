---
title: Hexo起手紀錄
date: 2024-05-25 00:58:40
tags:
  - Hexo
categories:
  - [frontend]
---

## 安裝

1. Node.js 版本需不低於 8.10，建議使用 Node.js 10.0 及以上版本
2. Git

```
node -v
npm -v
git -v
npm install -g hexo-cli
hexo -v
```

**補充**
npm 預設 global 資料夾與 cache 資料夾路徑(Windows)為
C:\Users\使用者名稱\AppData\Roaming\npm
C:\Users\使用者名稱\AppData\Roaming\npm-cache 或 C:\Users\使用者名稱\npm-cache
hexo 安裝路徑: `C:\Users\使用者名稱\AppData\Roaming\npm\node_modules\hexo-cli`
![image](https://raw.githubusercontent.com/xu3clayu83ire/images/demo-hexo/hexo-cli.png)

**遇到問題**
[參考網站](https://akoncc.github.io/2019/11/01/vscode-cant-run-script/)
![image](https://raw.githubusercontent.com/xu3clayu83ire/images/demo-hexo/powershell-restricted.png)

## 建立樣板網站

```
hexo init <你的網站名稱>
```

![image](https://raw.githubusercontent.com/xu3clayu83ire/images/demo-hexo/hexo-init.png)

```
// 移動到資料夾
cd <你的網站名稱>

// 啟動你的網站
hexo server
```

![image](https://raw.githubusercontent.com/xu3clayu83ire/images/demo-hexo/hexo-server.png)

在瀏覽器上輸入網址:http://localhost:4000/ 看到網站首頁
![image](https://raw.githubusercontent.com/xu3clayu83ire/images/demo-hexo/hexo-localgost.png)

## 常用指令

建立部落格：`hexo init <你的網站名稱>`
新增一篇部落格文章：`hexo new <部落格文章標題>`
輸出靜態網頁： `hexo generate`
清除快取：`hexo clean(清除快取檔案db.json和已產生的靜態檔案public。)`
啟動網站：`hexo server`
新增頁面: `hexo new page <資料夾名稱>`
標籤:`tags: -<名稱>`
分類: `categories -[名稱]`

## 配置說明

全站設定檔案: `.\_config.yml`
各主題設定檔案:`.\themes\<主題資料夾>\_config.yml`

## 加入主題

#### 加入預設主題

1. Hexo 預設主題: [landscape](https://github.com/hexojs/hexo-theme-landscape)
2. [其他主題](https://hexo.io/themes/)

## 部屬到 GitHub Page

[官方文件-一鍵佈署](https://hexo.io/zh-tw/docs/github-pages#%E4%B8%80%E9%8D%B5%E9%83%A8%E5%B1%AC)

自行佈署

1. `hexo generate`產生靜態網頁到 public 資料夾
2. 將 public 資料夾 push 到 GitHub [Repo/deploy 分支](https://github.com/xu3clayu83ire/demo-hexo/tree/deploy)
