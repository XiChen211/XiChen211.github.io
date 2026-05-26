# XiChen — 个人主页

零构建的个人网站：单文件 HTML + Tailwind CDN，部署在 GitHub Pages。

## 本地预览

直接双击 `index.html` 即可，或起一个本地服务器：

```powershell
cd d:\Projects\personal-site
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 文件说明

| 文件 | 用途 |
|------|------|
| `index.html` | 站点主文件，所有内容、样式、脚本都在这一个文件里 |
| `favicon.svg` | 浏览器标签页图标（矢量，现代浏览器优先使用） |
| `favicon.ico` | 旧浏览器与 Windows 兼容图标 |
| `apple-touch-icon.png` | iOS 添加到主屏幕时使用的图标（180×180） |
| `icon-192.png` / `icon-512.png` | Android / PWA 备用图标 |
| `.nojekyll` | 告诉 GitHub Pages 跳过 Jekyll 处理 |

## 替换占位内容

在 `index.html` 中搜索 `TODO:` 可以一次性定位所有需要你替换的位置：

- 头像图片（目前是 "XC" 字母占位）
- 职业一句话定位
- "关于我" 三段介绍文案
- 技能标签清单
- 经历时间线的 3 条条目
- LinkedIn / Twitter 链接（或删除整块）

## 发布到 GitHub Pages

1. 在 https://github.com/new 创建一个 **Public** 仓库
   - 推荐仓库名：`XiChen211.github.io`（这样访问地址就是 `https://XiChen211.github.io/`）
   - 或任意名（访问地址会带子路径）
   - 不要勾选 "Add a README"
2. 在本目录初始化并推送：
   ```powershell
   cd d:\Projects\personal-site
   git init
   git add .
   git commit -m "Initial commit: personal site"
   git branch -M main
   git remote add origin https://github.com/XiChen211/<repo-name>.git
   git push -u origin main
   ```
3. 仓库 → Settings → Pages
   - Source：**Deploy from a branch**
   - Branch：**main** / **/ (root)** → Save
4. 等 1–2 分钟刷新，页面顶部会显示访问 URL。
