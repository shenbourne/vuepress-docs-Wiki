---
title: Markdown 基本语法
icon: md
author: mattcone
category:
  - 教程
---

文章地址：

<VPBanner
  title=" Basic Syntax 基本语法"
  content="The comprehensive Markdown reference guide.  <br>全面的 Markdown 参考指南。"
  logo="https://raw.githubusercontent.com/mattcone/markdown-guide/c4328bbbd7c9b975a4ed82e80c9c2d9822f1dc67/assets/images/markdown-mark.svg"
  :actions='[
	 {
		text: "访问",
		link:"https://www.markdownguide.org/basic-syntax",
	 },{
		text: "仓库",
		link:"https://github.com/mattcone/markdown-guide",
		type: "default",
	 },{
		text: "汉化",
		link: "https://markdown.com.cn/basic-syntax/",
		type: "default",
	 },
  ]'
/>

---

## Markdown 基本语法

Markdown是一种轻量级标记语言，排版语法简洁，让人们更多地关注内容本身而非排版。它使用易读易写的纯文本格式编写文档，可与HTML混编，可导出 HTML、PDF 以及本身的 .md 格式的文件。因简洁、高效、易读、易写，Markdown被大量使用，如Github、Wikipedia、简书等。

在线体验一下 [Markdown在线编辑器](https://markdown.com.cn/editor/)。

千万不要被「标记」、「语言」吓到，Markdown的语法十分简单，常用的标记符号不超过十个，用于日常写作记录绰绰有余，不到半小时就能完全掌握。

就是这十个不到的标记符号，却能让人**优雅地沉浸式记录，专注内容而不是纠结排版**，达到「心中无尘，码字入神」的境界。

## 标题
 
要创建标题，请在单词或短语前添加数字符号 （ `#` ）。您使用的数字符号数量应与标题级别相对应。例如，要创建标题级别三 （ `<h3>` ），请使用三个数字符号（例如 `### My Header` ）。

|Markdown|HTML|输出|
|---|---|---|
|`# Heading level 1`|`<h1>Heading level 1</h1>`|<h1>Heading level 1</h1>|
|`## Heading level 2`|`<h2>Heading level 2</h2>`|<h2>Heading level 2</h2>|
|`### Heading level 3`|`<h3>Heading level 3</h3>`|<h3>Heading level 3</h3>|
|`#### Heading level 4`|`<h4>Heading level 4</h4>`|<h4>Heading level 4</h4>|
|`##### Heading level 5`|`<h5>Heading level 5</h5>`|<h5>Heading level 5</h5>|
|`###### Heading level 6`|`<h6>Heading level 6</h6>`|<h6>Heading level 6</h6>|

### 可选语法

或者，在文本下方的行上，为标题级别 1 添加任意数量的 `==` 字符，或 `--` 为标题级别 2 添加字符。

|Markdown|HTML|输出|
|---|---|---|
|`Heading level 1`<br>`===============`|`<h1>Heading level 1</h1>`|<h1>Heading level 1</h1>|
|`Heading level 2`<br>`---------------`|`<h2>Heading level 2</h2>`|<h2>Heading level 2</h2>|

#### 标题惯例用法

Markdown 应用程序对于如何处理数字符号 （ `#` ） 和标题名称之间缺失的空格没有达成一致。为了兼容，请始终在数字符号和标题名称之间留一个空格。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`# Here's a Heading`|`#Here's a Heading`|

为了兼容，您还应该在标题前后放置空行。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`Try to put a blank line before...`<br><br>`# Heading`<br><br>`...and after a heading.`|`Without blank lines, this might not look right.`<br>`# Heading`<br>`Don't do this!`|

## 段落

要创建段落，请使用空行分隔一行或多行文本。

|Markdown|HTML|输出|
|---|---|---|
|`I really like using Markdown.`<br><br>`I think I'll use it to format all of my documents from now on.`|`<p>I really like using Markdown.</p>`<br><br>`<p>I think I'll use it to format all of my documents from now on.</p>`|I really like using Markdown. <br><br>I think I'll use it to format all of my documents from now on.|

#### 段落惯例用法


除非[段落](#段落)位于列表中，否则不要缩进带有空格或制表符的段落。

注意：如果需要在输出中缩进段落，可以用 HTML 实体表示不间断空格 ( `&nbsp;`)

|✅ 执行此操作|❌ 别这样|
|---|---|
|`Don't put tabs or spaces in front of your paragraphs.`<br><br>`Keep lines left-aligned like this.`<br><br>``|`This can result in unexpected formatting problems.`<br><br>`  Don't add tabs or spaces in front of paragraphs.`|

## 换行

若要创建换行符或换行符 （ `<br>` ），请用两个或多个空格结束一行，然后键入 return。

|Markdown|HTML|输出|
|---|---|---|
|`This is the first line.`<br>`  And this is the second line.`|`<p>This is the first line.<br>`<br>`And this is the second line.</p>`|This is the first line. <br>And this is the second line. |

#### 换行惯例用法

在几乎每个 Markdown 应用程序中，您都可以使用两个或更多空格（通常称为“尾随空格”）来换行，但这是有争议的。在编辑器中很难看到尾随空格，许多人无意或有意地在每个句子后放置两个空格。出于这个原因，您可能希望使用尾随空格以外的其他内容来换行。如果你的 Markdown 应用程序支持 [HTML](#html)，你可以使用 `<br>` HTML 标签。
 
为了兼容起见，请在行尾使用空格或 `<br>` HTML 标记。
 
我不建议使用另外两个选项。CommonMark 和其他一些轻量级标记语言允许您在行尾键入反斜杠 （ `\` ），但并非所有 Markdown 应用程序都支持此功能，因此从兼容性的角度来看，它不是一个好的选择。而且，至少有几个轻量级标记语言不需要在行尾添加任何内容——只需键入 return，它们就会创建一个换行符。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`First line with two spaces after.  `<br>`And the next line.`<br><br>`First line with the HTML tag after.<br>`<br>`And the next line.`|`First line with a backslash after.\`<br>`And the next line.`<br><br>`First line with nothing after.`<br>`And the next line.`|

## 强调

您可以通过将文本设为粗体或斜体来添加强调。

### 粗体
 
对于粗体文本，请在单词或短语前后添加两个星号或下划线。要将单词的中间加粗以强调，请在字母周围添加两个星号，不带空格。

|Markdown|HTML|输出|
|---|---|---|
|`I just love **bold text**.`|`I just love <strong>bold text</strong>.`|I just love **bold text**.  <br>|
|`I just love __bold text__.`|`I just love <strong>bold text</strong>.`|I just love **bold text**.  <br>|
|`Love**is**bold`|`Love<strong>is</strong>bold`|Love**is**bold |

#### 粗体惯例用法

Markdown 应用程序在如何处理单词中间的下划线方面没有达成一致。为了兼容，请使用星号将单词的中间加粗以强调。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`Love**is**bold`|`Love__is__bold`|

### 斜体

若要将文本斜体化，请在单词或短语前后添加一个星号或下划线。要将单词的中间斜体化以示强调，请在字母周围添加一个星号，不带空格。

|Markdown|HTML|输出|
|---|---|---|
|`Italicized text is the *cat's meow*.`|`Italicized text is the <em>cat's meow</em>.`|Italicized text is the _cat’s meow_.  <br>|
|`Italicized text is the _cat's meow_.`|`Italicized text is the <em>cat's meow</em>.`|Italicized text is the _cat’s meow_.  <br>|
|`A*cat*meow`|`A<em>cat</em>meow`|A_cat_meow |

#### 斜体惯例用法

Markdown 应用程序在如何处理单词中间的下划线方面没有达成一致。为了兼容，请使用星号将单词的中间斜体化以强调。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`A*cat*meow`|`A_cat_meow`|

### 粗体和斜体

要同时使用粗体和斜体强调文本，请在单词或短语前后添加三个星号或下划线。要将单词的中间加粗和斜体以强调，请添加三个星号，字母周围不带空格。

|Markdown|HTML|输出|
|---|---|---|
|`This text is ***really important***.`|`This text is <em><strong>really important</strong></em>.`|This text is _**really important**_.  <br>|
|`This text is ___really important___.`|`This text is <em><strong>really important</strong></em>.`|This text is _**really important**_.  <br>|
|`This text is __*really important*__.`|`This text is <em><strong>really important</strong></em>.`|This text is _**really important**_.  <br>|
|`This text is **_really important_**.`|`This text is <em><strong>really important</strong></em>.`|This text is _**really important**_.  <br>|
|`This is really***very***important text.`|`This is really<em><strong>very</strong></em>important text.`|This is really_**very**_important text.  <br>|

> [!note] 注意
>  `em` and `strong` 标记的顺序可能会相反，具体取决于您使用的 Markdown 处理器。

#### 粗体和斜体的惯例用法

Markdown 应用程序在如何处理单词中间的下划线方面没有达成一致。为了兼容起见，请使用星号加粗并将单词中间斜体化以强调。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`This is really***very***important text.`|`This is really___very___important text.`|

## 引用

要创建引用块，请在段落前添加 a `>` 。

```
> Dorothy followed her through many of the beautiful rooms in her castle.
```

呈现的输出如下所示：

> Dorothy followed her through many of the beautiful rooms in her castle.  

#### 引用惯例用法

为了兼容，请在块引号前后放置空行。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`Try to put a blank line before...`<br><br>`> This is a blockquote`<br><br>`...and after a blockquote.`|`Without blank lines, this might not look right.`<br>`> This is a blockquote`<br>`Don't do this!`|

### 多个段落的引用块

块引号可以包含多个段落。在段落之间的空白行上添加 a `>` 。

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

呈现的输出如下所示：

> Dorothy followed her through many of the beautiful rooms in her castle.  
> 
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.  

### 嵌套引用块

引用块可以嵌套。在要嵌套的段落前面添加 a `> >` 。

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

呈现的输出如下所示：

> Dorothy followed her through many of the beautiful rooms in her castle.  
> 
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.  

### 带有其他元素的引用块

Blockquotes 可以包含其他 Markdown 格式的元素。并非所有元素都可以使用——您需要进行实验，看看哪些元素有效。

```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

呈现的输出如下所示：

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.

## 列表

您可以将项目组织到有序列表和无序列表中。

### 有序列表

要创建有序列表，请添加带有数字后跟句点的行项目。数字不必按数字顺序排列，但列表应从数字1 开始。

|Markdown|HTML|输出|
|---|---|---|
|`1. First item`<br>`2. Second item`<br>`3. Third item`<br>`4. Fourth item`|`<ol>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item</li>`<br>`  <li>Fourth item</li>`<br>`</ol>`|1. First item 第一项<br>2. Second item 第二项<br>3. Third item 第三项<br>4. Fourth item 第四项|
|`1. First item`<br>`1. Second item`<br>`1. Third item`<br>`1. Fourth item`|`<ol>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item</li>`<br>`  <li>Fourth item</li>`<br>`</ol>`|1. First item 第一项<br>2. Second item 第二项<br>3. Third item 第三项<br>4. Fourth item 第四项|
|`1. First item`<br>`8. Second item`<br>`3. Third item`<br>`5. Fourth item`|`<ol>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item</li>`<br>`  <li>Fourth item</li>`<br>`</ol>`|1. First item 第一项<br>2. Second item 第二项<br>3. Third item 第三项<br>4. Fourth item 第四项|
|`1. First item`<br>`2. Second item`<br>`3. Third item`<br>`    1. Indented item`<br>`    2. Indented item`<br>`4. Fourth item`|`<ol>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item`<br>`    <ol>`<br>`      <li>Indented item</li>`<br>`      <li>Indented item</li>`<br>`    </ol>`<br>`  </li>`<br>`  <li>Fourth item</li>`<br>`</ol>`|1. First item 第一项<br>2. Second item 第二项<br>3. Third item  第三项<br>&nbsp;&nbsp;&nbsp;&nbsp; 1. Indented item 缩进项<br>&nbsp;&nbsp;&nbsp;&nbsp; 2. Indented item 缩进项<br>4. Fourth item 第四项|

#### 有序列表惯例用法

CommonMark 和其他一些轻量级标记语言允许您使用括号 （ `)` ） 作为分隔符（例如， `1) First item` ），但并非所有 Markdown 应用程序都支持此功能，因此从兼容性的角度来看，它不是一个好的选择。为兼容起见，仅限使用期限。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`1. First item`<br>`2. Second item`|`1) First item`<br>`2) Second item`|

### 无序列表

要创建无序列表，请在行项前添加短划线 （ `-` ）、星号 （ `*` ） 或加号 （ `+` ）。缩进一个或多个项目以创建嵌套列表。

|Markdown|HTML|输出|
|---|---|---|
|`- First item`<br>`- Second item`<br>`- Third item`<br>`- Fourth item`|`<ul>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item</li>`<br>`  <li>Fourth item</li>`<br>`</ul>`|- First item 第一项<br>- Second item 第二项<br>- Third item 第三项<br>- Fourth item 第四项|
|`* First item`<br>`* Second item`<br>`* Third item`<br>`* Fourth item`|`<ul>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item</li>`<br>`  <li>Fourth item</li>`<br>`</ul>`|- First item 第一项<br>- Second item 第二项<br>- Third item 第三项<br>- Fourth item 第四项|
|`+ First item`<br>`+ Second item`<br>`+ Third item`<br>`+ Fourth item`|`<ul>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item</li>`<br>`  <li>Fourth item</li>`<br>`</ul>`|- First item 第一项<br>- Second item 第二项<br>- Third item 第三项<br>- Fourth item 第四项|
|`- First item`<br>`- Second item`<br>`- Third item`<br>`    - Indented item`<br>`    - Indented item`<br>`- Fourth item`|`<ul>`<br>`  <li>First item</li>`<br>`  <li>Second item</li>`<br>`  <li>Third item`<br>`    <ul>`<br>`      <li>Indented item</li>`<br>`      <li>Indented item</li>`<br>`    </ul>`<br>`  </li>`<br>`  <li>Fourth item</li>`<br>`</ul>`|- First item 第一项<br>- Second item 第二项<br>- Third item  第三项<br>&nbsp;&nbsp;&nbsp;&nbsp; - Indented item 缩进项<br>&nbsp;&nbsp;&nbsp;&nbsp; - Indented item 缩进项<br>- Fourth item 第四项|

#### 无序列表惯例用法

Markdown 应用程序对于如何处理同一列表中的不同分隔符没有达成一致。为了兼容，不要在同一列表中混合和匹配分隔符 - 选择一个并坚持使用。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`- First item`<br>`- Second item`<br>`- Third item`<br>`- Fourth item`|`+ First item`<br>`* Second item`<br>`- Third item`<br>`+ Fourth item`|

#### 使用数字开始无序列表项

如果需要以数字后跟句点开始无序列表项，则可以使用反斜杠 （ `\` ） 对句点进行[转义](#转义字符)。

|Markdown|HTML|输出|
|---|---|---|
|`- 1968\. A great year!`<br>`- I think 1969 was second best.`|`<ul>`<br>`  <li>1968. A great year!</li>`<br>`  <li>I think 1969 was second best.</li>`<br>`</ul>`|- 1968. A great year!  <br>- I think 1969 was second best.  <br>|

### 在列表中嵌套其他元素

若要在列表中添加另一个元素，同时保持列表的连续性，请将元素缩进四个空格或一个制表符，如以下示例所示。

> [!tip] 提示
> 
> 如果内容未按预期方式显示，请仔细检查是否已将列表中的元素缩进四个空格或一个制表符。

#### 段落

```
* This is the first list item.
* Here's the second list item.

    I need to add another paragraph below the second list item.

* And here's the third list item.
```

呈现的输出如下所示：

- This is the first list item.  
- Here’s the second list item.  

	 I need to add another paragraph below the second list item.  

- And here’s the third list item.  

#### 引用块

```
* This is the first list item.
* Here's the second list item.

    > A blockquote would look great below the second list item.

* And here's the third list item.
```

呈现的输出如下所示：

* This is the first list item.
* Here's the second list item.

    > A blockquote would look great below the second list item.

* And here's the third list item.

#### 代码块

代码块通常缩进四个空格或一个制表符。当它们位于列表中时，将它们缩进 8 个空格或 2 个制表符。

```
1. Open the file.
2. Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3. Update the title to match the name of your website.
```

呈现的输出如下所示：

1. Open the file.
2. Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3. Update the title to match the name of your website.

#### 图片

```
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

    ![Tux, the Linux mascot](/assets/images/tux.png)

3. Close the file.
```


呈现的输出如下所示：

1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

    ![Tux, the Linux mascot](https://mdg.imgix.net/assets/images/tux.png)

3. Close the file.

#### 列表

您可以将无序列表嵌套在有序列表中，反之亦然。

```
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
```

呈现的输出如下所示：

1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item

## 代码

要将单词或短语表示为代码，请将其括在反引号（`` ` ``）中。

|Markdown|HTML|输出|
|---|---|---|
|``At the command prompt, type `nano`.``|`At the command prompt, type <code>nano</code>.`|At the command prompt, type `nano`.|

### 转义反引号

如果要表示为代码的单词或短语包含一个或多个反引号，则可以通过将单词或短语括在双反引号（ ` `` `）中来转义它 。

|Markdown|HTML|输出|
|---|---|---|
|``` ``Use `code` in your Markdown file.`` ```|``<code>Use `code` in your Markdown file.</code>``|``Use `code` in your Markdown file.``|

### 代码块

要创建代码块，请将代码块的每一行至少缩进四个空格或一个制表符。

```
    <html>
      <head>
      </head>
    </html>
```

呈现的输出如下所示：

    <html>
      <head>
      </head>
    </html>

> [!note] 注意
> 
> 要创建不缩进行的代码块，请使用 [围栏式代码块](Markdown-extended-syntax#围栏式代码块).。


## 分割线

要创建水平线，请在一行上单独使用三个或更多星号 （ `***` ）、短划线 （ `---` ） 或下划线 （ `___` ）。

```
***

---

_________________
```

所有三个的渲染输出看起来相同：

---

#### 水平规则惯例用法

为了兼容，请在水平线前后放置空行。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`Try to put a blank line before...`<br><br>`---`<br><br>`...and after a horizontal rule.`|`Without blank lines, this would be a heading.`<br>`---`<br>`Don't do this!`|

## 链接


要创建链接，请将链接文本括在括号中（例如， `[Duck Duck Go]` ），然后立即在括号中加上 URL（例如， `(https://duckduckgo.com)` ）。

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
```

呈现的输出如下所示：

My favorite search engine is [Duck Duck Go](https://duckduckgo.com/).  

> [!note] 注意
>
> **Note:** To link to an element on the same page, see [linking to heading IDs](https://www.markdownguide.org/extended-syntax/#linking-to-heading-ids). To create a link that opens in a new tab or window, see the section on [link targets](https://www.markdownguide.org/hacks/#link-targets).  
> 
> 要链接到同一页面上的元素，请参阅链接到标题 ID。要创建在新标签页或窗口中打开的链接，请参阅有关链接目标的部分。

#### 链接惯例用法
  
Markdown 应用程序对于如何处理 URL 中间的空格没有达成一致。为了兼容，请尝试使用 `%20` URL 对任何空格进行 URL 编码。或者，如果你的 Markdown 应用程序支持 HTML](#html)，你可以使用 `a` HTML 标记。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`[link](https://www.example.com/my%20great%20page)`<br><br>`<a href="https://www.example.com/my great page">link</a>      `|`[link](https://www.example.com/my great page)   `|

URL 中间的括号也可能是有问题的。为了兼容，请尝试使用 URL 对左括号 （ `(` ） 和 `%28` 右括号 （ `)` ） 进行 `%29` URL 编码。或者，如果你的 Markdown 应用程序支持 [HTML](#html)，你可以使用 `a` HTML 标记。

|✅ 执行此操作|❌ 别这样|
|---|---|
|`[a novel](https://en.wikipedia.org/wiki/The_Milagro_Beanfield_War_%28novel%29)`<br><br>`<a href="https://en.wikipedia.org/wiki/The_Milagro_Beanfield_War_(novel)">a novel</a>      `|`[a novel](https://en.wikipedia.org/wiki/The_Milagro_Beanfield_War_(novel))`|


### 添加标题

您可以选择性地为链接添加标题。当用户将鼠标悬停在链接上时，这将显示为工具提示。要添加标题，请在 URL 后将其括在引号中。

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
```

呈现的输出如下所示：

My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

### URL 和电子邮件地址

要快速将 URL 或电子邮件地址转换为链接，请将其括在尖括号中。

```
<https://www.markdownguide.org>
<fake@example.com>
```

呈现的输出如下所示：

<https://www.markdownguide.org>
<fake@example.com>

### 格式化链接

要[强调](#强调)链接，请在括号和括号前后添加星号。若要将链接表示为[代码](#代码)，请在括号中添加反引号。

```
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
```

呈现的输出如下所示：

I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#代码).

### 引用样式链接

引用样式链接是一种特殊类型的链接，它使 URL 更易于在 Markdown 中显示和阅读。引用样式链接由两部分构成：与文本内联的部分，以及存储在文件中其他位置以保持文本易于阅读的部分。

#### 设置链接第一部分的格式

引用样式链接的第一部分使用两组括号进行格式设置。第一组括号括起来的文本应该显示为链接。第二组括号显示一个标签，用于指向您存储在文档中其他位置的链接。

虽然不是必需的，但您可以在第一组和第二组括号之间添加一个空格。第二组括号中的标签不区分大小写，可以包含字母、数字、空格或标点符号。

这意味着以下示例格式与链接的第一部分大致相同：

- `[hobbit-hole][1]`
- `[hobbit-hole] [1]`

#### 设置链接第二部分的格式
 
引用样式链接的第二部分使用以下属性进行格式设置：

1. 标签，用括号括起来，紧跟一个冒号和至少一个空格（例如， `[label]:` ）。
2. 链接的 URL，您可以选择将其括在尖括号中。
3. 链接的可选标题，可以用双引号、单引号或括号括起来。

这意味着以下示例格式对于链接的第二部分都大致相同：

- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)`

您可以将链接的第二部分放在 Markdown 文档中的任何位置。有些人将它们放在它们出现的段落之后，而另一些人则将它们放在文档的末尾（如尾注或脚注）。

#### 将各部分放在一起的示例

假设您将 URL 添加为段落的[标准 URL 链接](#链接)，它在 Markdown 中看起来像这样：

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.
```

尽管它可能指向有趣的附加信息，但显示的 URL 除了使其更难阅读之外，实际上并没有对现有的原始文本增加太多。要解决此问题，您可以改为设置URL的格式：

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole][1], and that means comfort.

[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
```

在上述两种情况下，呈现的输出将是相同的：

> In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.  

链接的 HTML 为：

```
<a href="https://en.wikipedia.org/wiki/Hobbit#Lifestyle" title="Hobbit lifestyles">hobbit-hole</a>
```

## 图片

要添加图片，请添加感叹号 （ `!` ），后跟括号中的替代文本，并在括号中添加图片资产的路径或 URL。您可以选择在路径或 URL 后添加引号中的标题。

```
![The San Juan Mountains are beautiful!](/assets/images/san-juan-mountains.jpg "San Juan Mountains")
```

呈现的输出如下所示：

![The San Juan Mountains are beautiful!](https://mdg.imgix.net/assets/images/san-juan-mountains.jpg "San Juan Mountains")

> [!note] 注意
>
> **Note:** To resize an image, see the section on [image size](https://www.markdownguide.org/hacks/#image-size). To add a caption, see the section on [image captions](https://www.markdownguide.org/hacks/#image-captions).  
>
>要调整图片大小，请参阅有关图片大小的部分。要添加标题，请参阅有关图片标题的部分。

### 链接图片

To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parentheses.  
若要向图片添加链接，请将图片的 Markdown 括在括号中，然后将链接添加到括号中。

```
[![An old rock in the desert](/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)
```

The rendered output looks like this:  
呈现的输出如下所示：

[![An old rock in the desert](https://mdg.imgix.net/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

## 转义字符

To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash (`\`) in front of the character.  
若要显示本来将用于设置 Markdown 文档中文本格式的文本字符，请在字符前面添加反斜杠 （ `\` ）。

```
\* Without the backslash, this would be a bullet in an unordered list.
```

The rendered output looks like this:  
呈现的输出如下所示：

* Without the backslash, this would be a bullet in an unordered list.  
* 如果没有反斜杠，这将是无序列表中的一个项目符号。

### 你可以转义的字符

You can use a backslash to escape the following characters.  
您可以使用反斜杠对以下字符进行转义。

|Character 字符|Name 名字|
|---|---|
|\|backslash 反斜線|
|`|backtick 反引号（另请参阅在代码中转义反引号）|
|*|asterisk 星号|
|_|underscore 强调|
|{ }|curly braces 大括号|
|[ ]|brackets 括弧|
|< >|angle brackets 尖括号|
|( )|parentheses 括弧|
|#|pound sign 井号|
|+|plus sign 加号|
|-|minus sign (hyphen) 减号（连字符）|
|.|dot 点|
|!|exclamation mark 感叹号|
|\||pipe (see also [escaping pipe in tables](https://www.markdownguide.org/extended-syntax/#escaping-pipe-characters-in-tables))  <br>管道（另请参阅表中的转义管道）|

## HTML

许多 Markdown 应用程序允许您在 Markdown 格式的文本中使用 HTML 标签。如果您更喜欢某些 HTML 标签而不是 Markdown 语法，这将很有帮助。例如，有些人发现对图片使用 HTML 标签更容易。当您需要更改元素的属性时，例如指定[文本的颜色](https://www.markdownguide.org/hacks/#color)或更改图片的宽度，使用 HTML 也很有帮助。

要使用 HTML，请将标记放在 Markdown 格式文件的文本中。

```
This **word** is bold. This <em>word</em> is italic.
```

呈现的输出如下所示：

This **word** is bold. This _word_ is italic.  

#### HTML 惯例用法

出于安全原因，并非所有 Markdown 应用程序都支持 Markdown 文档中的 HTML。如有疑问，请查看 Markdown 应用程序的文档。某些应用程序仅支持 HTML 标记的子集。

使用空行将块级 HTML 元素（如 `<div>` 、 `<table>` 、 `<pre>` ）与 `<p>` 周围内容分开。尽量不要使用制表符或空格缩进标签，这可能会干扰格式设置。

不能在块级 HTML 标记中使用 Markdown 语法。例如， `<p>italic and **bold**</p>` 将不起作用。