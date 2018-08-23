# CSS3
css和css3基础知识点大全
###什么是css
> css层叠样式表，CSS3知识CSS2的升级版本，在2的基础上增加了好多新的特性
> 前缀        浏览器
> - [-webkit]   chrome和safari
> - [-moz]      firefox
> - [-ms]   	IE
> - [-O]   		Opera

###CSS能做什么？

> 1、CSS把很多以前需要使用图片和脚本来实现的效果、甚至动画效果，只需要短短几行代码就能搞定。比如圆角，图片边框，文字阴影和盒阴影，过渡、动画等。

> CSS简化了前端开发工作人员的设计过程，更灵活的页面布局，更快的页面加载速度。

> 可以将站点上所有的网页风格都使用一个CSS文件进行控制，只要修改这个CSS文件中相应的代码，那么整个站点的所有页面都会随之发生变动。

> CSS可以支持多种设备,比如手机,PDA,打印机,电视机,游戏机等。

> 目的：将表现与结构分离。

###CSS的选择符可以分成:
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
| -------------------------   | ----------  | :----------:  |
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

事列：
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

	</body>

```

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

-----------------------------------------------

