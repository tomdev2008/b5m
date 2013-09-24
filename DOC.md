B5M.WEB前端开发规范
===


## 一、规范目的与标准

### 1.1 规范目的
统一网站前端目录结构，统一书写规范，统一开发习惯，为提高团队协作效率，便于程序开发人员添加功能及前端后期的优化维护。

### 1.2 HTML页面兼容性标准

<table>
<tbody><tr><td> </td><td> WinXP </td><td> Win7 </td><td> OS X 
</td></tr><tr><td> IE9 </td><td> B  </td><td> B </td><td> 
</td></tr><tr><td> IE8 </td><td> A  </td><td> A </td><td> 
</td></tr><tr><td> IE7 </td><td> B  </td><td> B </td><td> 
</td></tr><tr><td> IE6 </td><td> B  </td><td> B </td><td> 
</td></tr><tr><td> Chrome </td><td> A  </td><td> A </td><td> A 
</td></tr><tr><td> Firefox </td><td> A </td><td> A </td><td> A 
</td></tr><tr><td> Safari </td><td> B  </td><td> B </td><td> B 
</td></tr></tbody></table>

*  A级－交互和视觉完全符全设计的要求
*  B级－视觉上允许有所差异，但不破坏页面的整体效果
*  C级－可忽略设计上的细节，但不防碍使用

数据参考地址：http://tongji.baidu.com/data/browser


     
## 二、命名规则

### 2.1 文件夹命名

要求： 
  
1. 文件夹名称统一由小写的英文字母、数字、下划线、英文句号组合而成，不允许使用汉字、空格、特殊字符  
  
2. 文件夹名称要能直观的体现当前文件夹的项目或版本  

    例：  
	帮5买   www  
	韩国馆  korea    
	淘物价  tao    
	        tao_1.0  淘特价1.0版本  


### 2.2 文件命名

要求：  

1. 文件名称统一由小写的英文字母、数字、下划线组合而成，不允许使用汉字、空格、特殊字符  

2. 文件名称要能直观的体现当前文件的文件类型、项目、内容性质  

	例：       
	HTML文件：项目名/内容性质.html    
		淘特价首页	/tao/index.html  
		淘持价列表	/tao/list.html  

	CSS文件：项目名称.css  
		公共样式	common.css  
		淘特价样式	tao.css  
		帮5游样式	you.css   

	JS文件：公共框架：框架名+版本.js (必需是压缩版)  
		Jquery公共库	 jquery-1.9.1.min.js  
	  	Jquery扩展	 jquery.easing.1.3.js  
	  	注：所有基于jquery的扩展都必需使用官网的命名，不允许修改  
	  	所有引用的第三方扩展需同团队成员共同讨论决定    

  	手写文件：内容性质.js  
  	选项卡功能	tab.js  
  	消息弹窗	message.js  


### 2.3 变量命名

要求：  
1. 变量名称统一由小写的英文字母、下划线、中划线组合而成，且符合语义，避免使用中文拼音 
2. id 、class必需由小写字母、中划线组成  
3. 为JavaScript预留钩子命名必须以 J_开头，如 J_tab  
4. JavaScript公共变量由大家字母、下划线组成，如 var USER_NAME  



## 三、网站前端架构规则

### 3.1 WEB静态资源CDN地址
http://staticcdn.b5m.com/  


###3.2 目录结构

	.  
	└──static									--- 存放前端代码  
	    ├── html
	    	├── common	 						
	    	├── tao  
	    	├── you	  							
	    	├── header.html  
	    	└── footer.html  
	    ├── css              					--- 样式目录  
			├── common  
				├── common.css 					--- 公共样式，如reset / header / footer  
				└── common.min.css	  
			├── tao  
				├── index.css  
				└── style.css  
			└── you  
				└── style.css     	
	    ├── images  
	    	├── common 							--- 图片目录  
	    	├── tao  
			└── you  
		├── scripts              				--- 脚本目录  
			├── common  
				└── jquery-1.9.1.min.js	  
			├── tao  
				├── index.js  
				└── down-list.js  
			└── you   
	    └── public								--- 其它静态资源 xml、swf  



## 四、HTML书写规范

### 4.1 基本要求
1. 所有编码均遵循xhtml标准，标签、属性、属性命名必须由小写字母及下划线数字组成(特殊情况除外)， 且所有标签必须闭合，包括 br (&lt;br /&gt;), hr(&lt;hr /&gt;)等；属性值必须用双引号包括；

2. 充分利用无兼容性问题的html自身标签，比如span、em、strong、optgroup、label等等；需要为html元素添加自定义属性的时候，首先要考虑下有没有默认的已有的合适标签去设置，如果没有，可以使用须以"data-"为前缀来添加自定义属性，避免使用"data:"等其他命名方式；

3. 语义化html，如标题根据重要性用h*(同一页面只能有一个h1)，段落标记用p，列表用ul，内联元素中不可嵌套块级元素；

4. 重要图片必须加上alt属性

5. 给区块代码及重要功能(比如循环)加上注释，方便后台添加功能；

6. 为JavaScript预留钩子class名，禁止为其写样式，如J_tab

7. 特殊符号使用：尽可能使用代码替代: 比如 <(&lt;)、>(&gt;)、空格(&nbsp;)等等；

8. 必须为含有描述性表单元素(input，textarea)添加label
```html
<p>
	<label for="name">姓 名: </label>
	<input type="text" id="name" />
</p>
```


### 4.2 书写规则
1. 使用HTML5标准文档结构  
```html
<!doctype html>
<html>
	<head>
		<meta charset="utf-8">
		<title>标题</title>
		<meta name="keywords" content="关键字" />
		<meta name="description" content="页面描述" />
		<link rel="stylesheet" href="..." />
		<script src="..."></script>
	</head>
	<body>

	</body>
</html>
```

2. 设置文本为UTF-8  
```html
<meta charset="utf-8" />
```

3. 设置 keywords  
```html
<meta name="keywords" content="关键字" />
```

4. 设置 description  
```html
<meta name="keywords" content="页面描述" />
```

5. 设置外链样式  
```html
<link rel="stylesheet" href="..." />
```

6. 设置JavaScript地址  
```html
<script src="..."></script>
```  
注：除非特殊需要，可以考虑将JavaScript放置页面底部

7. 考虑运用DNS预获取（dns-prefetch）  
```html
<link rel=”dns-prefetch” href=”http://cdn.bang5mai.com”/>
```

8. 如为解决 IE 6 兼容性问题，要单独引用CSS  
```html
<!--[if IE 6]>
	<link rel="stylesheet" href="..." />
<![endif]-->
```


## 五、CSS书写规范

### 5.1 所有CSS标签、属性必须由小写字母、数字、中划线组合

### 5.2 非特殊情况下，样式文件必须外链至`<head>`…`</head>`之间，写法如下：
```html
<link rel="stylesheet" href="..." />
```
如遇特殊情况可使用：`<style>`...`</style>` ，严重杜绝在元素标签里写样式（特殊情况除外）

### 5.3 尽量避免使用Filter，避免 CSS 表达式

### 5.4 单行形式适用于直接写在页面中和长文件的情况。声明写在一行。
```css
.selector { property:value;property:value; }
```

### 5.5 CSS3兼容书写形式和对齐方式
```css
.selector { 
	-webkit-box-shadow: 0 0 5px rgba(200, 200,200, 0.8);
    -moz-box-shadow: 0 0 5px rgba(200, 200,200, 0.8);
	box-shadow: 0 0 5px rgba(200, 200,200, 0.8);
}
```

### 5.6 CSS3中逗号分隔的长属性值
```css
.selector {
    box-shadow:
        1px 1px 1px #000,
        2px 2px 1px 1px #ccc inset;
    background-image:
        linear-gradient(#fff, #ccc),
        linear-gradient(#f3c, #4ec);
}
```

### 5.7 多个(>2)selector每个占一行
```css
.selector1,
.selector2,
.selector3 { ... }
```

### 5.8 规则声明的顺序：定位、盒模型（width/height/padding/border/margin）、行高、字体/字号/颜色、背景、CSS3效果等

### 5.9 避免滥用CSS Hack
区别属性：
<table style="margin-left:60px;">
<tbody><tr><td> IE6 </td><td style="text-align:left;"> _property:value 
</td></tr><tr><td> IE6/7 </td><td style="text-align:left;"> *property:value 
</td></tr><tr><td> IE6/7/8/9 </td><td style="text-align:left;"> property:value\9 
</td></tr></tbody></table>
区别规则：
<table style="margin-left:60px;">
<tbody><tr><td> IE6 </td><td style="text-align:left;"> * html selector { ... } 
</td></tr><tr><td> IE7 </td><td style="text-align:left;"> *:first-child+html selector { ... } 
</td></tr><tr><td> 非IE6 </td><td style="text-align:left;"> html&gt;body selector { ... } 
</td></tr><tr><td> firefox only </td><td style="text-align:left;"> @-moz-document url-prefix() { ... } 
</td></tr><tr><td> saf3+/chrome1+ </td><td style="text-align:left;"> @media all and (-webkit-min-device-pixel-ratio:0) { ... } 
</td></tr><tr><td> opera only </td><td style="text-align:left;"> @media all and (-webkit-min-device-pixel-ratio:10000),not all and (-webkit-min-device-pixel-ratio:0) { ... } 
</td></tr><tr><td> iPhone/mobile webkit </td><td style="text-align:left;"> @media screen and (max-device-width: 480px) { ... } 
</td></tr></tbody></table>
注意：SCSS会自动转换一些不标准CSS写法，会破坏CSS Hack。

### 5.10 CSS reset内容
	body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,button,textarea,p,blockquote,th,td{margin:0;padding:0}fieldset,img{border:0}:focus{outline:0}address,caption,cite,code,dfn,em,strong,th,var,optgroup{font-style:normal;font-weight:normal}h1,h2,h3,h4,h5,h6{font-size:100%;font-weight:normal}abbr,acronym{border:0;font-variant:normal}input,button,textarea,select,optgroup,option{font-family:inherit;font-size:inherit;font-style:inherit;font-weight:inherit}code,kbd,samp,tt{font-size:100%}input,button,textarea,select{*font-size:100%}ol,ul{list-style:none}table{border-collapse:collapse;border-spacing:0}caption,th{text-align:left}sup,sub{font-size:100%;vertical-align:baseline}:link,:visited,ins{text-decoration:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:'';content:none}

### 5.11 默认body设置
`body{font: 12px/1.5 tahoma,arial,\5b8b\4f53; background: #fff;}`



## 六、JavaScript书写规范

### 6.1 变量、对象属性/方法

1. 变量或命名表达式加上var 关键字
2. 以驼峰格式命名，如var myName
3. 以类型、含义和使用范围来命名，尽量不要使用data 这样范围太广的单词
4. 私有变量、方法、属性约定以下划线开

### 6.2 常量

使用大写加下划线的组合命名。如：`var MY_APPNAME`

### 6.3 以分号结尾

### 6.4 空格与换行

在关键字、运算符等前后加空格，起始大括号后换行，便于阅读。如:
```javascript 
for (var key in obj) {
	if (_.has(obj, key)) {
		if (iterator.call(context, obj[key], key, obj) === breaker)
		return;
	}
}
```

### 6.5 函数声明与函数表达式

在函数块内，推荐使用表达式。如：`var getName = function(){}`，而不是`function getName(){}`

### 6.6 字面量与对象

使用字面量定义而非对象定义。如`var appname = [1,2]` 而非`var appname = new Array(1,2);`

### 6.7 逻辑判断

使用三个等于号的严格判断，两个等于号会转义类型后判断

### 6.8 原型

1. 自定义对象中的工具函数、多处使用的方法或属性、需要继承的方法或属性添加到原型链中
2. 禁止给基本数据类型添加原型，也不允许修改

### 6.9 Eval 和with，如果不是转义json、模块框架开发，不要使用

### 6.10 注释和jsDoc

1. 变量、对象属性根据上下文添加单行注释
2. 顶层/文件注释用于告诉不熟悉这段代码的读者这个文件中包含哪些东西. 应该提供文件的大体内容, 它的作者, 依赖关系和兼容性信息
3. 每个类的定义都要附带一份注释, 描述类的功能和用法
4. 方法与函数的注释提供参数说明，返回值，功能

### 6.11 jQuery 与ajax

1. jQuery 对象使用前缀$，如：`var $myName = $(‘#J_myName’)`
2. Html 中id 增加前缀J_，来标识此id 是给js 使用的
3. Ajax 需增加error、complate、loading 以及对于ui上的反馈
4. 多个子元素的事件使用委托
5. Ajax 请求中，查询数据库/缓存/输出等使用get 请求，增、删、改使用post 请求。格式为json



## 七、其它标准

### 7.1 尽可能的使用png图片
### 7.2 全站引入通用样式
```html
<link rel="stylesheet" href="http://staticcdn.b5m.com/static/css/common/common.css" />
```

### 7.3 全站页面宽度 980px （www搜索结果页除外）



## 八、命名推荐

### 8.1 通用命名
	页面外围控制整体布局宽度：wrap
	头：header
	内容：content/container
	尾：footer
	导航：nav
	侧栏：sidebar
	栏目：column  
	左右中：left right center
	登录条：loginbar
	标志：logo
	广告：banner
	页面主体：main
	热点：hot
	新闻：news
	下载：download
	子导航：subnav
	菜单：menu
	子菜单：submenu
	搜索：search
	友情链接：friendlink
	页脚：footer
	版权：copyright
	滚动：scroll
	内容：content
	标签页：tab
	文章列表：list
	提示信息：msg
	小技巧：tips
	栏目标题：title
	加入：joinus
	指南：guild
	服务：service
	注册：regsiter
	状态：status
	投票：vote
	合作伙伴：partner

### 8.2 导航类
	导航：nav
	主导航：mainbav
	子导航：subnav
	顶导航：topnav
	边导航：sidebar
	左导航：leftsidebar
	右导航：rightsidebar
	菜单：menu
	子菜单：submenu
	标题: title
	摘要: summary

### 8.3 功能类
	标志：logo
	广告：banner
	登陆：login
	登录条：loginbar
	注册：regsiter
	搜索：search
	功能区：shop
	标题：title
	加入：joinus
	状态：status
	按钮：btn
	滚动：scroll
	标签页：tab
	文章列表：list
	提示信息：msg
	当前的: current
	小技巧：tips
	图标: icon
	注释：note
	指南：guild
	服务：service
	热点：hot
	新闻：news
	下载：download
	投票：vote
	合作伙伴：partner
	友情链接：link
	版权：copyright

