# Dataview 入门

Dataview 是 Obsidian 最强大的数据查询插件，把笔记库变成可查询的数据库。

## 数据来源

Dataview 从笔记中读取两类数据：

**1. Properties (Frontmatter)**
```
---
rating: 5
author: 卡尔维诺
genre: [小说, 文学]
---
```

**2. 行内字段**
```
作者:: 卡尔维诺
评分:: 5
```

## 三种查询类型

### LIST — 列出笔记

```dataview
LIST
FROM "读书笔记"
WHERE rating >= 4
SORT rating DESC
```

### TABLE — 表格展示

```dataview
TABLE author, rating, genre
FROM "读书笔记"
SORT rating DESC
LIMIT 10
```

### TASK — 汇总任务

```dataview
TASK
FROM "日记"
WHERE !completed
SORT file.name DESC
```

## 常用操作

| 语法 | 作用 |
|------|------|
| `FROM "文件夹名"` | 限定范围 |
| `FROM #标签` | 按标签筛选 |
| `WHERE rating > 3` | 条件过滤 |
| `SORT file.ctime DESC` | 排序 |
| `LIMIT 10` | 限制数量 |
| `FLATTEN genre` | 展开数组 |
| `GROUP BY author` | 分组聚合 |

## 实用查询模板

**书单表格**
```dataview
TABLE author, rating, date AS "读完日期"
FROM #书单
WHERE rating >= 3
SORT rating DESC
```

**当月日记列表**
```dataview
LIST
FROM "日记"
WHERE file.day.month = date(now).month
SORT file.day DESC
```

**未完成任务汇总**
```dataview
TASK
FROM "项目"
WHERE !completed
GROUP BY file.link
```

---

## 相关
- [[标签与搜索]] — 标签是 Dataview 的重要筛选条件
- [[Properties与元数据]] — Properties 是 Dataview 的核心数据来源
- [[模板与自动化]] — 配合 Templater 自动生成带 Dataview 的面板
- [[社区插件精选]] — DB Folder、Projects 等替代方案

← 回到 [[00-目录|目录]]
