# creonlee.app

個人自我介紹網站的原始碼。

- 線上位置：<https://creonlee.app>
- 生活動態：<https://blog.creonlee.app>（要登入才看得到私密貼文）
- Writeups：<https://writeup.creonlee.app>（要登入）
  兩個站是同一個 Cloudflare Worker，原始碼在 `creon-shit/blog`（private）
- 小恐龍：<https://dinosaur.creonlee.app>
- 踩地雷：<https://mines.creonlee.app>（原始碼在 [creon-shit/mines](https://github.com/creon-shit/mines)）

## 檔案

```
.
├── index.html   # 整個網站就這一個檔案（HTML + CSS + JS 都在裡面）
├── CNAME        # creonlee.app
└── README.md
```

## 怎麼改網站

1. 編輯 `index.html`
2. `git add . && git commit -m "更新內容" && git push`
3. 等約 1 分鐘，GitHub Pages 會自動重新部署

想在本機先看效果，直接用瀏覽器打開 `index.html` 就好。

## 網域設定

DNS 在 Cloudflare。要讓這個 repo 的內容真的上線，`creonlee.app` 必須指向 GitHub Pages
（`creon-shit.github.io`），而且不能有 Cloudflare Worker 路由蓋掉它。
