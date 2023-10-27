/common
common.css - 封装的部分公共样式
free.css - 用法类似于tailwind css的css样式
全局样式库
```js
// App.vue
<style>
	/*每个页面公共css */
	/* 引入全局样式库 */
	@import url("/common/free.css");
	@import url("/common/common.css");
	/*  #ifndef APP-PLUS-NVUE */
	@import url("/common/icon.css");
	/*  #endif  */
</style>
```

icon.css - 阿里巴巴上部分图片的css文件
从阿里巴巴上下载文件压缩包包含几个文件woff2/woff/ttf
icon.css 需要引用到这几个文件
在阿里巴巴图标库可自制激活图片or未激活图片

* 条件编译
```js
// App.vue style中引用
	/*  #ifndef APP-PLUS-NVUE */
	@import url("/common/icon.css");
	/*  #endif  */

```

* 小程序中不支持配置midButton
```js
// pages.json
 "tabBar": {
	 // ...其他代码
		"midButton": {
			"iconPath": "/static/tabbar/min.png",
			"iconWidth": "60px",
			"height": "65px"
		},
 }

```
