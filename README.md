# Hengfei Zhao — Academic Personal Website

纯静态学术个人主页，零依赖，可直接部署到 GitHub Pages 或本地双击 `index.html` 预览。

## 文件结构

```
website/
├── index.html      # 页面结构
├── style.css       # 样式
├── main.js         # 导航交互（滚动阴影 + 汉堡菜单）
├── assets/
│   └── avatar.jpg  # 头像（当前为占位图，需替换）
└── README.md
```

## 本地预览

直接用浏览器打开 `index.html`，或在项目目录启动本地服务器：

```bash
cd website
python3 -m http.server 8000
# 访问 http://localhost:8000
```

## 需要替换的占位内容

在 `index.html` 中搜索 `TODO` 可找到所有占位项：

| 占位项 | 说明 |
|--------|------|
| `assets/avatar.jpg` | 替换为你的个人照片 |
| Google Scholar 链接 | 侧边栏图标 `href="#"` |
| GitHub 链接 | 侧边栏图标 `href="#"` |
| CV PDF 链接 | 侧边栏图标 `href="#"` |
| TaCauchy PDF / Code / BibTeX | 论文卡片中的链接 |
| News 占位条目 | 两条 `Placeholder for future news` |

## 部署到 GitHub Pages

1. 将 `website/` 目录推送到 GitHub 仓库（可单独建 repo，如 `username.github.io`）
2. 进入仓库 **Settings → Pages**
3. **Source** 选择 `Deploy from a branch`
4. **Branch** 选 `main`，文件夹选 `/ (root)` 或 `/docs`（若放在 docs 子目录）
5. 保存后等待几分钟，访问 `https://<username>.github.io`

> 若网站文件在子目录 `website/` 中，可将该目录内容移到仓库根目录，或在 Pages 设置中指定对应分支/路径。

## 技术说明

- 主题色：清华紫 `#660874`
- 字体：Inter（Google Fonts CDN）
- 图标：Font Awesome 6（CDN）
- 响应式断点：768px（≥768px 两栏，<768px 单栏堆叠）
