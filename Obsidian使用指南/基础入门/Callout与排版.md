# Callout 与排版

Callout 是 Obsidian 的彩色提示框，比普通引用更醒目，可折叠、可嵌套。

## 基本语法

```
> [!类型] 标题
> 内容文字
```

所有类型共用一个 `>`，内容中间空行也要加 `>`。

## 所有类型

| 类型 | 用途 |
|------|------|
| `note` | 普通笔记、补充说明 |
| `info` | 信息提示 |
| `tip` / `hint` | 技巧、小窍门 |
| `success` / `done` | 成功、已完成 |
| `warning` / `caution` | 警告、注意 |
| `danger` / `error` | 危险、错误 |
| `example` | 示例 |
| `quote` / `cite` | 引用 |
| `question` / `help` | 问题 |
| `abstract` / `summary` / `tldr` | 摘要、总结 |
| `bug` | Bug 记录 |
| `todo` | 待办提醒 |
| `checklist` | 检查清单 |
| `faq` | 常见问题 |

## 折叠

在类型后加 `+` 默认展开，加 `-` 默认折叠：

```
> [!tip]- 点击展开技巧
> 这段内容默认隐藏
```

## 嵌套

```
> [!info] 主提示
> 外层内容
> > [!warning] 嵌套警告
> > 内层警告内容
```

## 自定义标题

```
> [!note] 我的自定义标题
> 内容...
```

## 无标题

```
> [!note]
> 无标题的 Callout
```

## 排版建议

- **重要笔记**: 顶部用 `> [!abstract]` 做摘要
- **行动提醒**: 用 `> [!todo]` 标记待办
- **关键警告**: 用 `> [!warning]` 强调易错点
- **步骤教程**: 用 `> [!example]` 展示范例

---

## 相关
- [[Markdown语法速查]] — 基础排版语法，Callout 是其补充
- [[Mermaid图表]] — 在 Callout 中嵌入 Mermaid 图表增强表现力
- [[Properties与元数据]] — 用 `cssclasses` 属性自定义 Callout 外观

← 回到 [[00-目录|目录]]
