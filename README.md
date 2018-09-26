<a name="zore"></a>
# CSS3+HTML5笔记

* CSS和CSS3基础知识点大全
	- [什么是css](#什么是css)
	- [css引入](#css引入)
	- [CSS的选择符](#CSS的选择符)
	- [元素的定位](#元素的定位)
	- [文本](#文本)
	- [边框](#边框)
	- [字体样式](#字体样式)
	- [段落样式](#段落样式)
	- [背景](#背景)
	- [浮动](#浮动)


* HTML5笔记
	- [html基础](#html基础)
	- [html段落](#html段落)
	- [文本格式化](#文本格式化)
	- [a标签](#a标签)
	- [表格](#表格)
	- [表单](#表单)
	- [内联框架](#内联框架)
	- [音频+视频](#音频、视频)


## 什么是 HTML？

> HTML 是用来描述网页的一种语言。
- HTML 指的是超文本标记语言 (Hyper Text Markup Language)
- HTML 不是一种编程语言，而是一种标记语言 (markup language)
- 标记语言是一套标记标签 (markup tag)
- HTML 使用标记标签来描述网页

**学习路线**

![](http://html5book.bluej.cn/static/images/%E5%89%8D%E7%AB%AF%E5%8F%91%E5%B1%95%E6%8A%80%E8%83%BD%E6%A0%91.png)


<a name="html基础"></a>

#### html基础

HTML标题

- HTML
 标题（Heading）是通过 `<h1> - <h6>` 等标签进行定义的。
>事列

		<h1>This is a heading</h1>
		<h2>This is a heading</h2>
		<h3>This is a heading</h3>

<a name="html段落"></a>		

### html段落

- HTML 段落是通过 `<p>` 标签进行定义的。
> 实例

		<p>This is a paragraph.</p>
		<p>This is another paragraph.</p>
		
p元素是块级元素，不能嵌套块级元素，列如p，div，table，ul
	
<a name="文本格式化"></a>		

### 文本格式化

        <b>定义粗体文本</b>
        <i> 定义斜体文本 </i>
        <del>定义删除文本</del>
        <sup>定义上标字</sup>
        <sub>定义下标字</sub>
 
<a name="a标签"></a>    
   
### a标签
		
			<!-- 
	    <a href=“URL”> ~ </a>
	    说明：
	    href        定义链接地址
	    title       链接提示信息
	    target      链接打开方式(_blank 新的空白页,_self  当前页,_top(结合iframe使用))
	
	     -->
```     
<a href="" title="你好" target="_top">hello world</a>
<a href="tel:电话号码" title="你好" target="_top">拨打号码</a>
<a href="" title="你好" target="_top">hello world</a>
<a href="" title="你好" target="_top">hello world</a>
<a href="" title="你好" name="p元素.html">hello world</a>
<a href="" target=""></a>
```
	    <!--baidu.com 一级域名
	    	二级域名：http://news.baidu.com/
	    -->
	    <a href="https://www.baidu.com">跳转到百度</a>
	    <!--相对地址-->
	    <a href="./p元素.html">p元素</a>
	    <!--锚点-->
	    <a href="#one">跳转到第二章</a>
	    
	    
	    <h1 style="height: 400px;">一</h1>
	    
	    <a name="one"></a>
	    <h2>二</h2>
	    
	    <!--跳转到顶部-->
	    <a name="top"></a>
	    <p style="height: 900px;">1、块级元素会独占一行，其宽度自动填满其父元素的宽高
	
	行内元素不会独占一行，相邻的行内元素会排列在同一行，若一行排不下，会自动换行。其宽度会随内容的变化而变化</p>
	    <a href="#top">跳转到p段落顶部</a>

<a name="表格"></a> 

### 表格	    

		<!--
			
			border： 边框
			cellspacing： 单元格外边距
			cellpadding： 单元格内边距
			thead: 表头
			tbody：表的主体
			tfoot： 表尾
			tr代表行
			th代表表头
			td: 普通单元格
			rowspan: 行合并
			colspan: 列合并
			
		-->
		<!--
			td包含的属性： rowspan: 行合并，colspan: 列合并（数字是多少就代表占多少格）
			align: 单元格内容水平对齐方式：left（默认） right，center
			valign: 单元格内容垂直对齐方式：middle（默认） top，bottom
			
		-->
		<table border="" cellspacing="" cellpadding="30">
			<thead>
				<tr>
					<th>姓名111111111111111</th>
					<th>年龄</th>
					<th>班级</th>
				</tr>
			</thead>

			<tbody>
				<tr align="center">
					<td>张三</td>
					<td>18</td>
					<td rowspan="2">33</td>
				</tr>
				<tr align="center">
					<td>李四</td>
					<td>20</td>
				</tr>
			</tbody>
			<tfoot>
				<tr>
					<th>人数</th>
					<th colspan="2">2</th>
				</tr>
			</tfoot>
		</table>
		<table border="" cellspacing="" cellpadding="30">
			<!--
				col: 代表列，通过控制col列控制列的样式
				span: 合并
				caption： 标签必须紧随 table 标签之后。您只能对每个表格定义一个标题。通常这个标题会被居中于表格之上。
			-->
			<caption>表格的内容</caption>
			<colgroup>
				<col span="2" style="background-color: aquamarine;"/>
				<col/>
			</colgroup>
			<tr>
				<th>Header</th>
				<th>Header</th>
				<th>Header</th>
			</tr>
			<tr>
				<td>Data</td>
				<td>Data</td>
				<td>Data</td>
			</tr>
			<tr>
				<td>Data</td>
				<td>Data</td>
				<td>Data</td>
			</tr>
		</table>

		
<a name="表单"></a> 		

### 表单

		<!--
			action： 提交的地址
			method： get，post
			get，post的区别：
			您能够使用 GET（默认方法）：

			如果表单提交是被动的（比如搜索引擎查询），并且没有敏感信息。
			
			当您使用 GET 时，表单数据在页面地址栏中是可见的：	
			
			action_page.php?firstname=Mickey&lastname=Mouse
			
			注释：GET 最适合少量数据的提交。浏览器会设定容量限制。
			POST：
			
			如果表单正在更新数据，或者包含敏感信息（例如密码）。
			
			POST 的安全性更加，因为在页面地址栏中被提交的数据是不可见的。
			
			1、传参方式
				- get: 内容通过URL地址传参，post裸露在请求体里面
			2、安全性
				- get： 内容裸露在url, post相对安全
			3、数量
				- get 数据量交于post少
		-->   
		<!--
			input属相：
				type： 类型（text，password，button，submit）
				name： 表示数据对应的参数名
				value： 值
				placeholder： 提示语
				disable： 不可用状态
		-->
		<form action="http://c14.bluej.cn/api/form.php" method="post" >
			<div class="about">
				用户名： <input type="text" name="username" value="" / placeholder="请输入用户名"> 
			</div>
			<div class="about">
				密码： <input type="password" name="password" value="" placeholder="请输入用户密码" />
			</div>
			<input type="submit" value="提交"/>
		</form>
		
#### 表单常用类型
	
	input：
		
			<div>
				用户： <input type="text" name="username" />
			</div>
			<div>
				密码： <input type="password" name="password" />
			</div>
			<div>
				手机号： <input type="number" name="number" />
			</div>
			<div>
				<!--
				
			radio单选：如果是使用表示同一组数据的不用选项，就要设置相同的name的值
			lable 标签的作用是将输入项或选项及其标签文字关联起来。
			label的for属相相同时，就可以点击label选中radio，id是惟一的
			-->
				<label for="man">
				男生： <input type="radio" name="sex" id="man" />
			</label>
				<label for="woman">
				女生： <input type="radio" name="sex" id="woman"/>
			</label>
			</div>
			<div>
				<!--
				checkbox：单选多选
				
			-->
				擅长：
				<label for="lol">英雄联盟<input type="checkbox" name="lol" id="lol" checked="checked"/></label>
				<label for="王之荣耀">王之荣耀<input type="checkbox" name="王之荣耀" id="王之荣耀" /></label>
			</div>
			
	下拉框：
		
		<div>
				<!--
				下拉框：
				option： 分组
				optgroup的label： 设置组名
				size： 下拉列表框的显示行数
				multiple			是否多选
				disabled			是否禁用
				selected			设置默认选中的选项
				value			选项的值

			-->
				地址：
				<select name="city">
					<option value="gz">广州</option>
					<option value="sh">深圳</option>
					<option value="zh">珠海</option>
					<option value="qy">清远</option>
					<option value="bj">北京</option>
				</select>
		</div>
	

[表格和表单制作简历案例：](https://struggle-wjf.gitee.io/table_resume__dome/)

<a name="内联框架"></a>

### 内联框架iframe

作用：
	
	引入其他页面来使用
	列如：地图组件、客服系统等第三方工具
	引入的是别人的页面，有些样式不能修改
	
    - <iframe src="iframe2.html" width="800" height="600" frameborder="no">
	</iframe>
	
a标签和iframe的配合使用：

		_parent让父框架进行跳转
		
		<a href="https://www.baidu.com/" target="_parent">跳转百度页面</a>
		<br />
		_self自身跳转
		
		<a href="https://www.baidu.com/" target="_self">跳转百度页面</a>
		
		_top 让最顶层的框架跳转,也就是最外层
		
		<a href="https://www.baidu.com/" target="_top">跳转百度页面</a>
		
			1._blank      <a href="document.html" target="_blank">my document</a> 
                  	浏览器会另开一个新窗口显示document.html文档   
			2._parent     <a href="document.html" target="_parent">my document</a>      
			                  指向父frameset文档   
			3._self       <a href="document.html" target="_self">my document</a>           
			                  把文档调入当前页框  
			4._top        <a href="document.html" target="_top">my document</a>          
			                  去掉所有页框并用document.html取代frameset文档   
			

<a name="音频、视频"></a>

### 音频：

**audio标签用来引用音频标签**
	
- src： 引入的资源
- controls: 控件，在不同浏览器下面呈现的样式也会不同
- autoplay: 自动播放
- loop: 循环播放
- preload： 如果出现该属性，则音频在页面加载时进行加载，并预备播放。如果		使用 "autoplay"，则忽略该属性。
- muted： 静音

		<audio src="media/music.mp3" preload="auto" controls="controls" muted="muted">

		</audio>
		
音频的兼容性写法

		<audio>
			<source src="media/music.mp3" type="audio/mp3" />
			<source src="media/ogg.ogg" type="audio/ogg" />
			<p>Your browser does not support the audio tag.</p>
			<a href="media/ogg.mp3">点击下载此视频</a>
		</audio>
		
- source： 引入资源
- type： 音频类型

### 视频：

video
			
		autoplay	autoplay	如果出现该属性，则视频在就绪后马上播放。
		controls	controls	如果出现该属性，则向用户显示控件，比如播放按钮。
		loop	loop	如果出现该属性，则当媒介文件完成播放后再次开始播放。
		muted	muted	规定视频的音频输出应该被静音。
		poster	URL	规定视频下载时显示的图像，或者在用户点击播放按钮前显示的图像。
		preload	preload	如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果                  		使用 "autoplay"，则忽略该属性。
		src	url	要播放的视频的 URL。
		width	pixels	设置视频播放器的宽度。
		height	pixels	设置视频播放器的高度。
		
	<video src="media/video.mp4" controls="controls" autoplay="autoplay"></video>
	
视频兼容性写法：

		<video width="800" height="">
			<source src="media/video.flv" type="video/mp4"></source>
			<source src="media/video.mp4" type="video/mp4"></source>
			<source src="media/video.webm" type="video/webm"></source>
			<object width="" height="" type="application/x-shockwave-flash" data="myvideo.swf">
				<param name="movie" value="myvideo.swf" />
				<param name="flashvars" value="autostart=true&amp;file=myvideo.swf" />
			</object>
			当前浏览器不支持 video直接播放，点击这里下载视频： <a href="myvideo.webm">下载视频</a>
		</video>
	
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
- [x] 伪类选择符
- [x] 属性选择符
- [x] 伪对象选择符

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

**注意细节**
		
E::before

- 在p标签内容添加信息
- 内容之前添加一个伪元素
- 必须设置content调用出来，即使值为空也要写
- 为元素为行内元素
	
E::first-letter: 设置对象内的第一个字符的样式。

- 此伪对象仅作用于块对象。内联对象要使用该伪对象，必须先将其设置为块级对象。该伪类常被用来配合font-size属性和float属性制作首字下沉效果。	
	
E:first-line/E::first-line : 设置对象内的第一行的样式。

- 此伪对象仅作用于块对象。内联对象要使用该伪对象，必须先将其设置为块级对象。
	
E::selection: 设置对象被选择时的颜色。 

- 需要注意的是，::selection只能定义被选择时的background-color，color及text-shadow(IE11尚不支持定义该属性)。
	
E::placeholder  : 设置对象文字占位符的样式。兼容性不好，同时设置会覆盖

- ::placeholder 伪元素用于控制表单输入框占位符的外观，它允许开发者/设计师改变文字占位符的样式，默认的文字占位符为浅灰色。
	
		当表单背景色为类似的颜色时它可能效果并不是很明显，那么就可以使用这个伪元素来改变文字占位符的颜色。
	
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
	
				div5 {
				width: 200px;
				height: 200px;
				border: 1px dashed #0000FF;
				}

	
三角形画法

		1、三角形的方向，假设三角形朝上，设置底边
		2、量宽度
		3、将三角形腰的两条边设置透明颜色
		
				width: 0px;
				height: 0px;
				border-top: 0px solid transparent;
				border-right: 20px solid transparent;
				border-bottom: 20px solid #07521e;
				border-left: 8px solid transparent;
边框样式：

	none：无轮廓。border-color将被忽略，border-width计算值为0，除非边框轮廓为图像，即border-image。
	hidden：隐藏边框。IE7及以下尚不支持
	dotted：点状轮廓。IE6下显示为dashed效果
	dashed：虚线轮廓。
	solid：实线轮廓
	double：双线轮廓。两条单线与其间隔的和等于指定的border-width值
	groove：3D凹槽轮廓。
	ridge：3D凸槽轮廓。
	inset：3D凹边轮廓。
	outset：3D凸边轮廓。

- border-radius圆角

	- border-radius: 25px;可以是具体的像素，也可以是百分比%
	
例子：

		/* 所有角都使用半径为10px的圆角 */ 
		div{ border-radius:10px;}  
		
		/* 四个半径值分别是左上角、右上角、右下角和左下角，顺时针 */ 
		div{ border-radius: 5px 4px 3px 2px; }
			
		/*也可以分别设置每个角的垂直半径和水平半径,用斜杠隔开，第一个参数表示左上角开始顺时针的水平半径，第二个参数表示左上角开始顺时针的垂直半径*/
		div{ border-radius: 10px 20px 30px 40px  /  5px 10px 15px 20px; }
		
		/*圆*/
		div{ border-radius:50% }
		
		<div>
			这是一个有边框的圆角
		</div>
		
		div {
			width: 200px;
			height: 200px;
			border: 2px solid;
			border-radius: 25px;
			-moz-border-radius: 25px;
			text-align: center;
		}
		
		
- border-img圆角边框

			<style>
			body
			{
				margin:30px;
			}
			.serach {
				width: 40px;
				padding: 5px 10px;
				border: 10px solid transparent;
				border-image: url(http://www.w3school.com.cn/i/border_image_button.png) 0 14 0 14 stretch;
			}
			.img3 {
				border:15px solid transparent;
				width:300px;
				padding:10px 20px;
				border-image: url(http://www.w3school.com.cn/i/border.png) 30 30 round;
			}
			.img4 {
				border:15px solid transparent;
				width:300px;
				padding:10px 20px;
				border-image: url(http://www.w3school.com.cn/i/border.png) 20 20 stretch;
			}
			</style>
			<!--  Internet Explorer 11, Firefox, Opera 15, Chrome 以及 Safari 6 支持 border-image 属性。
			
			Safari 5 支持替代的 -webkit-border-image 属性。
			定义和用法
			border-image 属性是一个简写属性，用于设置以下属性：
			
			border-image-source	用在边框的图片的路径。	
			border-image-slice	图片边框向内偏移。	
			border-image-width	图片边框的宽度。	
			border-image-outset	边框图像区域超出边框的量。	
			border-image-repeat	图像边框是否应平铺(repeated)、铺满(rounded)或拉伸(stretch)。
		-->
		<div class="serach">
			Search
		</div>
		<div>
			
		</div>
		<div class="img1">
			<p>这是我们使用的图片：</p>
			<img src="http://www.w3school.com.cn/i/border_image_button.png" alt="">
		</div>
		<div class="img2">
			<p>原始图片</p>
			<img src="http://www.w3school.com.cn/i/border.png" alt="">
		</div>
		<br>
		<br>
		<br>
		<br>
		<div class="img3">
			border-image 属性允许您规定用于边框的图片！
		</div>
		<div class="img4">
			border-image 属性允许您规定用于边框的图片！
		</div>
		</body>

**[返回目录](#zore)**

<a name="字体样式"></a>

### 字体样式

- font-family： 字体名称。按优先顺序排列。以逗号隔开。如果字体名称包含空格或中文，则应使用引号括

		p {
			font-family: "微软雅黑",arial,"黑体";
			font-weight: 400;
		}
- font-size：字体大小
		
		p {
			font-size: 16px;
		}
		
- font-style：字体样式

		font-style : normal | italic | oblique 
			normal：
			指定文本字体样式为正常的字体
			italic：
			指定文本字体样式为斜体。对于没有设计斜体的特殊字体，如果要使用斜体外观将应用oblique
			oblique：
			指定文本字体样式为倾斜的字体。人为的使文字倾斜，而不是去选取字体中的斜体字
			
- font-weight：字体粗细

		font-weight : normal | bold | bolder | lighter | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 
		
#### [自定义字体的引入](http://www.iconfont.cn/home/index?spm=a313x.7781069.1998910419.2)

在阿里云字体图标中去引用

		@font-face {font-family: "iconfont";
		  src: url('iconfont.eot?t=1537861818426'); /* IE9*/
		  src: url('iconfont.eot?t=1537861818426#iefix') format('embedded-opentype'), /* IE6-IE8 */
		  url('data:application/x-font-woff;charset=utf-8;base64,d09GRgABAAAAAAWEAAsAAAAACCgAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAADMAAABCsP6z7U9TLzIAAAE8AAAARAAAAFY8r0ivY21hcAAAAYAAAABfAAABnLSUHiVnbHlmAAAB4AAAAZ0AAAHstzmbCWhlYWQAAAOAAAAALwAAADYSz1dxaGhlYQAAA7AAAAAgAAAAJAfvA5NobXR4AAAD0AAAABAAAAAQEA8AAGxvY2EAAAPgAAAACgAAAAoBRgCubWF4cAAAA+wAAAAfAAAAIAERAEZuYW1lAAAEDAAAAUUAAAJtPlT+fXBvc3QAAAVUAAAALwAAAECwRGwWeJxjYGRgYOBikGPQYWB0cfMJYeBgYGGAAJAMY05meiJQDMoDyrGAaQ4gZoOIAgCKIwNPAHicY2BkYWGcwMDKwMHUyXSGgYGhH0IzvmYwYuRgYGBiYGVmwAoC0lxTGByeWTzbwdzwv4EhhrmRoREozAiSAwDwxQzZeJztkMEJgDAMRV/aKkUcxaOI80gPjtiJukZNEw8O4Q8vJJ+QwwcmICqbkkBuhKFLXTE/spifOHTPWgHa2UqrvX8nk9hF1in4B5n5tVrf3y2O1BzLsjjmVwd5APRZFnoAeJw1kD1P21AUhs97fT8SJzFx7MQTLgZhu0soTmwUKYQNZ+jasRIsYetfgG7tFDrC1JEBVenCGHVn6x+oVKQOZqjUjxG31005w3nv8JxzHl0ySJfxkn2lGkX0jGjbgttLsmFodAeOsqB8eEEahFG6FyTZASZI+4iCCI8cXvlxPI7jH/lpwjgQ+7gqZxIbED2/diYYnPbD7yf4tMKuUfVxzLLD8ueLmlPzY+SQfOy0vwkl2g4OH27/M1qNEf055W3jNW3SiKiOcFNB6ssHsLXZIJ1gT2d3oNP2KiFDO29Vjjq7W32kNrLEA6+XO73MLXdUy1H72PbvkKfDnN2th9hXHesdmuYNO5pOj9iN2cKJ6iic4BKfXbfsq05LTsqmRmdpDj04Q7iOXxPZ6pS7ZhOj6TFwPB3pHSzQs6q8qL5Vu38x3hs+Ncijp0RCW618rX+PlaQPx/Oh5BpkGIWpPcwGCaNFIUSx+FhwXnyYLzlfzs+r/ryoC8FFYbrSWGuoDX6/WJGL+/yROZ8v8f2tdE3B3whhSgW7YRH9BZ5CYE4AAAB4nGNgZGBgAOLii1p98fw2Xxm4WRhA4PoFzl0I+n89iwBzI5DLwcAEEgUAMb0KoQB4nGNgZGBgbvjfwBDDws/A8P8/iwADUAQFsAAAdIYEigQAAAAEAAAABA8AAAQAAAAAAAAAAFAArgD2AAB4nGNgZGBgYGGwYmBmAAEmIOYCQgaG/2A+AwAOpQFYAHicZY9NTsMwEIVf+gekEqqoYIfkBWIBKP0Rq25YVGr3XXTfpk6bKokjx63UA3AejsAJOALcgDvwSCebNpbH37x5Y08A3OAHHo7fLfeRPVwyO3INF7gXrlN/EG6QX4SbaONVuEX9TdjHM6bCbXRheYPXuGL2hHdhDx18CNdwjU/hOvUv4Qb5W7iJO/wKt9Dx6sI+5l5XuI1HL/bHVi+cXqnlQcWhySKTOb+CmV7vkoWt0uqca1vEJlODoF9JU51pW91T7NdD5yIVWZOqCas6SYzKrdnq0AUb5/JRrxeJHoQm5Vhj/rbGAo5xBYUlDowxQhhkiMro6DtVZvSvsUPCXntWPc3ndFsU1P9zhQEC9M9cU7qy0nk6T4E9XxtSdXQrbsuelDSRXs1JErJCXta2VELqATZlV44RelzRiT8oZ0j/AAlabsgAAAB4nGNgYoAALgbsgIWRiZGZkYWRlYElMdPMjK04I7+0MpUtKT8tMS+dgQEAStkGcwA=') format('woff'),
		  url('iconfont.ttf?t=1537861818426') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+*/
		  url('iconfont.svg?t=1537861818426#iconfont') format('svg'); /* iOS 4.1- */
		}
		
		.iconfont {
		  font-family:"iconfont" !important;
		  font-size:16px;
		  font-style:normal;
		  -webkit-font-smoothing: antialiased;
		  -moz-osx-font-smoothing: grayscale;
		}
		
		.icon-ai66:before { content: "\e6b8"; }
		
		.icon-shouye:before { content: "\e638"; }
		
		.icon-play:before { content: "\e664"; }
		
- 在HTML中link标签引入css文件

- 使用方法：

**标签尽量使用行内标签**
	
		<i class="iconfont icon-shouye">首页</i>
		<i class="iconfont icon-ai66">购物车</i>
		<i class=" iconfont icon-play"></i>

**[返回目录](#zore)**

[move的布局dome](https://struggle-wjf.gitee.io/move_layout/)

<a name="段落样式"></a>

### 段落样式

1、段落缩进： text-indent 适用于：块容器
	
- 取值：

		<length>：用长度值指定文本的缩进。可以为负值。
		
		<percentage>：用百分比指定文本的缩进。可以为负值。
		
		
		each-line：定义缩进作用在块容器的第一行或者内部的每个强制换行的首行，软换行不受影响。（CSS3）
		
		hanging：反向所有被缩进作用的行。（CSS3）

2、段落对齐： text-align : left | right | center | justify 
	
- 取值：快容器

	left：内容左对齐。
	
	center：内容居中对齐。
	
	right：内容右对齐。
	
	justify：两端对齐，仅限于多行时，但对于强制打断的行（被打断的这一行）及最后一行（包括仅有一行文本的情况，因为它既是第一行也是最后一行）不做处理。（CSS3）
	
	start：内容对齐开始边界。（CSS3）
	
	end：内容对齐结束边界。（CSS3）
	
3、文字溢出
		
		/*文字在一行内的省略号*/
		.textOverflow1 {
			text-overflow: ellipsis; /*超出部分显示...*/
			overflow: hidden; /*超出部分隐藏*/
			white-space: nowrap;/*不换行*/
		}

		/*文字在二行内的省略号*/
		.textOverflow2 {
			text-overflow: ellipsis; /*超出部分显示...*/
			overflow: hidden; /*超出部分隐藏*/
			display: -webkit-box; /*设置为伸缩盒子*/
			-webkit-line-clamp: 2;/*这是要显示的行数*/
			-webkit-box-orient: vertical;/*设置排版方向为从上到下*/
		}

		/*文字在三行内的省略号*/
		.textOverflow2 {
			text-overflow: ellipsis; /*超出部分显示...*/
			overflow: hidden; /*超出部分隐藏*/
			display: -webkit-box; /*设置为伸缩盒子*/
			-webkit-line-clamp: 3;/*这是要显示的行数*/
			-webkit-box-orient: vertical;/*设置排版方向为从上到下*/
		}

4、 text-shadow

取值：

	none：无阴影
	
	<length>①：第1个长度值用来设置对象的阴影水平偏移值。可以为负值
	
	<length>②：第2个长度值用来设置对象的阴影垂直偏移值。可以为负值
	
	<length>③：如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值
	
	<color>：设置对象的阴影的颜色。
	
		<style>
			.test li{margin-top:10px;}
			.test .mormal p{text-shadow:1px 1px rgba(0,0,0,.3);}
			.test .blur p{text-shadow:1px 1px 1px rgba(0,0,0,.3);}
			.test .group p{text-shadow:1px 1px 0 rgba(255,255,255,1),1px 1px 2px rgba(0,85,0,.8);}
		</style>
		</head>
			<body>
			<ul class="test">
				<li class="mormal">
					<strong>普通文字阴影</strong>
					<p>测试普通文字阴影效果</p>
				</li>
				<li class="blur">
					<strong>模糊文字阴影效果</strong>
					<p>测试模糊文字阴影效果</p>
				</li>
				<li class="group">
					<strong>多重模糊文字阴影效果</strong>
					<p>测试多重模糊文字阴影效果</p>
				</li>
			</ul>
		</body>

5、box-shadow和text-shadow用法相似

[实战中布局演示](https://struggle-wjf.gitee.io/new_word_static_web_page/)

**[返回目录](#zore)**

<a name="背景"></a>

### 背景

- background-image: 指定对象的背景图像。可以是真实图片路径或使用渐变创建的“背景图像

	`background-image:url(test1.jpg),url(test2.jpg),url(test3.jpg);`

可以写多个背景图片:

> 如果设置了 <' background-image '>，同时也建议设置 <' background-color '> 用于当背景图像不可见时保持与文本颜色有一定的对比度。
如果定义了多组背景图，且背景图之间有重叠，写在前面的将会盖在写在后面的图像之上。

- background-repeat： 指定对象的背景图像如何铺排填充。

	- repeat-x：背景图像在横向上平铺

	- repeat-y：背景图像在纵向上平铺
	
	- repeat：背景图像在横向和纵向平铺
	
	- no-repeat：背景图像不平铺
	
	- round：背景图像自动缩放直到适应且填充满整个容器。（CSS3）

	- space：背景图像以相同的间距平铺且填充满整个容器或某个方向。（CSS3）

- background-size： 指定对象的背景图像的尺寸大小。
取值：

		<length>：用长度值指定背景图像大小。不允许负值。
		
		<percentage>：用百分比指定背景图像大小。不允许负值。
		
		auto：背景图像的真实大小。
		
		cover：将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。
		
		contain：将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。
	
- background-position： 指定对象的背景图像位置。

取值：
>背景图位置 ，默认先x后y，可以先写方位，再写具体尺寸 left 10px bottom
		<percentage>：用百分比指定背景图像填充的位置。可以为负值。
		
		<length>：用长度值指定背景图像填充的位置。可以为负值。
		
		center：背景图像横向和纵向居中。
		
		left：背景图像在横向上填充从左边开始。
		
		right：背景图像在横向上填充从右边开始。
		
		top：背景图像在纵向上填充从顶部开始。
		
		bottom：背景图像在纵向上填充从底部开始。

- background-color：指定对象的背景颜色。
- background-origin 指定对象的背景图像显示的原点。

取值：

		padding-box：从padding区域（含padding）开始显示背景图像。
		
		border-box：从border区域（含border）开始显示背景图像。
		
		content-box：从content区域开始显示背景图像。

- background-clip 指定对象的背景图像向外裁剪的区域。

取值：

		padding-box：从padding区域（不含padding）开始向外裁剪背景。
		border-box：从border区域（不含border）开始向外裁剪背景。
		content-box：从content区域开始向外裁剪背景。
		text：从前景内容的形状（比如文字）作为裁剪区域向外裁剪，如此即可实现使用背景作为填充色之类的遮罩效果。遮罩效果 

<a name="浮动"></a>

### 浮动

取值：所有元素

	none：设置对象不浮动
	
	left：设置对象浮在左边
	
	right：设置对象浮在右边

> 浮动的目的：
	就是要打破文档流的默认显示规则。如果要让元素按照我们的布局要求进行显示。这时就
	要利用float属性。

- 说明：

	1.任何申明为 float 的元素自动被设置为一个“块级元素”。 
	
	2.在标准浏览器中 浮动元素脱离了文档流 ，所以浮动元素后的元素会占据浮动元素本来应该所处的位置。
	
	3.如果水平方向上没有足够的空间容纳浮动元素，则转向下一行 。
	
	4.文字内容会围绕在浮动元素周围 。
	
	5.浮动元素只能浮动至左侧或者右侧 。

	
特点：

	1、浮动的元素不占据空间，但是文字会环绕浮动的元素
	
	2、浮动的元素宽高默认由内容撑开，也可以设置宽高,也可以设置margin值
	
	3、清除浮动
	
	- 在一个父级元素添加一个块级元素
	
	- 伪类::after作为最后一个儿子清除浮动
			.clearfix::after {
				display: block;
				content: '';
				clear: both;
				height: 0;
				line-height: 0;
				visibility: hidden;
			}
			
	4、当父元素的宽度不足以放下子元素时，子元素就会自动往下一行布局
	
	5、不管是左浮动还是右浮动，宽度不足的时候，先掉下去的是最后一个儿子

清除浮动的三种方式：
	
1、在浮动元素后面紧跟一个空div,并给该div设置clear:both(全浏览器兼容)

2、给父元素添加overflow:auto即可(除了ie6要用zoom:1,其余都支持)

3、使用after伪对象清除浮动(支持IE8以上浏览器,但IE8只支持单冒号写法`:after`)

		.clearfix::after{
			display:block;
			clear:both;
			content:'';
			visibility:hidden;
			height:0;
			line-height:0;
		}
		.clearfix {
			zoom: 1; /*兼容ie*/
		}

**为什么要清除浮动**

浮动的元素不占据空间，父元素无法用内容来撑开

		<div class="box clearfix">
			<div class="son1 fl ">
				设置浮动元素
			</div>
			<!--<div class=""></div>-->
			<!--<p>
				<img src="dashuju.png"/>
				该属性的值指出了对象是否及如何浮动。请参阅clear属性如果float不是none，当display:inline-table时，display的计算值为table；当disp
				该属性的值指出了对象是否及如何浮动。请参阅clear属性如果float不是none，当display:inline-table时，display的计算值为table；当disp
				该属性的值指出了对象是否及如何浮动。请参阅clear属性如果float不是none，当display:inline-table时，display的计算值为table；当disp
			</p>-->
		</div>
		
		.box {
				/*浮动的元素不占据空间*/
				/*父元素无法用内容来撑开，先可以看到，边框并没有包裹浮动的内容
				 实际大小就是2像素边框，所以要清除浮动
				 * */
				border: 1px solid #ADFF2F;
			}
			
**[返回目录](#zore)**