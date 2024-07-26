---
title: Markdown 非正式语法
icon: md
author: mattcone
category:
  - 教程
---

文章地址：

<VPBanner
  title=" Hack 非正式语法"
  content="Workarounds for things not officially supported by Markdown.<br>针对 Markdown 未正式支持的内容的解决方法"
  logo="https://raw.githubusercontent.com/mattcone/markdown-guide/c4328bbbd7c9b975a4ed82e80c9c2d9822f1dc67/assets/images/markdown-mark.svg"
  :actions='[
	 {
		text: "访问",
		link:"https://markdownguide.offshoot.io/hacks/",
	 },{
		text: "仓库",
		link:"https://github.com/mattcone/markdown-guide",
		type: "default",
	 },
  ]'
/>

---

针对 Markdown 未正式支持的内容的解决方法。

## Markdown 非正式语法

大多数使用 Markdown 的人会发现[基本](Markdown-Basic-Syntax)和[扩展语法](Markdown-Extended-Syntax)元素可以满足他们的需求。但是，如果你使用 Markdown 的时间足够长，你很可能会发现它不支持你需要的某些东西。本页提供了解决 Markdown 限制的技巧和窍门。

> [!tip] 提示：
> 
> 这些技巧不一定适用于您的 Markdown 应用程序。如果您需要经常使用这些技巧，则应考虑使用 Markdown 以外的其他语言进行写作。

## 下划线

带下划线的文本在网页写作中并不常见，可能是因为带下划线的文本几乎与链接同义。但是，如果您正在撰写论文或报告，则可能需要为单词和短语添加下划线的功能。一些应用程序（如[Bear](https://markdownguide.offshoot.io/tools/bear/)和[Simplenote）](https://markdownguide.offshoot.io/tools/simplenote/)支持为文本添加下划线，但 Markdown 本身并不支持下划线。如果您的 Markdown 处理器支持[HTML](Markdown-Basic-Syntax#html)，则可以使用`<ins>`HTML 标签为文档中的文本添加下划线。

```
Some of these words <ins>will be underlined</ins>.
```

渲染的输出如下所示：

Some of these words <ins>will be underlined</ins>.

## 缩进（Tab）

在 Markdown 中，制表符和空格具有特殊含义。您可以使用尾随空格来创建[换行符](Markdown-Basic-Syntax#换行)，也可以使用制表符来创建[代码块](Markdown-Basic-Syntax#代码)。但是，如果您需要使用制表符键以传统方式缩进段落，该怎么办？Markdown 并未提供简单的方法来实现这一点。

最好的办法可能是使用支持缩进的 Markdown 编辑器。这在更面向桌面出版的应用程序中很常见。例如，[iA Writer](https://markdownguide.offshoot.io/tools/ia-writer/)允许您在应用程序首选项中自定义编辑器的缩进设置。它还提供模板自定义选项，以便您可以使呈现的文档看起来符合您的预期，包括缩进等。

[如果您的 Markdown 处理器支持HTML](Markdown-Basic-Syntax#html) ，则另一个选项是使用 HTML 实体表示不间断空格 ( `&nbsp;`)。这可能应该是您的最后选择，因为它可能会变得很尴尬。基本上，`&nbsp;`Markdown 源中的每个 都将在渲染输出中替换为空格。因此，如果您在`&nbsp;`段落前放置四个 ，则该段落看起来就像缩进了四个空格。

```
&nbsp;&nbsp;&nbsp;&nbsp;This is the first sentence of my indented paragraph.
```

渲染的输出如下所示：

    这是我的缩进段落的第一句话。

## 居中

在撰写论文或报告时，居中文本是必需的。不幸的是，Markdown 没有任何文本对齐的概念（使用[表格](Markdown-Extended-Syntax#表格)时可能存在例外）。好消息是您可以使用 HTML 标签：`<center>`。如果您的 Markdown 处理器支持[HTML](Markdown-Basic-Syntax#html)，您可以将这些标签放在您想要居中对齐的任何文本周围。

```
<center>This text is centered.</center>
```

渲染的输出如下所示：

<center>This text is centered.</center>

HTML标签`<center>`在技术上是受支持的，但官方[已弃用](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/center)，这意味着它目前可用，但您不应该使用它。不幸的是，没有其他纯 HTML 替代方案。您可以尝试使用其中一种 CSS 替代方案。并非所有 Markdown 应用程序都提供 CSS 支持，但如果您使用的应用程序提供 CSS 支持，这里有一个标签的替代方案`<center>`：

```
<p style="text-align:center">Center this text</p>
```

如果您的 Markdown 应用程序支持此功能，则输出如下所示：

<p style="text-align:center">Center this text</p>

## 颜色

Markdown 不允许你更改文本的颜色，但如果你的 Markdown 处理器支持[HTML]Markdown-Basic-Syntax#html)，则可以使用`<font>`HTML 标签。该`color`属性允许你使用颜色名称或十六进制`#RRGGBB`代码指定字体颜色。

```
<font color="red">This text is red!</font>
```

渲染的输出如下所示：

<font color="red">This text is red!</font>

HTML标签`<font>`在技术上是受支持的，但官方[已弃用](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/font)，这意味着它目前可用，但您不应该使用它。不幸的是，没有其他纯 HTML 替代方案。您可以尝试使用其中一种 CSS 替代方案。并非所有 Markdown 应用程序都提供 CSS 支持，但如果您使用的应用程序提供 CSS 支持，这里有一个标签的替代方案`<font>`：

```
<p style="color:blue">Make this text blue.</p>
```

如果您的 Markdown 应用程序支持此功能，则输出如下所示：

<p style="color:blue">Make this text blue.</p>

## 注释

有些人需要能够在 Markdown 文件中编写_不会_出现在渲染输出中的句子。这些注释本质上是隐藏文本。文本可供文档作者查看，但不会打印在网页或 PDF 上。Markdown 本身不支持注释，但一些有进取心的人已经想出了一个解决方案。

要添加注释，请将文本放在括号内，后跟冒号、空格和磅号（例如`[comment]: #`）。注释前后应留空行。

```
Here's a paragraph that will be visible.

[This is a comment that will be hidden.]: # 

And here's another paragraph that's visible.
```

Here's a paragraph that will be visible.

[This is a comment that will be hidden.]: # 

And here's another paragraph that's visible.

 **提示：**此技巧来自[Stack Overflow](https://stackoverflow.com/questions/4823468/comments-in-markdown)。它已通过同行评审，并被数千人使用！

## 警告

警告经常用于文档中，以引起对警告、说明和提示的注意。Markdown 没有提供警告的特殊语法，大多数 Markdown 应用程序也不支持警告（[MkDocs](https://markdownguide.offshoot.io/tools/mkdocs/)除外）。

但是，如果您需要添加警告，您可能能够使用带有[表情符号](https://markdownguide.offshoot.io/extended-syntax/#emoji)和[强调](Markdown-Basic-Syntax#强调)的[块](Markdown-Basic-Syntax#引用)引用来创建与您在其他网站上看到的警告类似的内容。

```
> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.
```

渲染的输出如下所示：

> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.

## 图片大小

[Markdown 的图像](Markdown-Basic-Syntax#图片)语法不允许您指定图像的宽度和高度。如果您需要调整图像大小并且您的 Markdown 处理器支持[HTML](Markdown-Basic-Syntax#html)，则可以使用`img`带有`width`和`height`属性的 HTML 标签来设置图像的尺寸（以像素为单位）。

```
<img src="image.png" width="200" height="100">
```

渲染的输出将包含调整为您所指定尺寸的图像。例如：

<img src="../Markdown/example.jpg" width="200" height="100">

## 图片说明

Markdown 本身不支持图像标题，但有两种可能的解决方法。如果您的 Markdown 应用程序支持[HTML](https://markdownguide.offshoot.io/basic-syntax/#html)，则可以使用`figure`和`figcaption`HTML 标签为图像添加标题。

```
<figure>
    <img src="/assets/images/albuquerque.jpg"
         alt="Albuquerque, New Mexico">
    <figcaption>A single track trail outside of Albuquerque, New Mexico.</figcaption>
</figure>
```

渲染的输出如下所示：

![新墨西哥州阿尔伯克基](https://mdg.imgix.net/assets/images/albuquerque.jpg)

新墨西哥州阿尔伯克基市郊外的一条单行道。

 **提示：**如果您的 Markdown 应用程序支持 CSS，您可以使用 CSS 来设置标题的外观。

如果您的 Markdown 应用程序不支持 HTML，您可以尝试将标题直接放在图像下方并使用[强调](https://markdownguide.offshoot.io/basic-syntax/#emphasis)。

```
![Albuquerque, New Mexico](/assets/images/albuquerque.jpg)
*A single track trail outside of Albuquerque, New Mexico.*
```

渲染的输出如下所示：

![新墨西哥州阿尔伯克基](https://mdg.imgix.net/assets/images/albuquerque.jpg)

_新墨西哥州阿尔伯克基市郊外的一条单行道。_

## 链接目标

[有些人喜欢创建在新标签页或窗口中打开的链接。Markdown 的链接](https://markdownguide.offshoot.io/basic-syntax/#links)语法不允许您指定该`target`属性，但如果您的 Markdown 处理器支持[HTML](https://markdownguide.offshoot.io/basic-syntax/#html)，则您可以使用 HTML 来创建这些链接。

```
<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>
```

渲染的输出如下所示：

[学习Markdown！](https://www.markdownguide.org/)

## 符号

Markdown 不提供符号的特殊语法。但是，在大多数情况下，您可以将要使用的任何符号复制并粘贴到 Markdown 文档中。例如，如果您需要显示 Pi (π)，只需在网页上找到该符号，然后将其复制并粘贴到文档中。该符号应按预期显示在渲染输出中。

或者，如果您的 Markdown 应用程序支持[HTML](https://markdownguide.offshoot.io/basic-syntax/#html)，则可以使用 HTML 实体来表示您想要使用的任何符号。例如，如果您想要显示版权符号 (©)，则可以将版权的 HTML 实体 ( `&copy;`) 复制并粘贴到您的 Markdown 文档中。

以下是 HTML 符号实体的部分列表：

- 版权 (©) —`&copy;`
- 注册商标（®）—`&reg;`
- 商标 (™) —`&trade;`
- 欧元 (€) —`&euro;`
- 左箭头 (←) —`&larr;`
- 向上箭头 (↑) —`&uarr;`
- 向右箭头 (→) —`&rarr;`
- 向下箭头 (↓) —`&darr;`
- 度 (°) —`&#176;`
- 圆周率 (π) —`&#960;`

有关可用 HTML 实体的完整列表，请参阅 Wikipedia 的[HTML 实体](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references)页面。

## 表格格式

Markdown[表格](https://markdownguide.offshoot.io/extended-syntax/#tables)非常挑剔。您无法使用许多 Markdown 语法元素来格式化表格单元格中的文本。但至少有两个常见的表格问题有解决方法：换行符和列表。

### 表格单元格内的换行符

您可以使用一个或多个`<br>`HTML 标签分隔表格单元格内的段落。

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title |
| Paragraph   | First paragraph. <br><br> Second paragraph. |
```

渲染的输出如下所示：

|句法|描述|
|---|---|
|标头|标题|
|段落|第一段。  <br>  <br>第二段。|

### 表格单元格内的列表

您可以使用 HTML 标签在表格单元格内添加列表。

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title |
| List        | Here's a list! <ul><li>Item one.</li><li>Item two.</li></ul> |
```

渲染的输出如下所示：

|句法|描述|
|---|---|
|标头|标题|
|列表|这是一个清单！<br><br>- 第一项。<br>- 第二项。|

## 目录

一些 Markdown 应用程序（例如[Markdeep）可以根据](https://markdownguide.offshoot.io/tools/markdeep/)[标题](https://markdownguide.offshoot.io/basic-syntax/#headings)自动生成目录（也称为_toc_），但并非所有 Markdown 应用程序都提供此功能。但是，如果您的 Markdown 应用程序支持[标题 ID ，则可以使用](https://markdownguide.offshoot.io/extended-syntax/#heading-ids)[列表](https://markdownguide.offshoot.io/basic-syntax/#lists-1)和一些[链接](https://markdownguide.offshoot.io/basic-syntax/#links)为您的 Markdown 文件创建目录。[](https://markdownguide.offshoot.io/basic-syntax/#headings)[](https://markdownguide.offshoot.io/extended-syntax/#heading-ids)[](https://markdownguide.offshoot.io/basic-syntax/#lists-1)[](https://markdownguide.offshoot.io/basic-syntax/#links)

```
#### Table of Contents

- [Underline](#underline)
- [Indent](#indent)
- [Center](#center)
- [Color](#color)
```

渲染的输出如下所示：

#### 目录

- [强调](https://markdownguide.offshoot.io/hacks/#underline)
- [缩进](https://markdownguide.offshoot.io/hacks/#indent)
- [中心](https://markdownguide.offshoot.io/hacks/#center)
- [颜色](https://markdownguide.offshoot.io/hacks/#color)

## 视频

如果您的 Markdown 应用程序支持[HTML](https://markdownguide.offshoot.io/basic-syntax/#html)，您应该能够通过复制和粘贴 YouTube 或 Vimeo 等视频网站提供的 HTML 代码将视频嵌入到您的 Markdown 文件中。如果您的 Markdown 应用程序不支持 HTML ，您就无法嵌入视频，但您可以通过添加图片[和](https://markdownguide.offshoot.io/basic-syntax/#images-1)视频链接来做到这一点。您几乎可以对任何视频服务上的任何视频执行此操作。

由于 YouTube 简化了这一过程，我们将以它们为例。以这个视频为例：`https://www.youtube.com/watch?v=8q2IjQOzVpE`。URL 的最后一部分 ( `8q2IjQOzVpE`) 是视频的 ID。我们可以获取该 ID 并将其放入以下模板中：

```test
[![Image alt text](https://img.youtube.com/vi/YOUTUBE-ID/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE-ID)
```

YouTube 会自动为每个视频生成一张图片 ( `https://img.youtube.com/vi/YOUTUBE-ID/0.jpg`)，因此我们可以使用该图片并将[图片链接](https://markdownguide.offshoot.io/basic-syntax/#linking-images)到 YouTube 上的视频。替换图片替代文本并添加视频 ID 后，我们的示例如下所示：

```test
[![Less Than Jake — Scott Farcas Takes It On The Chin](https://img.youtube.com/vi/PYCxct2e0zI/0.jpg)](https://www.youtube.com/watch?v=PYCxct2e0zI)
```

渲染的输出如下所示：

[![比杰克还差——斯科特·法卡斯承受了巨大的打击](https://img.youtube.com/vi/PYCxct2e0zI/0.jpg)](https://www.youtube.com/watch?v=PYCxct2e0zI)