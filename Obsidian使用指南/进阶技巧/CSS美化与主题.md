# CSS 美化与主题

## 主题市场

`设置 → 外观 → 主题 → 管理` 浏览社区主题。

### 热门主题推荐

| 主题 | 风格 |
|------|------|
| **Minimal** | 极简干净，高度可定制 |
| **Blue Topaz** | 功能丰富，中文优化 |
| **AnuPpuccin** | 柔和色彩，圆角设计 |
| **Things** | macOS 风格，精致优雅 |

点击安装后即可应用，后续可在"主题"下拉菜单随时切换。

## 字体与基础设置

`设置 → 外观` 中：

- **基础字体**: 界面 UI 字体
- **正文字体**: 编辑器/阅读模式字体
- **代码字体**: 代码块字体
- **字体大小**: 正文默认大小
- **快速调整**: `Ctrl+滚轮` 实时缩放

推荐中文字体组合：
```
正文: 霞鹜文楷 / 思源宋体
代码: JetBrains Mono / Fira Code
界面字体: 使用默认即可
```

## CSS Snippets（自定义片段）

在不修改主题的前提下注入自定义 CSS。

### 创建位置

`.obsidian/snippets/` 文件夹下放 `.css` 文件，然后在 `设置 → 外观 → CSS 代码片段` 中刷新并启用。

### 常用片段

**1. 图片居中与最大宽度**
```css
img {
  display: block;
  margin: 0 auto;
  max-width: 100%;
}
```

**2. 加宽编辑区**
```css
.markdown-source-view, .markdown-preview-view {
  max-width: 900px;
  margin: 0 auto;
}
```

**3. 隐藏特定文件夹（如模板）的标题栏**
```css
.nav-folder-title[data-path="模板"] {
  display: none;
}
```

**4. 更明显的粗体**
```css
strong {
  color: var(--text-accent);
}
```

## Style Settings 插件

搭配 **Style Settings** 社区插件使用，可在 `设置` 面板中用滑块和开关微调主题参数（颜色、圆角、字体大小等），无需写 CSS。

---

## 相关
- [[社区插件精选]] — Style Settings 插件让主题调节可视化
- [[Callout与排版]] — Callout 可以通过 CSS snippet 自定义样式
- [[Properties与元数据]] — `cssclasses` 属性为单篇笔记加载特定 CSS

← 回到 [[00-目录|目录]]
