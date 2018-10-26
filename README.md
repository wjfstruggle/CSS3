<a name="zore"></a>

# CSS3+HTML5笔记

* HTML5笔记
	- [html基础](#html基础)
	- [html段落](#html段落)
	- [文本格式化](#文本格式化)
	- [a标签](#a标签)
	- [表格](#表格)
	- [表单](#表单)
	- [内联框架](#内联框架)
	- [音频+视频](#音频、视频)
	- [地图map](#地图map)

	
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
	- [过渡](#过渡)
	- [变形](#变形)
	- [动画](#动画)
	- [css3+html实战页面](css3+html实战页面)
	- [sass常用语法](#sass常用语法)
	- [移动端定宽网页适配方案](#移动端定宽网页适配方案)
		
		
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
```html	
		<h1>This is a heading</h1>
		<h2>This is a heading</h2>
		<h3>This is a heading</h3>
```

<a name="html段落"></a>		

### html段落

- HTML 段落是通过 `<p>` 标签进行定义的。
> 实例

		<p>This is a paragraph.</p>
		<p>This is another paragraph.</p>
		
p元素是块级元素，不能嵌套块级元素，列如p，div，table，ul
	
<a name="文本格式化"></a>		

### 文本格式化
```html	
        <b>定义粗体文本</b>
        <i> 定义斜体文本 </i>
        <del>定义删除文本</del>
        <sup>定义上标字</sup>
        <sub>定义下标字</sub>
``` 
<a name="a标签"></a>    
   
### a标签

```html			
			<!-- 
	    <a href=“URL”> ~ </a>
	    说明：
	    href        定义链接地址
	    title       链接提示信息
	    target      链接打开方式(_blank 新的空白页,_self  当前页,_top(结合iframe使用))
	
	    -->
    
<a href="" title="你好" target="_top">hello world</a>
<a href="tel:电话号码" title="你好" target="_top">拨打号码</a>
<a href="" title="你好" target="_top">hello world</a>
<a href="" title="你好" target="_top">hello world</a>
<a href="" title="你好" name="p元素.html">hello world</a>
<a href="" target=""></a>

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
```

<a name="表格"></a> 

### 表格	    
```html	
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
```
		
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
```html			 
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
```
		
#### 表单常用类型
	
	input：
	
```html		
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
``` 		
	
	下拉框：
	
```html		
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
```	

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

```html
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
```			

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
```html
<audio>
	<source src="media/music.mp3" type="audio/mp3" />
	<source src="media/ogg.ogg" type="audio/ogg" />
	<p>Your browser does not support the audio tag.</p>
	<a href="media/ogg.mp3">点击下载此视频</a>
</audio>
```		
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
```html
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
```
<a name="地图map"></a>

## 地图map
> 高德地图API官网注册账号：拥有自己的key。[地址](https://lbs.amap.com/)

		<!-- 引入工具库 -->
		<script type="text/javascript" src="https://webapi.amap.com/maps?v=1.4.10&key=你自己的key"></script>

```javascript
<script>
    // 传入页面容器id
    var map = new AMap.Map('map', {
        zoom: 18,// 级别
        // 广州
        center: [113.320775, 23.126137], //中心点坐标
        viewMode: '3D'
    });
    var marker1 = new AMap.Marker({
            // 标记
            postion: [113.320775, 23.126137]
        })
        // 添加内容
    map.add(marker1);
    var infoWindow = new AMap.InfoWindow({
    	isCustom: false, // 是否使用自定义窗体
    	content: "<h1>津滨腾跃大厦</h1>", //内容
    	offset: new AMap.Pixel(16, -45) // 偏移
    })
    var onMarkerClick = function(e) {
    	infoWindow.open(map, e.target.getPosition());//打开信息窗体
    }
    marker1.on('click',onMarkerClick);//绑定click事件
</script>
```

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
```html			
			<body style="background-color:#ccccc;">
		
			<h1 style="font-size:12px; color:#ff0000;">这是一个标题</h1>
```

2. 页内引用	

页内引用作为页面中的一个单独部分，由```<style></style>```标签定位在```<head></head>```之中。

	例：
```html		
			<style type="text/css">
				div {
					color: blue;
					font-size: 16px;
				}
			</style>
```
3、外部引入
	
外部样式表是CSS应用中最好的一种形式，它将CSS样式代码单独放在一个外部文件中，再由网页进行调用。
		
		如：	
```html			
		style.css	:
	
		body {
		       background-color:#cccccc;
		}
	
		<link rel="stylesheet" type="text/css" href="style.css" />
```
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

```html
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
```html	
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
```		
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
	
```html		
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
```

* 伪类选择器child系列
	- 选择器：第几个儿子
	- nth里面的括号要传入的1开始的值，可以结合未知数n来使用
	
```html		
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
```
		
**第n个儿子和同类型的才能匹配**

- span无效果
```html	
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
```
		
相反，type类型的没child限制

		ol li:first-of-type {
			font-weight: bold;
		}
		/*第2n个li出现效果*/
		ol li:nth-of-type(2n) {
			letter-spacing: 5px;
		}
```html				
		<ol>
			<li>匹配同类型中的选择器1</li>
			<span>匹配同类型中的选择器2</span>
			<li>匹配同类型中的选择器3</li>
			<li>匹配同类型中的选择器4</li>
			<li>匹配同类型中的选择器5</li>
			<li>匹配同类型中的选择器6</li>
			<li>匹配同类型中的选择器7</li>
		</ol>
```		
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

```html
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
```

事列2：
```html	
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
```html
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
```html
<div id="header">页面头部</div>

<div id="content">
	<div id="left"></div>
	<div id="right"></div>
</div>

<div id="footer">页脚</div>
```
> 并列与嵌套div结构

- ![传统布局样式](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1535351869334&di=34374b8490d6a17c20dfbb119ecd6900&imgtype=0&src=http%3A%2F%2Fimage.codes51.com%2FArticle%2Fimage%2F20160301%2F20160301092939_5974.png)

- 设配IE9以及主流手机端页面布局方式

```html
<header>页面头部
	<nav>导航</nav>
</header>
<section>
	<aside> </aside>
	<article></article>
</section>
<footer>页脚</footer>

```

- ![主流布局样式](http://www.html5jscss.com/pic/htmljscss/html5-layout.jpg)

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

定位：

1、当元素没有设置宽高时，top和bottom，left，right **同时设置** 可以拉伸元素尺寸

2、定位完全脱离文档流（相对定位是不设置这些方位值的时候会占据空间）

3、绝对定位默认body为定位元素，如果父元素有position: relative;就参考这个元素，以此类推，直到body。

4、固定定位 position: fixed;相对于窗口定位

5、z-index：是可以设置定位元素的层级，数值越大越靠上，数值一致时，后来只居上

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
  
实现一个简单的层级效果
```html	
		<style type="text/css">
			div {
				position: absolute;				
			}
			.box1 {
				top: 80px;
				left: 30px;
				width: 100px;
				height: 100px;
				background-color: #000;
			}
			.box2 {
				top: 34px;
				left: 80px;
				width: 200px;
				height: 140px;
				background-color: skyblue;
				z-index: -1;
			}
			.box3 {
				top: 100px;
				left: 100px;
				width: 150px;
				height: 130px;
				background-color: green;
			}
			.box4 {
				position: relative;
				top: 75px;
				left: 160px;
				width: 300px;
				height: 130px;
				background-color: red;
			}
			.box5 {
				position: absolute;
				right: 0;
				bottom: 0;
				width: 50px;
				height: 50px;
				background-color: yellow;
			}
		</style>
			<div class="box1"></div>
			<div class="box2"></div>
			<div class="box3"></div>
			<div class="box4">
				<div class="box5"></div>
			</div>

- 用定位来实现元素的水平垂直居中：
	
		<style type="text/css">
			.boxS {
				width: 300px;
				height: 300px;
				background-color: red;
				position: relative;
			}
			.boxS1 {
				width: 150px;
				height: 150px;
				background-color: skyblue;
				position: absolute;
				top: 50%;
				left: 50%;
				margin-left: -75px;
				margin-top: -75px;
			}
		</style>
			垂直居中时，元素的top和left为50%，同时margin-left和margin-top设置为元素高宽的一般切位负值
			缺点：要清楚元素的宽高
		<div class="boxS">
			<div class="boxS1">111</div>
		</div>
```		
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
```html	
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
```		
		
- border-img圆角边框
```html	
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
```

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

```css
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
```		
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
```css		
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
```
4、 text-shadow

取值：
```html	
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
```
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
```css
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
```

**为什么要清除浮动**

浮动的元素不占据空间，父元素无法用内容来撑开
```css
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
```			
**[返回目录](#zore)**

<a name="过渡"><a/>

### 过渡transition
				
Internet Explorer 10、Firefox、Chrome 以及 Opera 支持 transition 属性。

Safari 需要前缀 -webkit-。

注释：Internet Explorer 9 以及更早的版本，不支持 transition 属性。

注释：Chrome 25 以及更早的版本，需要前缀 -webkit-。

要实现这一点，必须规定两项内容：

规定您希望把效果添加到哪个 CSS 属性上

规定效果的时长

转换属性：

属性	描述	CSS

- transition	简写属性，用于在一个属性中设置四个过渡属性。	

- transition-property	规定应用过渡的 CSS 属性的名称。	

- transition-duration	定义过渡效果花费的时间。默认是 0。	

- transition-timing-function	规定过渡效果的时间曲线。默认是 "ease"。
	
		linear：匀速
		ease-in：加速
		ease-out：减速
		ease-in-out：先加速后减速
- 贝塞尔曲线:	http://cubic-bezier.com	
	
![](http://dtop.powereasy.net/UploadFiles/Article/20141/201401031725140963.png)

- transition-delay	规定过渡效果何时开始。默认是 0。

- 也可以结合起来写： transition：属性 时间 动画 延迟

列如：
```css	
		div {
				width: 130px;
				height: 50px;
				line-height: 50px;
				text-align: center;
				background: skyblue;color: #fff;	
				border: 1px solid skyblue;	
				cursor: pointer;
				transition: background 500ms;
				transition: background 500ms,color 2s;
				/*all 所以属性都引用过渡*/
				transition: all 2s;
				/*运动的速度,linear匀速*/
				transition: all 2s linear  color,2s;
				/*width变为33px*/
				transition: width 2s linear  color,2s;
			}
			div:hover {
				width: 330px;
				background: #fff ;
				color:skyblue;	
			}
		
		<div class="link">css教程</div>
		<div class="link">css教程</div>
		<div class="link">css教程</div>
		<div class="link">css教程</div>
```
<a name="变形"><a/>

### 变形transform

CSS3 转换

	通过 CSS3 转换，我们能够对元素进行移动、缩放、转动、拉长或拉伸
	Internet Explorer 10、Firefox 以及 Opera 支持 transform 属性。

	Chrome 和 Safari 需要前缀 -webkit-。

	注释：Internet Explorer 9 需要前缀 -ms-。

2D 转换
在本章中，您将学到如下 2D 转换方法：
```css	
		matrix()：以一个含六值的(a,b,c,d,e,f)变换矩阵的形式指定一个2D变换，相当于直接应用一个[a,b,c,d,e,f]变换矩阵
		translate()：指定对象的2D translation（2D平移）。第一个参数对应X轴，第二个参数对应Y轴。如果第二个参数未提供，则默认值为0
		translatex()：指定对象X轴（水平方向）的平移
		translatey()：指定对象Y轴（垂直方向）的平移
		rotate()：指定对象的2D rotation（2D旋转），需先有 <' transform-origin '> 属性的定义
		scale()：指定对象的2D scale（2D缩放）。第一个参数对应X轴，第二个参数对应Y轴。如果第二个参数未提供，则默认取第一个参数的值
		scalex()：指定对象X轴的（水平方向）缩放
		scaley()：指定对象Y轴的（垂直方向）缩放
		skew()：指定对象skew transformation（斜切扭曲）。第一个参数对应X轴，第二个参数对应Y轴。如果第二个参数未提供，则默认值为0
		skewx()：指定对象X轴的（水平方向）扭曲
		skewy()：指定对象Y轴的（垂直方向）扭曲
		
		div {
			display: inline-block;
			width: 100px;
			height: 100px;
			background: red;
			transform: translate(50px, 100px);
			/*-ms-transform: translate(50px, 100px);*/
		}
		div
			{
			/* rotate(30deg) 把元素顺时针旋转 30 度。*/
			transform: rotate(30deg);
			-ms-transform: rotate(30deg);		/* IE 9 */
			-webkit-transform: rotate(30deg);	/* Safari and Chrome */
			-o-transform: rotate(30deg);		/* Opera */
			-moz-transform: rotate(30deg);		/* Firefox */
			}
			div
				{
					/* scale(2,4) 把宽度转换为原始尺寸的 2 倍，把高度转换为原始高度的 4 倍。*/
				transform: scale(2,4);
				-ms-transform: scale(2,4);	/* IE 9 */
				-webkit-transform: scale(2,4);	/* Safari 和 Chrome */
				-o-transform: scale(2,4);	/* Opera */
				-moz-transform: scale(2,4);	/* Firefox */
				}
				div
					{
					transform: skew(30deg,20deg);
					-ms-transform: skew(30deg,20deg);	/* IE 9 */
					-webkit-transform: skew(30deg,20deg);	/* Safari and Chrome */
					-o-transform: skew(30deg,20deg);	/* Opera */
					-moz-transform: skew(30deg,20deg);	/* Firefox */
					}
					div
						{
						transform:matrix(0.866,0.5,-0.5,0.866,0,0);
						-ms-transform:matrix(0.866,0.5,-0.5,0.866,0,0);		/* IE 9 */
						-moz-transform:matrix(0.866,0.5,-0.5,0.866,0,0);	/* Firefox */
						-webkit-transform:matrix(0.866,0.5,-0.5,0.866,0,0);	/* Safari and Chrome */
						-o-transform:matrix(0.866,0.5,-0.5,0.866,0,0);		/* Opera */
						}
```
3D Transform Functions：

网页中的3d坐标，如下如：

![](http://html5book.bluej.cn/static/images/css/3d/3d_1.png)

> 秘诀：伸出右手，大拇指对着自己，食指对地，中指对着你面朝方向的右边。

![](http://html5book.bluej.cn/static/images/css/3d/3d_2.jpg)

- 大拇指代表Z轴，食指代表Y轴，中指代表X轴，指甲所在端就是该轴的正方向
- 当你要判断物体旋转的时候，哪个方向是正，哪个方向是负？
- 只需要把对应表示该轴的手指指向自己，顺时针方向则是正方形，逆时针方向就是负方向

```css
		matrix3d()：以一个4x4矩阵的形式指定一个3D变换
		translate3d()：指定对象的3D位移。第1个参数对应X轴，第2个参数对应Y轴，第3个参数对应Z轴，参数不允许省略
		translatez()：指定对象Z轴的平移
		rotate3d()：指定对象的3D旋转角度，其中前3个参数分别表示旋转的方向x,y,z，第4个参数表示旋转的角度，参数不允许省略
		rotatex()：指定对象在x轴上的旋转角度
		rotatey()：指定对象在y轴上的旋转角度
		rotatez()：指定对象在z轴上的旋转角度
		scale3d()：指定对象的3D缩放。第1个参数对应X轴，第2个参数对应Y轴，第3个参数对应Z轴，参数不允许省略
		scalez()：指定对象的z轴缩放
		perspective()：指定透视距离
		
		div {
			margin: 0 auto;
			width: 100px;
			height: 100px;
			background: red;
			transform: rotateX(30deg);
			-webkit-transform: rotateX(120deg);	/* Safari 和 Chrome */
			-moz-transform: rotateX(120deg);	/* Firefox */
		}
		#div1 {
			margin: 0 auto;
			width: 100px;
			height: 100px;
			background: red;
			transform: rotateY(120deg);
			transform-origin: 30px 30px;
			-webkit-transform: rotateY(120deg);	/* Safari 和 Chrome */
			-moz-transform: rotateY(120deg);	/* Firefox */
		}
```		
**利用过渡和变形实现css奇妙图形**

**心形图**

![](https://images2018.cnblogs.com/blog/755438/201803/755438-20180329214731883-314703565.png)

实现原理：利用伪类和旋转角度实现
```css
		<div class="LovePic">
			<h1>heart Shaped</h1>
		</div>
		
		.LovePic {
				position: absolute;
				/*水平垂直居中*/
				top: 50%;
				left: 50%;
				/*旋转45度角*/
				transform: translate(-50%, -50%) rotate(45deg);
				width: 340px;
				line-height: 340px;
				background: rgba(255, 20, 147, .85);
				color: #FFFFFF;
				text-align: center;				
			}
			.LovePic h1 {
				font-size: 40px;
				position: relative;
				z-index: 10;
				transform:rotate(-45deg);
			}
			.LovePic::before, .LovePic::after {
				position: absolute;
				content: '';
				top: 0;
				left: -170px;
				width: 340px;
				height: 340px;
				background: rgb(255, 20, 147);
				border-radius: 50%;
			}
			.LovePic::before {				
				left: 0;
				top: -170px;	
			}
```			
**气泡三角形**

![](https://images2018.cnblogs.com/blog/755438/201803/755438-20180329215026949-162086909.png)
```css		
		<div class="trangle">
			<h1>heart Shaped</h1>
		</div>
		
		.trangle {
				position: absolute;
				top: 50%;
				left: 50%;
				transform: translate(-50%, -50%);
				width: 260px;
				padding: 60px 20px;
				background: #00aabb;
				text-align: center;
				border-radius: 10px;
			}
			
			.trangle h1 {
				color: #FFFFFF;
				font-size: 20px;
			}
			/*左边*/
			.trangle::after {
				content: '';
			    position: absolute;
			    left: 0;
			    border-top: 30px solid transparent;
				border-right: 60px solid #00aabb;
			    margin-left: -50px;
			}
			/*底部*/
			.trangle::after {
				content: '';
			    position: absolute;
			    bottom: -54px;
				border-top: 74px solid #00aabb;
				border-right: 50px solid transparent;
			    margin-left: 50px;
			}
```
**右边菜单栏过渡效果**

![](http://edu.bluej.cn/public/uploads/20180427/20180427154150Honeycam.gif)

实现原理：利用transition和tranform实现
```css
* {
		margin: 0;
		padding: 0;
		list-style: none;
	}
	a {
		text-decoration: none;
	}
	.box {
		position: absolute;
		text-align: center;
		right: -160px;
		width: 400px;
	}
	.box li {
		color: blue;
		padding-left: 200px;
		text-align: left;
		font-size: 0;
		margin-bottom: 4px;
	}
	.box li:nth-child(1) {
		transition: transform .3s linear;
	}
	.box li:nth-child(2) {
		transition: transform .3s linear .1s;
	}
	.box li:nth-child(3) {
		transition: transform .3s linear .2s;
	}
	.box li:nth-child(4) {
		transition: transform .3s linear .3s;
	}
	.box li:nth-child(5) {
		transition: transform .3s linear .4s;
	}
	.box li:nth-child(6) {
		transition: transform .3s linear .5s;
	}
	.box li:nth-child(7) {
		transition: transform .3s linear .6s;
	}
	.box li:nth-child(8) {
		transition: transform .3s linear .7s;
	}
	.box li:nth-child(9) {
		transition: transform .3s linear .8s;
	}
	.box li:nth-child(10) {
		transition: transform .3s linear .9s;
	}
	.box li:nth-child(11) {
		transition: transform .3s linear 1s;
	}
	.box li span {
		width: 20px;
		height: 20px;
		display: inline-block;
		text-align: center;				
		font-size: 18px;
		color: #fff;
		background: #0000FF;
		padding: 10px;
		cursor: pointer;
		vertical-align: bottom;
	}
	.box:hover li{
		transform: translateX(-160px);
	}
	.box li span:hover {
		background: greenyellow;
	}
	.box li a {
		display: inline-block;
		font-size: 16px;
		width: 150px;
		padding-left: 10px;
		vertical-align: bottom;
		border-bottom: 1px solid #ccc;
	}
	.box li a:hover {			
		background: skyblue;
	}
	
	<div class="box">
	<ul>
		<li>
			<span>1</span> <a href="">站长素材</a>
		</li>
		<li>
			<span>2</span><a href="">书签切换</a> 
		</li>
		<li>
			<span>3</span><a href="">幻灯片</a> 
		</li>
		<li>
			<span>4</span> <a href="">图片滚动正</a>
		</li>
		<li>
			<span>5</span><a href="">图片滚动上</a> 
		</li>
		<li>
			<span>6</span><a href="">图片无线滚动</a> 
		</li>
		<li>
			<span>7</span> <a href="">文字滚动</a>
		</li>
		<li>
			<span>8</span> <a href="">文字无缝滚动</a>
		</li>
		<li>
			<span>9</span><a href="">其他基础效果</a> 
		</li>
		<li>
			<span>10</span> <a href="">transition实现</a>
		</li>
		<li>
			<span>11</span><a href="">正则表达式</a> 
		</li>
	</ul>
</div>
```
**筛子立体图效果**

![](https://images2015.cnblogs.com/blog/967327/201610/967327-20161007183013192-1320367994.png)
```css
.shaizai {
		width: 100px;
		height: 100px;
		line-height: 100px;
		margin: 100px;
		text-align: center;
		/*3d模式*/
		transform-style: preserve-3d;
		position: relative;
		transition: all 10s;
	}
	.shaizai:hover {
		transform: rotateX(360deg) rotateY(360deg);
	}
	.side {
		width: 100%;
		height: 100%;
		position: absolute;
		top: 0;
		left: 0;
		opacity: .5;
	}
	.front {
		transform: translateZ(50px);
		background: red;
	}
	.back {
		transform: rotateY(180deg) translateZ(50px) ;
		background: skyblue;
	}
	.left {
		transform:rotateY(90deg) translateZ(50px) ;
		background: green;
	}
	.right {
		transform:rotateY(-90deg) translateZ(50px) ;
		background: orange;
	}
	.top {
		transform:rotateX(-90deg) translateZ(50px) ;
		background: pink;
	}
	.bottom {
		transform:rotateX(90deg) translateZ(50px) ;
		background: #000;
	}
	
<div class="shaizai">
	<div class="side top">1</div>
	<div class="side bottom">2</div>
	<div class="side left">3</div>
	<div class="side right">4</div>
	<div class="side front">5</div>
	<div class="side back">6</div>
</div>
```

**[返回目录](#zore)**
<a name="动画"></a>
### 动画animation

| 属性           | 版本         | 继承        | 描述  |
| -------------------------   | ----------  | :----------:  |
| animation			| CSS3   | 无  | 复合属性。检索或设置对象所应用的动画特效 |
| animation-name		| CSS3   | 无  | 检索或设置对象所应用的动画名称 |
| animation-duration 		| CSS3   | 无  | 检索或设置对象动画的持续时间 |
| animation-timing-function     | CSS3   | 无   | 检索或设置对象动画的过渡类型 |
| animation-delay 		| CSS3   | 无    | 检索或设置对象动画延迟的时间 |
| animation-iteration-count     | CSS3   | 无 	| 检索或设置对象动画的循环次数 |
| animation-direction 		| CSS3   | 无   | 检索或设置对象动画在循环中是否反向运动 |
| animation-play-state 		| CSS3   | 无     | 检索或设置对象动画的状态 |
| animation-fill-mode 		| CSS3   | 无   | 检索或设置对象动画时间之外的状态 |

**前5个与transition属性基本一致**
```html
<style type="text/css">
	.ball {
		width: 100px;
		height: 100px;
		border-radius: 50%;
		background: #0000FF;
		animation: run 3s linear 1 alternate;
		/*animation-fill-mode: forwards;*/
	}
	@keyframes run{
		0%{
			
		}
		25%{
			transform: translateX(200px);
		}
		50%{
			transform:translateX(200px) translateY(200px);
		}
		75%{
			transform: translateX(0) translateY(200px);
		}
		100%{
			transform:translateY(200PX);
		}
	}
	.ball:hover {
		animation-play-state: paused;
	}
</style>
</head>
<body>
<!--
	animation-iteration-count:（次数） infinite 无线循环
	
	animation-direction：
		取值：
		normal：正常方向
		
		reverse：反方向运行
		
		alternate：动画先正常运行再反方向运行，并持续交替运行
		
		alternate-reverse：动画先反运行再正方向运行，并持续交替运行
		
	animation-play-state：播放状态
		默认：running
		展停：paused
		
	animation-fill-mode：检索或设置对象动画时间之外的状态
		none：默认值。不设置对象动画之外的状态
		
		forwards：设置对象状态为动画结束时的状态
		
		backwards：设置对象状态为动画开始时的状态
		
		both：设置对象状态为动画结束或开始的状态
-->
<div class="ball">
	
</div>
```

**动画库**

[animation.css](https://daneden.github.io/animate.css/)

**[返回目录](#zore)**

<a name="css3+html实战页面"><a/>

[css3+html实战页面演示](https://struggle-wjf.gitee.io/luban_shop/)

<a name="sass常用语法"><a/>

## 1、什么是sass

- SASS是一种CSS的开发工具，提供了许多便利的写法，大大节省了设计者的时间，使得CSS的开发，变得简单和可维护。

### 2、sass安装

> 因为sass依赖于ruby环境，所以装sass之前先确认装了ruby。先导[官网下载个ruby](https://rubyinstaller.org/downloads/) 在安装的时候，请勾选Add Ruby executables to your PATH这个选项，添加环境变量，不然以后使用编译软件的时候会提示找不到ruby环境

![](http://html5book.bluej.cn/static/images/css/sass1.png)

- 安装完ruby之后，在开始菜单中，找到刚才我们安装的ruby，打开Start Command Prompt with Ruby

![](http://html5book.bluej.cn/static/images/css/ruby-cmd.png)

- 然后直接在命令行中输入

		npm install sass
		
- 按回车键确认，等待一段时间就会提示你sass安装成功。最近因为墙的比较厉害，如果你没有安装成功，可以尝试下面方法，或参考下面的淘宝的RubyGems镜像安装sass，如果成功则忽略。

		gem source --remove https://rubygems.org
		gem source --add http://rubygems.org
		gem sources            //查看一下是否更新源成功

- 如果要安装beta版本的，可以在命令行中输入

		gem install sass --pre
		
- 你还可以从sass的Git repository来安装，git的命令行为

		git clone git://github.com/nex3/sass.git
		cd sass
		rake install
- 升级sass版本的命令行为

		gem update sass
- 查看sass版本的命令行为

		sass -v
		
- 你也可以运行帮助命令行来查看你需要的命令

		sass -h
		
##### 3.淘宝RubyGems镜像安装 sass(安装失败请继续看)由于国内网络原因（你懂的），导致 rubygems.org 存放在 Amazon S3 上面的资源文件间歇性连接失败。这时候我们可以通过gem sources命令来配置源，先移除默认的https://rubygems.org源，然后添加淘宝的源https://ruby.taobao.org/，然后查看下当前使用的源是哪个

- 关于常用gem source命令可参看：常用的gem source

		$ gem sources --remove https://rubygems.org/
		$ gem sources -a https://ruby.taobao.org/
		$ gem sources -l
		*** CURRENT SOURCES ***

		https://ruby.taobao.org

## 请确保只有 ruby.taobao.org,如果是淘宝的，则表示可以输入sass安装命令了。

		$ gem install sass
安装成功截图： ![](http://html5book.bluej.cn/static/images/css/sass2.png)

### 基础入门

#### 1.变量
sass中可以定义变量，方便统一修改和维护。
```css
sass代码：

$blue : #1875e7;　
div {
　color : $blue;
}
生成的css 代码：

div {
　color : #1875e7;
}
如果变量需要镶嵌在字符串之中，就必须需要写在#{}之中。

$side : left;
　　.rounded {
　　　　border-#{$side}-radius: 5px;
　　}
```

#### 2、嵌套

- sass可以进行选择器的嵌套，表示层级关系，看起来很优雅整齐。

```css
sass代码：

nav {
  ul {
    margin: 0;
  }

  li { display: inline-block; }

  a {
    display: block;
  }
}
生成的css代码：

nav ul {
  margin: 0;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
}
属性也可以嵌套，比如border-color属性，可以写成：

p {
　　　border: {
　　　　　color: red;
　　　}
　}
注意，border后面必须加上冒号。 在嵌套的代码块内，可以使用&引用父元素。比如a:hover伪类，可以写成：

a {
　　　&:hover { color: #ffb3ff; }
　}
```

### 3.导入
- sass中如导入其他sass文件，最后编译为一个css文件，优于纯css的@import。其中注意的是如果sass文件的名字以“_”开头，则不会被编译成css文件
- _reset.scss文件：
```css
html,
body,
ul,
ol {
   margin: 0;
  padding: 0;
}
base.scss文件：
@import 'reset';

body {
  font-size: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
最终生成的css:
html, body, ul, ol {
  margin: 0;
  padding: 0;
}

body {
  background-color: #efefef;
  font-size: 100% Helvetica, sans-serif;
}


```

### 4.mixin（可以重用的代码块）
```css
@mixin left {
　　　　float: left;
　　　　margin-left: 10px;
　　}
使用@include命令，调用这个mixin。

div {
　　　　@include left;
　　}
mixin的强大之处，在于可以指定参数和缺省值。

@mixin left($value: 10px) {
　　　float: left;
　　　margin-right: $value;
　}
```

### 5.扩展/继承
- sass可通过@extend来实现代码组合声明，使代码更加优越简洁。
```css
sass:

.message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  @extend .message;
  border-color: green;
}

.error {
  @extend .message;
  border-color: red;
}

.warning {
  @extend .message;
  border-color: yellow;
}
生成的css:

.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
``` 
### 6.运算
- sass可进行简单的加减乘除运算等
```css
sass:

$var:100px;
div {
　　　　margin: (14px/2);
　　　　top: 50px + 100px;
　　　　right: $var * 0.5;
　　}
生成的css:

div {
　　　　margin: 7px;
　　　　top: 150px;
　　　　right: 50px;
　　}
```

### 7. 自定义函数
- SASS允许用户编写自己的函数。
```css
　　@function double($n) {
　　　　@return $n * 2;
　　}
　　#sidebar {
　　　　width: double(5px);
　　}
生成的css:

#sidebar {
　　　　width: 10px;
　　}
如果要返回字符串，可以这样写

@function myurl($url){
    @return "../#{$url}";   //返回一个拼接的新地址
}
body{
    background-image: url(myurl(images/bg.jpg)); 
}
生成的css:

body {
  background-image: url("../images/bg.jpg"); }
```
<a name="移动端定宽网页适配方案"><a/>
## viewport快速学习指南

### viewport简介

- 没错，就是viewport特性，一个移动专属的meta值，用于定义视口的各种行为。

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

- 以iPhone4S为例，会在其320px②的visual viewport上，创建一个宽980px的layout viewport，于是用户可以在visual viewport中拖动或者缩放网页，来获得良好的浏览效果；布局视口用来配合CSS渲染布局，当我们定义一个容器的宽度为100%时，这个容器的实际宽度是980px而不是320px，通过这种方式大部分网页就能以缩放的形式正常显示在手机屏幕上了。

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
* 如果想页面默认以某个比例放大或者缩小然后呈现给用户，那么可以通过定义initial-scale来完成。

> initial-scale用于指定页面的初始缩放比例，假定你这样定义：

```html
<meta name="viewport" content="initial-scale=2" />
```
- 那么用户将会看到2倍大小的页面内容。

- 在说width的时候，我们说到initial-scale也能实现ideal viewport，是的，你只需要这样做，也可以得到完美视口：

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
- 如果你不想页面被放大或者缩小，通过定义user-scalable来约束用户是否可以通过手势对页面进行缩放即可。

该属性的默认值为yes，即可被缩放（如果使用默认值，该属性可以不定义）；当然，如果你的应用不打算让用户拥有缩放权限，可以将该值设置为no。

- 使用方法如下：

```html
<meta name="viewport" content="user-scalable=no" />
```
**移动端物理像素 px rem em像素单位**
- 选择：

		em是相对父亲字体大小的单位
		rem相对根节点字体大小单位（root rem）
		总结：屏幕实际实际接收px，rem和em是相对单位，按照一定的比例缩放
		
- 移动端设配最好采用rem像素单位，根据根节点的字体大小变化而变化

- JavaScript脚本自动设配移动端

```javascript
 document.body.style.height = window.innerHeight + "px";
    
    /*动态改变根元素字体大小*/
    function recalc() {
    	// 客户端的宽度
        var clientWidth = document.documentElement.clientWidth;
        if(!clientWidth) return;
        document.documentElement.style.fontSize = 40 * (clientWidth / 750) + 'px';
        // 字体大小   = 1个rem单位表示多少个像素（设备的宽度   /设计宽度）
    }

    function initRecalc() {
        recalc();
        // if(浏览器支持横竖屏切换的事件){横竖屏事件}else{ resize事件 }
        var resizeEvt = 'osrientationchange' in window ? 'orientationchange' : 'resize';
        if(!document.addEventListener) return;
        window.addEventListener(resizeEvt, recalc, false);
        document.addEventListener('DOMContentLoaded', recalc, false);
    }
                
    initRecalc();
```
[项目实战- 移动端](https://struggle-wjf.gitee.io/shop_mobile/)

默认宽度375px，iPhone6