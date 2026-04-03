# Ankr的个人主页

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-blue?logo=github)](https://ankr.github.io)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)

这是一个极简主义风格的个人主页，专为工商业分布式光伏从业者设计。

## 🌟 特性

- **极简科技风**：深色背景搭配光伏蓝/能源绿点缀色
- **动态粒子背景**：Canvas 实现的能量网络动画
- **打字机效果**：展示职业身份
- **玻璃拟态设计**：现代化卡片布局
- **GitHub 集成**：自动获取并展示最新仓库
- **响应式设计**：完美适配桌面和移动设备
- **无构建步骤**：纯 HTML + Tailwind CSS (CDN) + Vanilla JS

## 🚀 部署到 GitHub Pages

### 方法一：自动部署（推荐）

1. 确保此仓库名为 `ankr.github.io`
   ```bash
   # 如果当前仓库名不是这个，请在 GitHub 上重命名
   ```

2. 启用 GitHub Pages：
   - 进入仓库 **Settings** > **Pages**
   - Source 选择 **Deploy from a branch**
   - Branch 选择 **main** (或 master)
   - Folder 选择 **/(root)**
   - 点击 **Save**

3. 等待几分钟，访问：https://ankr.github.io

### 方法二：手动推送

```bash
# 提交更改
git add .
git commit -m "feat: 添加个人主页"
git push origin main
```

## 📁 文件结构

```
ankr.github.io/
├── index.html          # 主页面（包含所有样式和脚本）
└── README.md           # 说明文档
```

## 🎨 自定义

### 修改个人信息
编辑 `index.html` 中的以下内容：

- **头像**：搜索 `img src` 替换 URL
- **邮箱**：搜索 `angkorwu@gmail.com` 替换
- **介绍文字**：搜索 `工商业分布式光伏产业从业` 修改
- **技能条**：调整 `width: 90%` 等百分比

### 颜色主题
在 `<script>` 标签内的 `tailwind.config` 中修改 `solar` 颜色值：

```javascript
colors: {
    solar: {
        400: '#22d3ee', // 主色调
        500: '#0ea5e9', // 悬停色
        600: '#0284c7', // 深色
    }
}
```

## 🛠️ 技术栈

- HTML5
- Tailwind CSS (v3 via CDN)
- Vanilla JavaScript
- FontAwesome (图标)
- Google Fonts (Inter 字体)

## 📄 许可证

MIT License

---

**Built with ❤️ by Ankr Wu**
