B5M.WEB前端开发标准
===


## 公共内容HTML结构

帮5买 全网站通用模块html代码


### 1. 顶部topbar

HTML代码：
```html
<div class="topbar">
    <div class="topbar-inner">
        <div class="topbar-nav">
            <a target="_self" class="home" href="http://www.b5m.com">帮5买首页</a>
            <span class="line"></span>
            <a class="buy" href="http://hao.b5m.com">购物导航</a>
            <span class="line"></span>
            <a class="tao" href="http://t.b5m.com">帮5淘</a>
            <span class="line"></span>
            <a class="app" href="http://app.b5m.com">手机帮5买</a>
        </div>
        <!-- before login -->
        <div class="topbar-user" id="topbar-user-login">
            <div id="top_login" style="display: none;">
                <span class="hi">你好，</span>
                    <span class="user" data-hover="user-hover">
                        <a href="http://ucenter.b5m.com" id="b5muser" target="_self">b5m用户</a> <em class="arr"></em>
                        <span class="user-link">
                            <a href="http://ucenter.b5m.com/user/integral/integral.htm">积分</a>
                            <a href="http://ucenter.b5m.com/user/user/logout.htm">退出</a>
                        </span>
                    </span>
                <span class="line"></span>
            </div>
            <div id="top_unlogin" style="display: block;">
                <a href="http://ucenter.b5m.com" target="_self" rel="nofollow">登录</a>
                <a href="http://ucenter.b5m.com/forward.htm?method=/user/info/register" target="_self" rel="nofollow">免费注册</a>
            </div>
            <a href="javascript:void(0)" rel="fav" class="J_addFav" target="_self">收藏本站</a>
            <span class="line"></span>

            <div class="topbar-more" data-hover="topbar-more-hover">
                <a href="javascript:void(0)" id="J_addFav" target="_self" class="more">
                    网站导航 <em class="arr"></em>
                </a>

                <div class="topbar-prod">
                    <div class="item">
                        <a href="http://www.b5m.com" target="_blank">帮5买</a>
                        <a href="http://tejia.b5m.com" target="_blank">淘特价</a>
                        <a href="http://you.b5m.com" target="_blank">帮5游</a>
                        <a href="http://guang.b5m.com" target="_blank">帮5逛</a>
                        <a href="http://korea.b5m.com" target="_blank">韩国馆</a>
                        <a href="http://tuan.b5m.com/" target="_blank">团购</a>
                        <!--<a href="http://old.b5m.com/o/ticket" target="_blank">票务</a>-->
                    </div>
                    <div class="item">
                        <a class="h_icon b5t" href="http://t.b5m.com/" target="_blank">帮5淘</a>
                        <a class="h_icon gwdh" href="http://hao.b5m.com/" target="_blank">购物导航</a>
                        <a class="h_icon sjb5m" href="http://app.b5m.com/" target="_blank">手机帮5买</a>
                    </div>
                    <div class="item weixin">
                        <img alt="" src="http://cdn.bang5mai.com/upload/web/public/app/header/images/new_header/weixin_b5m.png">
                        <span>扫二维码，加帮5买微信好友</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
```

[演示](http://www.b5m.com)


### 2. 底部footer

HTML代码：
```html
<div class="footer">
	<div class="footer-links">
		<a class="item" target="_blank" rel="nofollow" href="http://old.b5m.com/o/about">关于帮5买</a>|<a class="item" target="_blank" rel="nofollow" href="http://old.b5m.com/o/about/contact">联系我们</a>|<a class="item" target="_blank" rel="nofollow" href="http://old.b5m.com/o/about/business">合作商家</a>|<a class="item" target="_blank" rel="nofollow" href="http://old.b5m.com/o/about/links">友情链接</a>|<a class="item" target="_blank" href="http://old.b5m.com/o/about/job">加入我们</a>|<a class="item" target="_blank" href="http://app.b5m.com/index.html">移动应用</a>|<a class="item" target="_blank" href="http://www.b5m.com/sitemap.html">站点地图</a>
	</div>
	<div class="footer-copyright">Copyright © 2011-2013 B5M.COM. All rights reserved. Powered by B5Msoft Co.,Ltd. 
	<br>增值电信业务经营许可证：沪B2-20130065号 | 中华人民共和国互联网药品信息服务资格证书（沪）-非经营性-2013-0034</div>
	<div class="footer-public">
		<a target="_blank" href="http://www.sgs.gov.cn/lz/licenseLink.do?method=licenceView&amp;entyId=20120620142952978"><img src="http://staticcdn.b5m.com/static/images/common/shgs.gif" alt="上海工商"></a> 
		<a target="_blank" href="http://www.sgs.gov.cn/lz/licenseLink.do?method=licenceView&amp;entyId=20120620142952978"><img src="http://staticcdn.b5m.com/static/images/common/cxwz.png" alt="诚信网站"></a> 
	</div>
</div>
```

[演示](http://www.b5m.com)


### 3. 友情链接

HTML代码：
```html
<div class="friend-links">
	<strong>友情链接：</strong>
    <a rel="nofollow" target="_blank" href="http://korea.b5m.com">韩国馆</a>                            
    <a rel="nofollow" target="_blank" href="http://www.b5m.com/article-5717-1.html">热门专题</a>                            
    <a rel="nofollow" target="_blank" href="http://www.b5m.com/article-5704-1.html?spm=0.0.0.0.0">最新资讯</a>
    <a rel="nofollow" target="_blank" href="http://tejia.b5m.com">天天特价</a>                            
    <a rel="nofollow" target="_blank" href="https://itunes.apple.com/cn/app/te-hui-you/id674936138?mt=8">特惠游</a>
    <a rel="nofollow" target="_blank" href="http://you.b5m.com">旅游网</a>                            
    <a rel="nofollow" target="_blank" href="https://itunes.apple.com/cn/app/tao-te-jia-tian-tian-tao-quan/id640526928?mt=8">淘特价</a>
    <a rel="nofollow" target="_blank" href="http://app.b5m.com/sejie.html">色界</a>                            
    <a rel="nofollow" target="_blank" href="http://s.b5m.com/search/s/___image________________%E8%8A%AD%E6%AF%94.html">芭比</a>
    <a rel="nofollow" target="_blank" href="http://tuan.b5m.com">帮5团</a>                            
    <a rel="nofollow" target="_blank" href="http://tiao.b5m.com/">帮5挑</a>                            
    <a rel="nofollow" target="_blank" href="http://www.b5m.com">比价网</a>                            
    <a rel="nofollow" target="_blank" href="http://bang.b5m.com/">帮社区</a>                            
    <a rel="nofollow" target="_blank" href="http://tejia.b5m.com/taoPage_specialOffer_taoIndex">最热单品</a>                    
</div>
```

[演示](http://www.b5m.com)


### 3. [autoFill搜索自动联想提示功能](doc/js.autoFill.md)


[演示](http://10.10.99.218/static/html/www/www.html)


