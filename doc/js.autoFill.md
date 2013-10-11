B5M.WEB前端开发标准
===


## autoFill - 自动填充功能

主要用于网站搜索，用户在搜索框中键入关键字后，系统会自动提示相应的关键字以便用户选择


### jquery原型方法

`autoFill (url:String,site:String,[callback:Function]):jQueryObject`

### 概述

为选定`input[tyep=text]`添加输入建议功能


### 参数说明

#### url

用来发送请求的URL字符串,空字符为默认：`http://s.b5m.com/allAutoFill.htm`

#### site

用来判定数据排序筛选的关键字，空字符串为默认：`www`，目前可选值有：`www,b5mo,tejia,hotel,ticketp,tourguide,tourp,tuana`

#### callback(可选)

点击（选中回城）aufoFill列表内本站结果跳转前回调函数


### 事件

#### listshow

aufoFill列表显示时在`$(selector)`触发`listshow`事件 

#### listhide

aufoFill列表隐藏时在`$(selector)`触发`listhide`事件 


### 返回

返回$(selector)


### 其它

请确保执行该方法的input提交/跳转功能不被绑定在keydown事件上，如果绑定可将`keydown`换成`keyup`


### 使用方法

1. 在`head`引入相应的CSS文件
```html
<link rel="stylesheet" href="http://staticcdn.b5m.com/static/css/common/common.css" />
```

2. 在`</body>`前引入js文件
```html
<script type="text/javascript" src="http://staticcdn.b5m.com/static/scripts/common/jquery-1.9.1.min.js"></script>
<script type="text/javascript" src="http://staticcdn.b5m.com/static/scripts/common/autoFill.js"></script>
```

3. 选择input对象装载功能
```js
$(selector).autoFill(url:String, site:String); 
```
```js
$(selector).autoFill(url:String, site:String,functino(){....});
```


