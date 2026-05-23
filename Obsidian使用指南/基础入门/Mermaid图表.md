# Mermaid 图表

Obsidian 原生支持 Mermaid 图表，在代码块中指定 `mermaid` 即可渲染。

## 流程图

````
```mermaid
graph TD
    A[开始] --> B{判断}
    B -->|是| C[执行A]
    B -->|否| D[执行B]
    C --> E[结束]
    D --> E
```
````

**方向**：`TD`(上下) / `LR`(左右) / `RL` / `BT`

**形状**：
```
A[矩形]      B(圆角)      C([椭圆])
D[[子程序]]   E[(数据库)]   F((圆形))
G{菱形判断}   H>标签]
```

## 时序图

````
```mermaid
sequenceDiagram
    用户->>服务器: 发送请求
    服务器->>数据库: 查询数据
    数据库-->>服务器: 返回结果
    服务器-->>用户: 响应数据
```
````

## 类图

````
```mermaid
classDiagram
    class Animal {
        +String name
        +void eat()
    }
    class Dog {
        +void bark()
    }
    Animal <|-- Dog
```
````

## 甘特图

````
```mermaid
gantt
    title 项目计划
    dateFormat  YYYY-MM-DD
    section 阶段一
    需求分析    :a1, 2026-06-01, 7d
    原型设计    :a2, after a1, 5d
    section 阶段二
    开发        :b1, after a2, 14d
    测试        :b2, after b1, 5d
```
````

## 饼图

````
```mermaid
pie title 时间分配
    "阅读" : 35
    "写作" : 25
    "复习" : 20
    "整理" : 15
    "其他" : 5
```
````

---

## 相关
- [[Callout与排版]] — 配合 Callout 让笔记图文并茂
- [[Canvas白板]] — Canvas 中也可嵌入 Mermaid 图表
- [[Markdown语法速查]] — Markdown 基础语法，代码块是 Mermaid 的载体

← 回到 [[00-目录|目录]]
