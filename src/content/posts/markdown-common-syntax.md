---
title: Markdown 常用写法速查：博客编辑入门
published: 2026-08-22
description: 整理一些写博客时最常用的 Markdown 语法，方便以后随写随查。
tags: [Markdown, 博客写作, 入门]
category: 学习笔记
draft: false
---

Markdown 是一种轻量级标记语言。写文章时只需要在文字前后加上一些简单符号，就能排出标题、列表、链接、代码块等常见格式。

这篇文章整理了一份够日常写博客使用的 Markdown 小抄，也顺便作为博客升级后的第一篇测试文章。

## 标题

标题使用 `#` 表示，`#` 越多，标题层级越低：

```markdown
# 一级标题
## 二级标题
### 三级标题
```

通常一篇文章只需要从二级标题开始组织正文，因为文章标题已经由 frontmatter 中的 `title` 提供了。

## 粗体、斜体与删除线

```markdown
**这是粗体**
*这是斜体*
~~这是删除线~~
`这是一小段行内代码`
```

显示效果：**这是粗体**、*这是斜体*、~~这是删除线~~，以及 `行内代码`。

## 列表

无序列表可以使用 `-`：

```markdown
- 第一项
- 第二项
  - 第二项的子项目
```

有序列表则使用数字加英文句点：

```markdown
1. 打开文章文件
2. 编辑正文
3. 保存并预览
```

## 引用

在一行开头添加 `>` 就能创建引用：

```markdown
> 写作是思考留下的脚印。
```

> 写作是思考留下的脚印。

## 链接与图片

链接的写法是 `[显示文字](网址)`：

```markdown
[访问我的博客](https://lonako-blog.bocchi0708.workers.dev/)
```

图片只比链接多一个感叹号：

```markdown
![图片说明](./images/example.avif)
```

博客文章自己的图片可以放进 `src/content/posts/images/`，然后使用相对路径引用。

## 代码块

短代码可以用一对反引号包住。较长的代码则放在三对反引号之间，并在开头注明语言以启用语法高亮：

````markdown
```javascript
const message = "Hello, Markdown!";
console.log(message);
```
````

效果如下：

```javascript
const message = "Hello, Markdown!";
console.log(message);
```

## 表格

```markdown
| 语法 | 用途 |
| --- | --- |
| `#` | 标题 |
| `-` | 列表 |
| `>` | 引用 |
```

| 语法 | 用途 |
| --- | --- |
| `#` | 标题 |
| `-` | 列表 |
| `>` | 引用 |

## 分割线与待办事项

单独输入三个短横线可以添加分割线：

```markdown
---
```

待办列表则这样写：

```markdown
- [x] 写完文章
- [x] 本地预览
- [ ] 继续更新博客
```

- [x] 写完文章
- [x] 本地预览
- [ ] 继续更新博客

## 文章开头的 frontmatter

这个博客的每篇文章都要以一段 frontmatter 开头，用来设置标题、日期、分类等信息：

```yaml
---
title: 文章标题
published: 2026-08-22
description: 一句话介绍文章内容
tags: [标签一, 标签二]
category: 学习笔记
draft: false
---
```

其中 `draft: true` 表示草稿，不会正常公开；准备发布时记得改为 `false`。

## 最后

Markdown 的核心不是记住所有语法，而是让注意力留在内容本身。标题、列表、链接、图片和代码块已经足够完成大多数博客文章；忘记写法时，再回来翻一下这份小抄就好。
