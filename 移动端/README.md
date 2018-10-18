## viewport快速学习指南

### viewport简介

- 没错，就是viewport特性，一个移动专属的Meta值，用于定义视口的各种行为。

- 该特性最先由Apple引入，用于解决移动端的页面展示问题，后续被越来越多的厂商跟进。

- 举个简单的例子来讲为什么会需要它：
  
> 我们知道用户大规模使用手机等移动设备来进行网页浏览器，其实得益于智能手持设备的兴起，也就是近几年的事。（还记得不久前的几年，满大街都还是诺基亚的天下么？）这时有一个很现实的问题摆在了厂商面前，用户并不能很好地通过手机等设备访问网页，因为屏幕太小。

#### layout viewport

- Apple也发现了这个问题，并且适时的出现，它提出了一个方案用来解决这个问题。在iOS Safari中定义了一个viewport meta标签，用来创建一个虚拟的布局视口（layout viewport），而这个视口的分辨率接近于PC显示器，Apple将其定义为**980px**（其他厂商各有不同①）。

> ①的描述大致如下，数值不一定持续准确，厂商可能更改，但这个绝对值其实并非特别重要： iOS, Android基本都是: 980px BlackBerry: 1024px

对于visual viewport，开发者一般只需要知道它的存在和概念就行，因为无法对它进行任何设置或者修改。很明显，visual viewport的尺寸不会是一个固定的值，甚至每款设备都可能不同。大致列几种常见设备的visual viewport尺寸：

- iPhone4~iPhone5S: 320*480px
- iPhone6~iPhone6S: 375*627px
- iPhone6 Plus~iPhone6S Plus: 414*736px

以iPhone4S为例，会在其320px②的visual viewport上，创建一个宽980px的layout viewport，于是用户可以在visual viewport中拖动或者缩放网页，来获得良好的浏览效果；布局视口用来配合CSS渲染布局，当我们定义一个容器的宽度为100%时，这个容器的实际宽度是980px而不是320px，通过这种方式大部分网页就能以缩放的形式正常显示在手机屏幕上了。

> ②的描述大致如下： 早期移动前端开发工程师常能见到宽640px的设计稿，原因就是UI工程师以物理屏幕宽度为320px的iPhone4-iPhone5S作为参照设计； 当然，现在你还可能会见到750px和1242px尺寸的设计稿，原因当然是iPhone6的出现

### viewport特性

- 通常情况下，viewport有以下6种设置。当然厂商可能会增加一些特定的设置，比如iOS Safari7.1增加了一种在网页加载时隐藏地址栏与导航栏的设置：minimal-ui，不过随后又将之移除了。

| Name         | Value        |  描述        |
| -------------------------   | ----------  | :----------:  |
| width   | 正整数或device-width|   定义视口的宽度，单位为像素   |
| height   | 正整数或device-width |   定义视口的高度，单位为像素   |
| initial-scale  | [0.0-10.0] |   定义初始缩放值   |
| minimum-scale  | [0.0-10.0] |   定义缩小最小比例，它必须小于或等于maximum-scale设置 |
| maximum-scale  | [0.0-10.0]css3 |   定义放大最大比例，它必须大于或等于minimum-scale设置  |
| user-scalable    | yes/no |   定义是否允许用户手动缩放页面，默认值yes |

### width

width被用来定义layout viewport的宽度，如果不指定该属性（或者移除viewport meta标签），则layout viewport宽度为厂商默认值。如：iPhone为980px；

* 举个例子：
  ```html
  <meta name="viewport" content="width=device-width" />
  ```
> 此时的layout viewport将成为ideal viewport，因为layout viewport宽度与设备视觉视口宽度一致了。除了width之外，还有一个属性定义也能实现ideal viewport，那就是initial-scale。

### height
与width类似，但实际上却不常用，因为没有太多的use case。

### initial-scale
如果想页面默认以某个比例放大或者缩小然后呈现给用户，那么可以通过定义initial-scale来完成。

> initial-scale用于指定页面的初始缩放比例，假定你这样定义：

```html
<meta name="viewport" content="initial-scale=2" />
```
那么用户将会看到2倍大小的页面内容。

在说width的时候，我们说到initial-scale也能实现ideal viewport，是的，你只需要这样做，也可以得到完美视口：

```html
<meta name="viewport" content="initial-scale=1" />
```

### maximum-scale
在移动端，你可能会考虑用户浏览不便，然后给予用户放大页面的权利，但同时又希望是在一定范围内的放大，这时就可以使用maximum-scale来进行约束。

- maximum-scale用于指定用户能够放大的比例。

- 举个例子来讲：

```html
<meta name="viewport" content="initial-scale=1,maximum-scale=5" />
```

假设页面的默认缩放值initial-scale是1，那么用户最终能够将页面放大到这个初始页面大小的5倍。

### minimum-scale
类似maximum-scale的描述，不过minimum-scale是用来指定页面缩小比例的。

通常情况下，为了有更好地体验，不会定义该属性的值比1更小，因为那样页面将变得难以阅读。

### user-scalable
如果你不想页面被放大或者缩小，通过定义user-scalable来约束用户是否可以通过手势对页面进行缩放即可。

该属性的默认值为yes，即可被缩放（如果使用默认值，该属性可以不定义）；当然，如果你的应用不打算让用户拥有缩放权限，可以将该值设置为no。

- 使用方法如下：

```html
<meta name="viewport" content="user-scalable=no" />
```

[项目实战- 移动端](https://struggle-wjf.gitee.io/shop_mobile/)

默认宽度375px，iPhone6