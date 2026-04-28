# 汤梓燊 学术主页

个人学术静态网站，基于纯 HTML + CSS 构建，无框架依赖。

## 文件结构

```
academic-site/
├── index.html    # 主页面（全部内容）
├── style.css     # 样式文件
└── README.md     # 本说明文件
```

## 本地预览

在 `academic-site/` 目录下运行：

```bash
python -m http.server 8080
```

然后在浏览器中打开 [http://localhost:8080](http://localhost:8080)

> 注意：需要通过 HTTP 服务访问，直接双击 `index.html` 打开可能导致 Google Fonts 加载失败（CORS 限制），但内容显示不受影响。

## 部署到 GitHub Pages

1. 在 GitHub 创建一个新仓库（如 `academic-site`）

2. 将本目录内容推送到仓库：

   ```bash
   cd academic-site
   git init
   git add .
   git commit -m "init: academic homepage"
   git remote add origin https://github.com/<your-username>/academic-site.git
   git push -u origin main
   ```

3. 进入仓库的 **Settings → Pages**，Source 选择 `main` 分支，根目录 `/`，保存。

4. 稍等片刻后，网站将发布至 `https://<your-username>.github.io/academic-site/`

## 内容更新指南

所有内容均在 `index.html` 中，按以下位置修改：

| 内容 | 位置 |
|------|------|
| 姓名 / 单位 / 邮箱 | `<header>` 区块 |
| 发表论文 | `<section id="publications">` |
| 学术会议 | `<section id="conferences">` |
| 获奖情况 | `<section id="awards">` |
| 学术服务 | `<section id="service">` |
| 页脚年份 | `<footer>` |

样式调整（颜色、字号、间距）统一修改 `style.css` 顶部的 CSS 变量（`:root` 块）。
