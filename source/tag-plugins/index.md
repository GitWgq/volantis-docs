---
layout: page
group: docs
title: Tag Plugins「内建标签」
cover: false
meta:
  header: [title, author, updated]
mathjax: true
links:
  repo: https://github.com/xaoxuu/hexo-theme-volantis
  bug: https://github.com/xaoxuu/hexo-theme-volantis/issues/new?assignees=&labels=BUG&template=bug-report.md
  doubt: https://github.com/xaoxuu/hexo-theme-volantis/issues/new?labels=疑问&template=question-report.md
  idea: https://github.com/xaoxuu/hexo-theme-volantis/issues/new?assignees=&labels=建议&template=feature-request.md
---


主题支持<b><red>丰</red><yellow>富</yellow><green>多</green><blue>彩</blue></b>的标签。

## 彩色文字 <sup class='blue'>^1.5.2</sup>

在一段话中方便插入各种颜色的标签，包括：<red>红色</red>、<yellow>黄色</yellow>、<green>绿色</green>、<cyan>青色</cyan>、<blue>蓝色</blue>、<gray>灰色</gray>。

```md 写法如下：
在一段话中方便插入各种颜色的标签，包括：<red>红色</red>、<yellow>黄色</yellow>、<green>绿色</green>、<cyan>青色</cyan>、<blue>蓝色</blue>、<gray>灰色</gray>。
```

## 超大文字 <sup class='blue'>^1.5.2</sup>

文档「开始」页面中的标题部分就是超大文字。目前支持的尺寸有：`large`、`huge`。

{% raw %}
<details>
<summary>
示例效果
</summary>
{% endraw %}

<center>
<p class='large' style='color:#666'>Volantis</p>
<b style='font-size:.9em;color:#666'>A Wonderful Theme for Hexo 4.2+</b>
</center>

{% raw %}</details>{% endraw %}

```md 写法如下：
<center>
<p class='large' style='color:#666'>Volantis</p>
<b style='font-size:.9em;color:#666'>A Wonderful Theme for Hexo 4.2+</b>
</center>
```

## 插入简单按钮 <sup class='blue'>^1.6</sup>

目前共支持四种尺寸的按钮。

{% raw %}
<details>
<summary>
示例效果
</summary>
{% endraw %}

在一句话中插入一个不太重要的 <btn class='small'>[小按钮](/)</btn> 。
在一句话中插入一个正常尺寸的 <btn>[按钮](/)</btn> 。
而这个更像是常规的按钮：
<btn class='regular'>[常规按钮](/)</btn>

这个适合用作首页：
<center>

<btn class='large'>[<i class='fas fa-download'></i> 开始使用](/wiki/volantis/getting-started/)</btn>

</center>

{% raw %}</details>{% endraw %}


```md 写法如下：
在一句话中插入一个不太重要的 <btn class='small'>[小按钮](/)</btn> 。
在一句话中插入一个正常尺寸的 <btn>[按钮](/)</btn> 。
而这个更像是常规的按钮：
<btn class='regular'>[常规按钮](/)</btn>

这个适合用作首页：
<center><btn class='large'>[<i class='fas fa-download'></i> 开始使用](/wiki/volantis/getting-started/)</btn></center>
```

::: danger

由于未知原因，上例中如果 `<center></center>` 与其中的 `<btn>[按钮](/)</btn>` 之间没有空行，hexo不会解析成按钮。

:::

## 插入含有丰富内容的按钮 <sup class='blue'>^1.6</sup>

如果需要显示类似「团队成员」之类的一组含有头像的链接，建议使用这种方式：

{% raw %}
<div class='links-wrapper circle'>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
</div>
{% endraw %}

```md 写法如下：
{% raw %}
<div class='links-wrapper circle'>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
<a href='https://github.com/xaoxuu'><img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png'>xaoxuu</a>
</div>
{% endraw %}
```

```md 提示：
{% raw %} 和 {% endraw %} 之间的内容是不解析的，只能写HTML标签。
```

### 图片样式

- 方形（`<div class='links-wrapper'>`）。
- 圆角矩形（`<div class='links-wrapper rounded'>`），适合app图标。
- 圆形（`<div class='links-wrapper circle'>`），适合头像。

### 文字样式

- 标题（`<p class='title'>标题</p>`）。
- 内容（`<p>内容描述</p>`）。

### 布局方式

- 占容器50%宽的按钮（`<div class='links-wrapper wide'>`）
- 自动宽度（`<div class='links-wrapper auto'>`）,适合视野内只有一两个的情况，多了显得乱。
- 填充布局（`<div class='links-wrapper fill'>`），适合文字量大的情况。


### 再举一个例子

圆角矩形 + 标题 + 描述 + 填充布局

{% raw %}
<div class='links-wrapper rounded fill'>
<a href='https://xaoxuu.com/wiki/heartmate/'>
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/heartmate/icon.png'>
  <p class='title'>一个简单易用的掌上心率计</p>
  <p style='text-align:left'>专为那些没有智能手环或手表却需要测量心率的用户而设计，可以方便快捷的测量和记录心率。</p>
  <p style='text-align:left'>使用Heart Mate心率助手，你可以在没有智能手环等心率监测设备的情况下随时检测并记录自己的心率。 通过设置tag标签，快速记录当前状态，如饭后、运动后等，方便以后检索具有同样标签的心率数据，从而分析这些情景下的心率数据，发现健康问题。</p>
</a>
<a href='https://xaoxuu.com/wiki/heartmate/'>
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/heartmate/icon_lite.png'>
  <p class='title'>一个简单易用的掌上心率计</p>
  <p style='text-align:left'>专为那些没有智能手环或手表却需要测量心率的用户而设计，可以方便快捷的测量和记录心率。</p>
  <p style='text-align:left'>「免费版」仅仅是个性化定制功能锁定，核心功能完全不受限制，并且没有任何广告。</p>
</a>
<a href='https://xaoxuu.com/wiki/prohud/'>
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/prohud/icon.png'>
  <p class='title'>ProHUD</p>
  <p>Toast + Alert + ActionSheet</p>
  <p style='text-align:left'>用简便的方法拿到已发布的实例，避免重复发布实例。可对已发布的实例进行数据更新。可对所有实例设置监听事件。对多实例并存堆叠的极端情况做了优化。完全可定制并易于扩展。</p>
</a>
</div>
{% endraw %}


{% raw %}
<details>
<summary>
上例写法如下
</summary>
{% endraw %}

```html
{% raw %}
<div class='links-wrapper rounded fill'>
<a href='https://xaoxuu.com/wiki/heartmate/'>
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/heartmate/icon.png'>
  <p class='title'>一个简单易用的掌上心率计</p>
  <p style='text-align:left'>专为那些没有智能手环或手表却需要测量心率的用户而设计，可以方便快捷的测量和记录心率。</p>
  <p style='text-align:left'>使用Heart Mate心率助手，你可以在没有智能手环等心率监测设备的情况下随时检测并记录自己的心率。 通过设置tag标签，快速记录当前状态，如饭后、运动后等，方便以后检索具有同样标签的心率数据，从而分析这些情景下的心率数据，发现健康问题。</p>
</a>
<a href='https://xaoxuu.com/wiki/heartmate/'>
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/heartmate/icon_lite.png'>
  <p class='title'>一个简单易用的掌上心率计</p>
  <p style='text-align:left'>专为那些没有智能手环或手表却需要测量心率的用户而设计，可以方便快捷的测量和记录心率。</p>
  <p style='text-align:left'>「免费版」仅仅是个性化定制功能锁定，核心功能完全不受限制，并且没有任何广告。</p>
</a>
<a href='https://xaoxuu.com/wiki/prohud/'>
  <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/proj/prohud/icon.png'>
  <p class='title'>ProHUD</p>
  <p>Toast + Alert + ActionSheet</p>
  <p style='text-align:left'>用简便的方法拿到已发布的实例，避免重复发布实例。可对已发布的实例进行数据更新。可对所有实例设置监听事件。对多实例并存堆叠的极端情况做了优化。完全可定制并易于扩展。</p>
</a>
</div>
{% endraw %}
```

{% raw %}</details>{% endraw %}

## 图片放大

1. 在主题配置文件中开启插件。

```yaml 主题配置文件
plugins:
  fancybox:
    css: '//cdn.jsdelivr.net/npm/@fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css'
    js: '//cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js'
```

2. 将需要放大预览的图片用 `<fancybox></fancybox>` 包含起来。

```md 写法如下：
例如这个图是不能点开的：
![](https://img.vim-cn.com/52/a54815c02ce232f11f54b2c547c1337828833c.png)
而这个图是可以点开的：
<fancybox>
<img src='https://img.vim-cn.com/52/a54815c02ce232f11f54b2c547c1337828833c.png'>
</fancybox>
```

{% raw %}
<details>
<summary>
示例效果
</summary>
{% endraw %}

例如这个图是不能点开的：
![](https://img.vim-cn.com/52/a54815c02ce232f11f54b2c547c1337828833c.png)
而这个图是可以点开的：
<fancybox>
<img src='https://img.vim-cn.com/52/a54815c02ce232f11f54b2c547c1337828833c.png'>
</fancybox>

{% raw %}</details>{% endraw %}

```md 「<b><red>注意</red></b>」这样写是无效的：
<fancybox>
![](https://img.vim-cn.com/52/a54815c02ce232f11f54b2c547c1337828833c.png)
</fancybox>
```

如需一行显示多图，将多个图片同时放在一对 `<fancybox></fancybox>` 中即可：

```html
<fancybox>
<img src='https://i.loli.net/2019/08/20/sgultOmRLXrwfA3.png'>&nbsp;
<img src='https://i.loli.net/2019/08/20/a2mCq871PwfbZEG.png'>&nbsp;
<img src='https://i.loli.net/2019/08/20/Zdz2cTphOlu3XKf.png'>&nbsp;
<img src='https://i.loli.net/2019/08/20/87UdSGaMuevV1iF.png'>&nbsp;
<img src='https://i.loli.net/2019/08/20/HEusSLBgG3XC1nN.png'>
</fancybox>
```

## 表格滚动 <sup class='blue'>^1.6</sup>

一般来说，表格默认会横向铺满，格子内文字过多会自动换行。但是当列数比较多时，每一列都很窄，推荐使用支持滚动的表格样式，用一对 `<overflow></overflow>` 把表格包起来。

```md 格式为：
<overflow>

md表格内容

</overflow>
```

{% raw %}
<details>
<summary>
示例
</summary>
{% endraw %}

<overflow>

| 类别     | 排序方法 | 平均时间复杂度       | 最优时间复杂度       | 最差时间复杂度       | 空间复杂度                  | 稳定性 | 复杂性 |
| :-------- | :-------- | :-------------------- | :-------------------- | :-------------------- | :--------------------------- | :------ | :------ |
| 插入排序 | 直接插入 | O(n<sup>2</sup>)     | O(n)                 | O(n<sup>2</sup>)     | O(1)                        | 稳定   | 简单   |
| 插入排序 | 希尔排序 | O(n<sup>1.3</sup>)   | O(n)                 | O(n<sup>2</sup>)     | O(1)                        | 不稳定 | 复杂   |
| 选择排序 | 直接选择 | O(n<sup>2</sup>)     | O(n<sup>2</sup>)     | O(n<sup>2</sup>)     | O(1)                        | 不稳定 | 简单   |
| 选择排序 | 堆排序   | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(1)                        | 不稳定 | 复杂   |
| 交换排序 | 冒泡排序 | O(n<sup>2</sup>)     | O(n)                 | O(n<sup>2</sup>)     | O(1)                        | 稳定   | 简单   |
| 交换排序 | 快速排序 | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(n<sup>2</sup>)     | O(nlog<sub>2</sub>n)~O(n) | 不稳定 | 复杂   |
|          | 归并排序 | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(n)                        | 稳定   | 复杂   |
|          | 基数排序 | O(d(r+n))            | O(d(r+n))            | O(d(r+n))            | O(rd+n)                     | 稳定   | 复杂   |

</overflow>

```md 写法如下：
<overflow>

| 类别     | 排序方法 | 平均时间复杂度       | 最优时间复杂度       | 最差时间复杂度       | 空间复杂度                  | 稳定性 | 复杂性 |
| :-------- | :-------- | :-------------------- | :-------------------- | :-------------------- | :--------------------------- | :------ | :------ |
| 插入排序 | 直接插入 | O(n<sup>2</sup>)     | O(n)                 | O(n<sup>2</sup>)     | O(1)                        | 稳定   | 简单   |
| 插入排序 | 希尔排序 | O(n<sup>1.3</sup>)   | O(n)                 | O(n<sup>2</sup>)     | O(1)                        | 不稳定 | 复杂   |
| 选择排序 | 直接选择 | O(n<sup>2</sup>)     | O(n<sup>2</sup>)     | O(n<sup>2</sup>)     | O(1)                        | 不稳定 | 简单   |
| 选择排序 | 堆排序   | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(1)                        | 不稳定 | 复杂   |
| 交换排序 | 冒泡排序 | O(n<sup>2</sup>)     | O(n)                 | O(n<sup>2</sup>)     | O(1)                        | 稳定   | 简单   |
| 交换排序 | 快速排序 | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(n<sup>2</sup>)     | O(nlog<sub>2</sub>n)~O(n) | 不稳定 | 复杂   |
|          | 归并排序 | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(n)                        | 稳定   | 复杂   |
|          | 基数排序 | O(d(r+n))            | O(d(r+n))            | O(d(r+n))            | O(rd+n)                     | 稳定   | 复杂   |

</overflow>
```

{% raw %}</details>{% endraw %}

## 折叠区域 <sup class='blue'>^1.5.2</sup>

{% raw %}
<details>
<summary>
One More Thing 👇
</summary>
{% endraw %}

懒加载占位图如果喜欢请拿去：<btn>[图片地址](https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/placeholder/d570170f4f12e1ee829ca0e85a7dffeb77343a.svg)</btn>

{% raw %}</details>{% endraw %}

```md 写法如下：
{% raw %}
<details>
<summary>
One More Thing 👇
</summary>
{% endraw %}

懒加载占位图如果喜欢请拿去：<btn>[图片地址](https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/placeholder/d570170f4f12e1ee829ca0e85a7dffeb77343a.svg)</btn>

{% raw %}</details>{% endraw %}
```


## 渲染公式（MathJax）

默认是不渲染的，如果文章内有公式，需要在 `front-matter` 中设置开启。

```md 示例：
---
title: 渲染公式（MathJax）
date: 2020-02-23
mathjax: true # false: 不渲染, true: 渲染, internal: 只在文章内部渲染，文章列表中不渲染
---

$$
\begin{equation}
\sum_{i=0}^n F_i \cdot \phi (H, p_i) - \sum_{i=1}^n a_i \cdot ( \tilde{x_i}, \tilde{y_i}) + b_i \cdot ( \tilde{x_i}^2 , \tilde{y_i}^2 )
\end{equation}
$$
$$
\begin{equation}
\beta^*(D) = \mathop{argmin} \limits_{\beta} \lambda {||\beta||}^2 + \sum_{i=1}^n max(0, 1 - y_i f_{\beta}(x_i))
\end{equation}
$$
```


{% raw %}
<details>
<summary>
示例效果
</summary>
{% endraw %}

$$
\begin{equation}
\sum_{i=0}^n F_i \cdot \phi (H, p_i) - \sum_{i=1}^n a_i \cdot ( \tilde{x_i}, \tilde{y_i}) + b_i \cdot ( \tilde{x_i}^2 , \tilde{y_i}^2 )
\end{equation}
$$
$$
\begin{equation}
\beta^*(D) = \mathop{argmin} \limits_{\beta} \lambda {||\beta||}^2 + \sum_{i=1}^n max(0, 1 - y_i f_{\beta}(x_i))
\end{equation}
$$

{% raw %}</details>{% endraw %}


> 如果公式仍无法正确渲染可以阅读 [@MicDZ](https://www.micdz.cn) 的这篇文章：[《在material-x上使用KaTeX》](https://www.micdz.cn/article/katex-on-volantis/)。


## Hexo原生支持的标签

### 引用块

引用书上的句子

{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}

引用网络上的文章

{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}

### 代码块

```md 格式：
{% codeblock [title] [lang:language] [url] [link text] [additional options] %}
code snippet
{% endcodeblock %}
```

#### 指定语言

{% codeblock lang:objc %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
{% endcodeblock %}

```md 写法如下：
{% codeblock lang:objc %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
{% endcodeblock %}
```

#### 附加说明

{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}

```md 写法如下：
{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}
```

#### 行标、高亮

{% codeblock lang:python line_number:true mark:3,5,8 %}
n=eval(input())
if n==0:
   print("Hello World")
elif n>0:
   print("He\nll\no \nWo\nrl\nd")
else:
   for c in "Hello World":
   print(c)
{% endcodeblock %}

```md 写法如下：
{% codeblock lang:python line_number:true mark:3,5,8 %}
n=eval(input())
if n==0:
   print("Hello World")
elif n>0:
   print("He\nll\no \nWo\nrl\nd")
else:
   for c in "Hello World":
   print(c)
{% endcodeblock %}
```

### Pull Quote
在文章中插入 `Pull quote`。
```md 写法如下：
{% pullquote [class] %}
content
{% endpullquote %}
```

### jsFiddle
在文章中嵌入 `jsFiddle`。
```md 写法如下：
{% jsfiddle shorttag [tabs] [skin] [width] [height] %}
```

### Gist
在文章中嵌入 `Gist`，<red>注意</red>：在国内无法加载。
```md 写法如下：
{% gist gist_id [filename] %}
```

### iframe
在文章中插入 `iframe`。
```md 写法如下：
{% iframe url [width] [height] %}
```

### Image
在文章中插入指定大小的图片。
```md 写法如下：
{% img [class names] /path/to/image [width] [height] '"title text" "alt text"' %}
```

### Link
在文章中插入链接，并自动给外部链接添加 `target="_blank"` 属性。
```md 写法如下：
{% link text url [external] [title] %}
```

### Include Code
插入 `source/downloads/code` 文件夹内的代码文件。`source/downloads/code` 不是固定的，取决于你在配置文件中 `code_dir` 的配置。
```md 写法如下：
{% include_code [title] [lang:language] [from:line] [to:line] path/to/file %}
```

{% raw %}
<details>
<summary>
示例
</summary>
{% endraw %}

嵌入 `test.js` 文件全文
```md
{% include_code lang:javascript test.js %}
```
只嵌入第 3 行
```md
{% include_code lang:javascript from:3 to:3 test.js %}
```
嵌入第 5 行至第 8 行
```md
{% include_code lang:javascript from:5 to:8 test.js %}
```
嵌入第 5 行至文件结束
```md
{% include_code lang:javascript from:5 test.js %}
```
嵌入第 1 行至第 8 行
```md
{% include_code lang:javascript to:8 test.js %}
```

{% raw %}</details>{% endraw %}

### 引用文章

引用其他文章的链接。

```md
{% post_path filename %}
{% post_link filename [title] [escape] %}
```

{% raw %}
<details>
<summary>
示例
</summary>
{% endraw %}

<br>

引用这篇文章：{% post_link 2020-02-22 %}

```md 写法如下：
引用这篇文章：{% post_link 2020-02-22 %}
```
{% raw %}</details>{% endraw %}

### 文章摘要和截断

在文章中使用 `<!-- more -->`，那么 `<!-- more -->` 之前的文字将会被视为摘要。首页中将只出现这部分文字，同时这部分文字也会出现在正文之中。


> 更多请见Hexo官方文档：[#标签插件](https://hexo.io/zh-cn/docs/tag-plugins)
