B5M.WEB前端开发标准
===


## 公共CSS属性

帮5买 全网站通用css样式
> 可以不用，但不能乱用


### 1. 网页宽度统一设定

样式名：`.wrap`
```css
	.wrap{
		width: 980px;
		margin: 0 auto;
	}
```

### 2. 清除浮动
	
样式名：`.cf`
```css
	.cf:after {
	    visibility:hidden;
	    display:block;
	    font-size:0;
	    content:" ";
	    clear:both;
	    height:0;
	}
	.cf {
	    zoom:1; /* for IE6 IE7 */
	}
```

### 3. 左右浮动，并设置内联元素

样式名：`.l` (向左浮动)  
样式名：`.r` (向右浮动)  
```css
	.l,.r {
	    display:inline;
	}
	.l {
	    float:left;
	}
	.r {
	    float:right;
	}
```

### 4. 单行文字溢出时出现省略号，需设定宽度 

样式名：`.tof`
```css
	.tof {
	    overflow: hidden;
	    text-overflow: ellipsis;
	    white-space: nowrap;
	}
```

### 5. 人民币显示符号

样式名：`.rmb`
```css
	.rmb {
	    font-family: arial;
	    font-style: normal;
	    padding-right: 4px;
	}
```
