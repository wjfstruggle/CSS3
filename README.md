<a name="zore"></a>
# CSS3

css和css3基础知识点大全

- [什么是css](#什么是css)
- [css引入](#css引入)
- [CSS的选择符](#CSS的选择符)
- [元素的定位](#元素的定位)
- [文本](#文本)
- [边框](#边框)

<a name="什么是css"></a>
### 什么是css
> css层叠样式表，CSS3知识CSS2的升级版本，在2的基础上增加了好多新的特性
> 前缀        浏览器
> - [-webkit]   chrome和safari
> - [-moz]      firefox
> - [-ms]   	IE
> - [-O]   		Opera

### CSS能做什么？

> 1、CSS把很多以前需要使用图片和脚本来实现的效果、甚至动画效果，只需要短短几行代码就能搞定。比如圆角，图片边框，文字阴影和盒阴影，过渡、动画等。

> CSS简化了前端开发工作人员的设计过程，更灵活的页面布局，更快的页面加载速度。

> 可以将站点上所有的网页风格都使用一个CSS文件进行控制，只要修改这个CSS文件中相应的代码，那么整个站点的所有页面都会随之发生变动。

> CSS可以支持多种设备,比如手机,PDA,打印机,电视机,游戏机等。

> 目的：将表现与结构分离。

<a name="css引入"></a>
### css的引入：

**3中引入方式**

1、行内引入

 指的是将css样式编码直接编写在HTML标签的style属性中 **注意这种方式的引入CSS，是不需要写选择器的。
**
		
		例：
		
			<body style="background-color:#ccccc;">
		
			<h1 style="font-size:12px; color:#ff0000;">这是一个标题</h1>


2. 页内引用	

页内引用作为页面中的一个单独部分，由```<style></style>```标签定位在```<head></head>```之中。

	例：
			<style type="text/css">
				div {
					color: blue;
					font-size: 16px;
				}
			</style>

3、外部引入
	
外部样式表是CSS应用中最好的一种形式，它将CSS样式代码单独放在一个外部文件中，再由网页进行调用。
		
		如：	
		style.css	:
	
		body {
		       background-color:#cccccc;
		}
	
		<link rel="stylesheet" type="text/css" href="style.css" />

**优先级比较**

- 优先级依次是：就近原则
- !important > 行内 > 页内 > 页外
- !important要慎用，因为优先级过高
- 选择器的权值累加也会影响优先级

<a name="CSS的选择符"></a>

### CSS的选择符:

大致分为：


- [x] 通配选择符
- [x] 元素选择符
- [x] 群组选择符
- [x] 关系选择符
- [x] id 及 class 选择符
- [x] 伪类选择符（部分扩展学习）
- [x] 属性选择符（扩展学习）
- [x] 伪对象选择符（扩展学习）

------------------------------------------------
- [x] 通配选择符
- 1.通配选择符 *

	*号表示所有的对象

	所谓通配选择符，就是指可以使用模糊指定的方式来对对象进行选择，指定样式。

	例：

	*{
	  color:blue;
	  margin:0;
	  padding:0;
	}

-----------------------------------------------

- [x] 元素(tagname)选择符

- 2.元素选择符
	
所谓元素选择符，指以网页中已有的标签名作为名称的选择符。

	例：
	
		body {}

		h1 {}

		p {}


-----------------------------------------------

- [x] 群组选择符
- 除了可以对单个标签进行样式指定外，还可以对一组标签进行相同的样式定义。
  
	例：

		h1,h2, h3, p {
		   font-size:12px;
		   font-family:arial;
		}

	使用逗号对选择符进行分隔。对页面中需要使用相同样式的地方，只需写一次样式

-----------------------------------------------

- [x] 关系选择符
- 关系选择符可分为：
> E F 包含选择符 选择所有被E包含的F元素

> E > F 子选择器 选择所有作为E元素的子元素F

> E + F 相邻选择符 选择紧贴所有作为E元素之后F元素

> E ~ F 兄弟选择器（CSS3） 选择所有作为E元素的兄弟元素F

- 事列：关系选择符.html

```
	/*包含选择符所有a下的为红色*/
			.seon1 a {
				color: red; 
			}
			/*seon2变为黄色，相邻的同级元素*/
			.seon1+div {
				background: yellow;
			}
			/*第一个a显示绿色，子代选择符*/
			.seon1 > a {
				color: green;
			}
			/*兄弟选择符，Seon的同级兄弟显示绿色*/
			.seon1 ~ div {
				background: green;
			}
		</style>
		<div class="fader">
			<div class="seon1">
				<a href="">html</a>
				<div class="garndson">
					<a href="">css</a>
				</div>
			</div>
			<div class="son2">son2</div>
			<div class="son3">son3</div>
		</div>
		
事列2：
		
		<style type="text/css">
			/*子代选择器*/
			
			div > a {
				background: red;
			}
			
			div > span > a {
				background: #67B374;
			}
			
			p:first-of-type {
				background: #0000FF;
			}
			/*相邻选择器，选择紧贴在E元素之后F元素*/
			p+ p {
				background: #808080;
			}
			.demo_1 {}
			/*选择E元素所有兄弟元素F。*/
			li ~ li {
				color: red;
			}
			<body>
		<div>
			<a>背景色是#E61061</a>
			<span>
				<a>背景色是#67B374</a>
        	</span>
		</div>
		<p class="first">背景色是#0000FF</p>
		<p>背景色是#808080</p>
		<p>背景色是#808080</p>
		
		
		
		<ul class="demo_1">
			<li>我是儿子
				<!--<ul>
					<li>我是孙子</li>
				</ul>-->
			</li>
			<li>我是儿子</li>
			<li>我是儿子</li>
		</ul>
	</body>
		</style>
```

-----------------------------------------------

- [x] id和class选择符

- id 及 class 均是css 提供由用户自定义标签名称的选择符，用户可以使用选择符id及class 来对页面中的xhtml标签进行自定义名称，从而达到扩展xhtml标签及组合html标签的目的。

- id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

- id 选择器以 "#" 来定义。

- 例： id 选择符

		<p id="p1"> 这是一个段落 </p>

		#p1 {
		  font-size:12px;
		  font-weight:bold;
		}
例： class 选择符

		<p class="p1"> 这是一个段落 </p>

		.p1 {
		  font-size:12px;
		  font-weight:bold;
		}
>在网页中，每个id名称中只能使用一次，不得重复。

>与id 不同，class 允许重复使用。比如页面中的多个元素，都可以使用同一个样式定义。

>一个元素可以定义多个class，用空格隔开

-----------------------------------------------

- [x] 伪类选择器

| 选择符           | 版本         |  描述        |
| :-------------------------:   | :----------: | :----------:  |
| E:link    | css1 |   设置超链接a在未被访问前的样式。    |
| E:visited    | css1 |   设置超链接a在已被访问过时的样式。    |
| E:hover    | css1/2 |   设置元素在鼠标悬停是的样式。    |
| E:active    | css1/2 |   设置元素在被用户激活(在鼠标点击与释放之间发生的事件)时的样式    |
| E:focus    | css1/2 |   设置元素在成为输入焦点(该元素的onfocus事件发生)时的样式    |
| E:not(s)    | css3 |   匹配不含有s选择符的元素E。    |
| E:root    | css3 |   匹配E元素在文档的根元素。常指html元素    |
| E:first-child    | css2 |   匹配父元素的第一个子元素E。    |
| E:last-child    | css3 |   匹配父元素的最后一个子元素E。    |
| E:noly-child    | css3 |   匹配父元素的仅有的一个子元素E。    |
| E:nth-child(n)    | css3 |   匹配父元素的第n个子元素E。    |
| E:nth-last-child(n)    | css3 |   匹配父元素的倒数第n个子元素E。    |
| E:first-of-type    | css3 |   匹配同类型中的第一个同级兄弟元素E。    |
| E:last-of-type    | css3 |   匹配同类型中的最后一个同级兄弟元素E。    |
| E:only-of-type    | css3 |   匹配同类型中的唯一的一个同级兄弟元素E。    |
| E:nth-of-type(n)    | css3 |   匹配同类型中的n个同级兄弟元素E。    |
| E:nth-last-of-type(n)    | css3 |   匹配同类型中的倒数第n个同级兄弟元素E。    |
| E:checked    | css3 |   匹配用户界面上处于选中状态的元素E。（用于input type为radio和CheckBox）    |
| E:enabled    | css3 |   匹配用户界面上处于可用状态的元素E。    |
| E:disabled    | css3 |   匹配用户界面上处于不可用状态的元素E。    |
| E:target    | css3 |   匹配相关URL指向的元素。    |

> 伪类：
	
- 1、交互效果
- 2、选择第n个元素
	
	
		<style type="text/css">
			/*设置超链接a在未被访问前的样式。*/
			a:link {
				color: #D30408;
			}
			/*设置超链接a在其链接地址已被访问过时的样式。*/
			a:visited {
				color: blue;
			}
			/*设置元素在其鼠标悬停时的样式。*/
			a:hover {
				font-weight: bold;
			}
			/*设置元素在被用户激活(在鼠标点击与释放之间发生的事件)时的样式。*/
			a:active {
				text-decoration: none;
			}
			/*设置元素在成为输入焦点(该元素的onfocus事件发生)时的样式。*/
			input:focus {
				outline: none;
			}
			/*勾选CheckBox选中状态*/
			input:checked + label {
				color: red;
			}
		</style>
		
		<a href="#">点我，有惊喜</a>
		<input type="text" name="" id="" value="" />
		<!--勾选CheckBox，让label也切换样式-->
		<input type="checkbox" checked="checked" id="check"/>
		<label for="check">选中		
		</label>

* 伪类选择器child系列
	- 选择器：第几个儿子
	- nth里面的括号要传入的1开始的值，可以结合未知数n来使用
	
			/*匹配父元素的第一个子元素E。*/
			ul li:first-child {
				color: blue;
			}
			/*匹配父元素的最后一个子元素E。*/
			ul li:last-child {
				color: blue;
			}
			/*匹配父元素的第n个子元素E。*/
			ul li:nth-child(2n) {
				background: red;
			}
			/*匹配不含有s选择符的元素E,除了第二个选择器以外，其余字体大小为20px*/
			ul li:not(:nth-child(2)) {
				font-size: 20px;
			}
			<ul>
			<li>伪类选择器1</li>
			<li>伪类选择器2</li>
			<li>伪类选择器3</li>
			<li>伪类选择器4</li>
			<li>伪类选择器5</li>
		</ul>	
**第n个儿子和同类型的才能匹配**

- span无效果

		ul li:nth-child(2) {
			text-decoration: underline;
		}
		<ul>
			<li>伪类选择器1</li>
			<span>伪类选择器2</span>
			<li>伪类选择器3</li>
			<li>伪类选择器4</li>
			<li>伪类选择器5</li>
		</ul>
		
相反，type类型的没child限制

		ol li:first-of-type {
			font-weight: bold;
		}
		/*第2n个li出现效果*/
		ol li:nth-of-type(2n) {
			letter-spacing: 5px;
		}
			
		<ol>
			<li>匹配同类型中的选择器1</li>
			<span>匹配同类型中的选择器2</span>
			<li>匹配同类型中的选择器3</li>
			<li>匹配同类型中的选择器4</li>
			<li>匹配同类型中的选择器5</li>
			<li>匹配同类型中的选择器6</li>
			<li>匹配同类型中的选择器7</li>
		</ol>
**[返回目录](#zore)**

-----------------------------------------------

- [x] 属性选择器

| 选择符           | 版本         |  描述        |
| -------------------------   | ----------  | :----------:  |
| E[attr]    | css2 |   选择具有attr属性的E元素    |
| E[attr="val"]    | css2 |   选择具有attr属性的元素且属性值为val的E元素    |
| E[attr~="val"]    | css2 |   选择具有attr属性的元素且属性值为一空元素分隔的字词列表，其中一个等于val的E元素   |
| E[attr^="val"]    | css3 |   选择具有attr属性的元素且属性值开头为val的字符串的E元素    |
| E[attr$="val"]    | css3 |   选择具有attr属性的元素且属性值结尾为val的字符串的E元素   |
| E[attr*="val"]    | css3 |   选择具有att属性且属性值为包含val的字符串的E元素。    |
| E[attr\="val"]    | css3 |   选择具有att属性且属性值且以val开头并且用"-"分隔的字符串的E元素。   |

事列1：
```
<style type="text/css">
			a {
				display: block;
				margin-top: 20px;
				text-decoration: none;
				color:#000;
			}
			a[class^='column'] {
				background: red;
			}
			a[href$="doc"] {
				background: green;
			}
			a[title*="box"] {
				background: blue;
			}
		</style>
	</head>

	<body>
		<a href="##" class="columnNews">我的背景想变成红色</a>
		<a href="##" class="columnVideo">我的背景想变成红色</a>
		<a href="##" class="columnAboutUs">我的背景想变成红色</a>
		<a href="1.doc">我的背景想变成绿色</a>
		<a href="2.doc">我的背景想变成绿色</a>
		<a href="##" title="this is a box">我的背景想变成蓝色</a>
		<a href="##" title="box1">我的背景想变成蓝色</a>
		<a href="##" title="there is two boxs">我的背景想变成蓝色</a>

事列2：

	</body>
			input[type="button"] {
				font-size: 30px;
			}
			
			input[type] {
				border: 1px solid #C40D0E;
			}
			/*选择具有att属性且属性值为以val开头的字符串的E元素。*/
			
			input[name^="p"] {
				border-color: blue;
			}
			/*选择具有att属性且属性值为以val结尾的字符串的E元素。*/
			
			input[name$="s"] {
				border-color: green;
			}
			
			input[value*="hello"] {
				border-color: green;
			}
			/*选择具有att属性且属性值为以val开头并用连接符"-"分隔的字符串的E元素。 */
			
			input[data-type|="dd"] {
				border-color: pink;
			}
	<input type="button" id="" value="btn" />
	<input type="submit" id="" name="" />
	<input type="radio" name="" id="" value="radio" /><label for=""></label>
	<input type="password" name="pass" value="hello" />
	<input type="text" name="pserachs" value="hello" data-type="dd-a">
	<input type="text" name="pserachs" value="hello" data-type="dd-a">
	<input type="text" name="pserachs" value="hello" data-type="dd">
```
**[返回目录](#zore)**

-----------------------------------------------

- [x] 伪对象选择器

| 选择符           | 版本         |  描述        |
| -----   | ----------  | :----------:  |
|E:first-letter/E::first-letter    | css1/3 |   设置对象内的第一个字符的样式。    |
|E:first-line/E::first-line     | css1/3 |   设置对象内的第一行的样式。     |
| E:before/E::before      | css2/3 |   设置在对象前（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用   |
| E:after/E::after    | css2/3 |   设置在对象后（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用    |
| E::placeholder    | css3 |   设置对象文字占位符的样式。   |
| E::selection    | css3 |   设置对象被选中时的样式

事列：    
```
<style type="text/css">
			/*p元素前面插入123*/
			p::before {
				content: '123';
			}
			
			p::after {
				content: 'abc';
			}
			/*ie10+,placeholder字体变绿*/
			
			input::-moz-placeholder {
				color: green;
			}
			
			input::-ms-input-placeholder {
				color: green;
			}
			
			input::-webkit-input-placeholder {
				color: green;
			}
			/*设置对象被选中时的样式*/
			h3::-moz-selection {
				background-color: red;
			}
			h3::selection {
				background: red;
			}
			p::-moz-selection {
				background-color: #E13300;
				color: white;
			}
			
			p::selection {
				background-color: #E13300;
				color: #333;
			}
		</style>
	</head>

	<body>
		<p class="test">test</p>
		<!--渲染为123 test abc-->
		<input type="search" placeholder="测试">
		<h3>请使用鼠标选取我</h3>
		<p>请使用鼠标选取我</p>

	</body>
```
**[返回目录](#zore)**

-----------------------------------------------

<a name="文本"></a>

## 文本

### 控制非中文字体换行规则
> - 这个属性是基于该容器允许换行的前提下才会生效，例如之前已经设置了white-space:nowrap,则该属性无效
> - 语法： word-break: normal | break-all
> - normal 依照亚洲语言和非亚洲语言的文本规则，允许在字内换行
> - break-all 允许非亚洲语言文本行的任意字内断开，例如连续的英文字母和数字

### 小结
- white-space:    一般用于强制文本单行显示。搭配overflow:hidden和text-overflow:ellipsis使用，
	      达到文字溢出显示省略号处理 。

- word-spacing:   定义元素中字之间插入多少空白符。“字” 定义为由空白符包围的一个字符串,即
	      “”abc” “efg“  两者为两个字符串可以使用负值.

- letter-spacing:   控制段落的文字间的距离,”字”定义为每一个字符,即ab为两个字符,可以使用负值

- word-break:       这个属性是基于该容器允许换行的前提下才会生效，如之前已设置white-space:nowrap,
	        则该属性无效.
 	        若设置word-break:normal;则letter作为一个单词是不会换行的

### text-transform
- 检索或设置对象中的文本的大小写。
- 取值：
  - none无转换
  - capitalize将每个单词第一个字母转换成大写
  - uppercase将每个单词转换成大写
  - lowercase将每个单词转换成小写
  - full-width（IE11+）所有字符转换成fullwidth形式。如果字符没有相应的fullwidth形式，将保留原样。这个值通常用于排版拉丁字符和数字等表意符号。（CSS3）

### vertical-align
	
	适用于：内联及 table-cell 元素
	取值：
		baseline：
		将支持valign特性的对象的内容与基线对齐
		sub：
		垂直对齐文本的下标
		super：
		垂直对齐文本的上标
		top：
		将支持valign特性的对象的内容与对象顶端对齐
		text-top：
		将支持valign特性的对象的文本与对象顶端对齐
		middle：
		将支持valign特性的对象的内容与对象中部对齐
		bottom：
		将支持valign特性的对象的文本与对象底端对齐
		text-bottom：
		将支持valign特性的对象的文本与对象顶端对齐
		<percentage>：
		用百分比指定由基线算起的偏移量。可以为负值。基线对于百分数来说就是0%。
		<length>：
		用长度值指定由基线算起的偏移量。可以为负值。基线对于数值来说为0。（CSS2）

### text-shadow
	- 取值：
		none：
		无阴影
		<length>①：
		第1个长度值用来设置对象的阴影水平偏移值。可以为负值
		<length>②：
		第2个长度值用来设置对象的阴影垂直偏移值。可以为负值
		<length>③：
		如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值
		<color>：
		设置对象的阴影的颜色。
		
# CSS布局
> 传统布局div + css
```
<div id="header">页面头部</div>

<div id="content">
	<div id="left"></div>
	<div id="right"></div>
</div>

<div id="footer">页脚</div>
> 并列与嵌套div结构
```
- ![传统布局样式](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1535351869334&di=34374b8490d6a17c20dfbb119ecd6900&imgtype=0&src=http%3A%2F%2Fimage.codes51.com%2FArticle%2Fimage%2F20160301%2F20160301092939_5974.png)

- 设配IE9以及主流手机端页面布局方式
```
<header>页面头部
	<nav>导航</nav>
</header>
<section>
	<aside> </aside>
	<article></article>
</section>
<footer>页脚</footer>
```
-  ![主流布局样式] (http://www.html5jscss.com/pic/htmljscss/html5-layout.jpg)
### 块级元素
- 常见的块级元素：
> `div h1~h6 p section aside article hr dl dt
				dd form footer table`
				
css语法： display：block

### 行内元素
- 常见的行内元素：
> `span、a、input、select、textarea、sub、sup、label、img、i、b、em、br、video、audio、 canvas`

css 语法: display: inline

注意:
input、select、textarea、 img  置换元素（通过属性来控制显示的内容）。这类特殊的元素都自带了宽高，所以这种元素可以设置宽高和设置垂直方向的边距(margin、padding)。

### 块级元素与行内元素区别
1、块级元素会独占一行，其宽度自动填满其父元素的宽高

行内元素不会独占一行，相邻的行内元素会排列在同一行，若一行排不下，会自动换行。其宽度会随内容的变化而变化

2、块级元素可以设置width和height属性，行内元素设置宽高无效[注意：块级元素技术设置了宽高，但是仍然独占一行]

3、块级元素可以设置margin和padding。行内元素的水平方向的padding-left，right;margin-left，right;都产生边距效果，
但是垂直方向的padding-top,padding-bottom,margin-top,margin-bottom无效（水平方向有效，垂直方向无效）

<a name="元素的定位"></a>

### 元素的定位

语法：position： **static** | **absolute** | **relative** | **fixed**
> static: 无定位，默认值

> absolute: 绝对定位
- 脱离文档流
- 通过top,right,bottom,left定位
- 如果父元素position为static，将以body坐标原点定位
- 如果父元素position为relative，将以父元素进行定位

> relative: 相对定位
- 相对定位（相对自己原来的位置而言）
- 不脱离文档流
- 参考自身静态位置通过top,right,bottom,left定位

> fixed: 固定定位
- 固定定位其实是绝对定位的特殊形式；固定定位相对浏览器窗口而固定
而不是相对其包含元素;即使页面滚动了，他仍然处于浏览器窗口中跟原来的一样的地方

> z-index:层叠
  - 适用于：定位元素。即定义了position为非static的元素
  - 检索或设置对象的层叠顺序。
  - z-index用于确定元素在当前层叠上下文中的层叠级别，并确定该元素是否创建新的局部层叠上下文。
  - 每个元素层叠顺序由所属的层叠上下文和元素本身的层叠级别决定（每个元素仅属于一个层叠上下文）。
  - 同一个层叠上下文中，层叠级别大的显示在上面，反之显示在下面。
  - 同一个层叠上下文中，层叠级别相同的两个元素，依据它们在HTML文档流中的顺序，写在后面的将会覆盖前面的。
  - 不同层叠上下文中，元素的显示顺序依据祖先的层叠级别来决定，与自身的层叠级别无关。
  - 当z-index未定义或者值为auto时，在IE6,7下会创建新的局部层叠上下文，而在高级浏览器中，按照规范不产生新的局部层叠上下文
  
**[返回目录](#zore)**

<a name="边框"></a>

## 边框

	默认值：看每个独立属性

	适用于：所有元素
	
	继承性：无
	
	动画性：看每个独立属性
	
	计算值：看每个独立属性
	
	相关属性：[ border-top ] || [ border-right ] || [ border-bottom ] || [ border-left ]
	
	取值：
	<line-width>：
	设置或检索对象边框宽度。
	<line-style>：
	设置或检索对象边框样式。
	<color>：
	设置或检索对象边框颜色。

