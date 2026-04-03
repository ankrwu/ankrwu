# Ankr Wu - 个人主页

这是一个极简主义风格的个人主页，专为工商业分布式光伏产业从业者设计。

## 🌟 特性

- **极简设计**：简单大方，略带科技感
- **动态效果**：
  - Canvas 粒子网络背景动画（象征能源连接）
  - 打字机效果展示职业身份
  - 滚动淡入动画
  - 玻璃拟态卡片设计
- **技术栈**：
  - 原生 HTML + CSS + JavaScript
  - Tailwind CSS (CDN 引入)
  - GitHub API 自动获取项目
- **响应式设计**：完美适配桌面和移动设备

## 🚀 部署到 GitHub Pages

### 方法一：使用 GitHub Actions（推荐）

1. 在本仓库根目录创建 `.github/workflows/deploy.yml`：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches:
      - main

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Setup Pages
        uses: actions/configure-pages@v4
      
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: '.'
      
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

2. 提交并推送代码：
```bash
git add .
git commit -m "Add personal website"
git push origin main
```

3. 在 GitHub 仓库设置中：
   - 进入 Settings → Pages
   - Source 选择 "GitHub Actions"
   - 等待部署完成

### 方法二：直接使用 gh-pages 分支

1. 创建 gh-pages 分支：
```bash
git checkout --orphan gh-pages
git reset --hard
git add .
git commit -m "Deploy personal website"
git push origin gh-pages --force
```

2. 在 GitHub 仓库设置中：
   - 进入 Settings → Pages
   - Source 选择 "gh-pages" 分支
   - 保存后等待几分钟

## 📱 访问地址

部署完成后，您的网站将在以下地址可用：

```
https://ankr.github.io/
```

## 🎨 自定义

### 修改个人信息

编辑 `index.html` 文件中的以下内容：

- **姓名**：搜索 "Ankr Wu" 进行替换
- **职业描述**：搜索 "工商业分布式光伏产业从业者"
- **联系方式**：搜索 "angkorwu@gmail.com"
- **头像**：修改 img 标签的 src 属性
- **统计数据**：在 About 部分修改数字

### 调整颜色主题

在 `index.html` 的 Tailwind 配置部分修改颜色：

```javascript
colors: {
    'solar-blue': '#0ea5e9',  // 主色调
    'solar-green': '#10b981', // 辅助色
}
```

## 📄 文件结构

```
.
├── index.html          # 主页面
└── README.md           # 说明文档
```

## 🌐 技术细节

- **粒子动画**：使用 HTML5 Canvas 实现，模拟能源网络连接效果
- **打字机效果**：纯 JavaScript 实现，展示职业身份
- **GitHub API**：自动获取并展示最新的 6 个仓库
- **玻璃拟态**：使用 backdrop-filter 实现磨砂玻璃效果
- **响应式导航**：移动端自动切换为汉堡菜单

## 📞 联系

- **Email**: angkorwu@gmail.com
- **GitHub**: https://github.com/ankr

---

**Powered by clean energy & clean code** ⚡🌱
