---
title: Markdown 速查表
icon: md
author: mattcone
category:
  - 教程
---

文章地址：

<VPBanner
  title=" Basic Syntax 速查表"
  content="The comprehensive Markdown reference guide.  <br>全面的 Markdown 参考指南。"
  logo="https://raw.githubusercontent.com/mattcone/markdown-guide/c4328bbbd7c9b975a4ed82e80c9c2d9822f1dc67/assets/images/markdown-mark.svg"
  :actions='[
	 {
		text: "访问",
		link:"https://www.markdownguide.org/cheat-sheet",
	 },{
		text: "仓库",
		link:"https://github.com/mattcone/markdown-guide",
		type: "default",
	 },{
		text: "汉化",
		link: "https://markdown.com.cn/cheat-sheet",
		type: "default",
	 },
  ]'
/>

---

## 总览

Markdown 速查表提供了所有 Markdown 语法元素的基本解释。如果你想了解某些语法元素的更多信息，请参阅更详细的 [基本语法](Markdown-Basic-Syntax) 和 [扩展语法](Markdown-Extended-Syntax).

## [基本语法](Markdown-Basic-Syntax)

这些是 John Gruber 的原始设计文档中列出的元素。所有 Markdown 应用程序都支持这些元素。

### [标题（Heading）](Markdown-Basic-Syntax#标题)

:::: md-demo 点击查看代码

# H1   
## H2   
### H3

::::

### [粗体（Bold）](Markdown-Basic-Syntax#粗体)

:::: md-demo 点击查看代码

**bold text**

::::

### [斜体（Italic）](Markdown-Basic-Syntax#斜体)

:::: md-demo 点击查看代码

*italicized text*

::::

### [引用块（Blockquote）](Markdown-Basic-Syntax#引用)

:::: md-demo 点击查看代码

> blockquote

::::

### [有序列表（Ordered List）](Markdown-Basic-Syntax#有序列表)

:::: md-demo 点击查看代码

1. First item
2. Second item
3. Third item

::::

### [无序列表（Unordered List）](Markdown-Basic-Syntax#无序列表)

:::: md-demo 点击查看代码

- First item   
- Second item   
- Third item

::::

### [代码（Code）](Markdown-Basic-Syntax#代码)

:::: md-demo 点击查看代码

`code`

::::

### [分隔线（Horizontal Rule）](Markdown-Basic-Syntax#分隔线)

:::: md-demo 点击查看代码

---

::::

### [链接（Link）](Markdown-Basic-Syntax#链接)

:::: md-demo 点击查看代码

[title](https://www.example.com)

::::

### [图片（Image）](Markdown-Basic-Syntax#图片)

:::: md-demo 点击查看代码

![alt text](example.jpg)

::::

## [扩展语法](Markdown-Extended-Syntax)

这些元素通过添加额外的功能扩展了基本语法。但是，并非所有 Markdown 应用程序都支持这些元素。

### [表格（Table）](Markdown-Extended-Syntax#表格)

:::: md-demo 点击查看代码

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

::::

### [代码块（Fenced Code Block）](Markdown-Extended-Syntax#围栏代码块)

:::: md-demo 点击查看代码

```
{
"firstName": "John",
"lastName": "Smith",
"age": 25
}
```

::::

### [脚注（Footnote）](Markdown-Extended-Syntax脚注)

:::: md-demo 点击查看代码

Here's a sentence with a footnote. [^1]
[^1]: This is the footnote.

::::

### [标题编号（Heading ID）](Markdown-Extended-Syntax#标题编号l)

:::: md-demo 点击查看代码

### My Great Heading {#custom-id}

::::

### [定义列表（Definition List）](Markdown-Extended-Syntax#定义列表)

:::: md-demo 点击查看代码

term  
: definition

::::

### [删除线（Strikethrough）](Markdown-Extended-Syntax#删除线)

:::: md-demo 点击查看代码

~~The world is flat.~~

::::

### [任务列表（Task List）](Markdown-Extended-Syntax#任务列表)

:::: md-demo 点击查看代码

- [x] Write the press release   
- [ ] Update the website   
- [ ] Contact the media

::::

## [非正式语法](Markdown-Hacks)

### [下划线（Underline）](Markdown-Hacks#下划线)

:::: md-demo 点击查看代码

Some of these words <ins>will be underlined</ins>.

::::

### [居中 （Center）](Markdown-Hacks#居中 )

:::: md-demo 点击查看代码

<p style="text-align:center">Center this text</p>

::::

### [颜色（Color）](Markdown-Hacks#颜色)

:::: md-demo 点击查看代码

<p style="color:blue">Make this text blue.</p>

::::

### [评论（Comments）](Markdown-Hacks#评论)

:::: md-demo 点击查看代码

Here's a paragraph that will be visible.

[This is a comment that will be hidden.]: # 

And here's another paragraph that's visible.

::::

### [警告（Admonitions）](Markdown-Hacks#警告)

:::: md-demo 点击查看代码

Some of these words <ins>will be underlined</ins>.

::::

### [图像尺寸（Image Size）](Markdown-Hacks#图像尺寸)

:::: md-demo 点击查看代码

<img src="./example.jpg" width="200" height="100">

::::

### [图片说明（Image Captions）](Markdown-Hacks#图片说明)

:::: md-demo 点击查看代码

<figure>
    <img src="./example.jpg"
         alt="Albuquerque, New Mexico">
    <figcaption>A single track trail outside of Albuquerque, New Mexico.</figcaption>
</figure>

::::

### [链接目标（Underline）](Markdown-Hacks#链接目标)

:::: md-demo 点击查看代码

<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>

::::

### [符号（Symbols）](Markdown-Hacks#符号)

:::: md-demo 点击查看代码

 &copy;

::::

### [表格格式（Table Formatting）](Markdown-Hacks#表格格式)

:::: md-demo 点击查看代码

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title |
| Paragraph   | First paragraph. <br><br> Second paragraph. |
| List        | Here's a list! <ul><li>Item one.</li><li>Item two.</li></ul> |

::::

### [## 目录（## Table of Contents）](Markdown-Hacks#目录)

:::: md-demo 点击查看代码

Table of Contents

- [Underline](#underline)
- [Indent](#indent)
- [Center](#center)
- [Color](#color)

::::

### [视频（Underline）](Markdown-Hacks#视频)

:::: md-demo 点击查看代码

[![Image alt text](https://img.youtube.com/vi/YOUTUBE-ID/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE-ID)

::::
