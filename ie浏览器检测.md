**<IE11的检测逻辑是检测不出来的**


## 关键词

浏览模式：ie为用户提供的新版本浏览器用老的版本浏览器版本的浏览器的一个功能；检测方式：navigator.userAgent
文档模式：ie为用户提供的让用户设置当前文档的渲染的功能；检测方式：document.documentMode
文档渲染引擎：ie的渲染内核；检测方式：document.compatMode


检测的结果实例(ie9浏览模式, Quirks)：

```html
navigator.userAgent: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.1; WOW64; Trident/5.0; SLCC2; .NET CLR 2.0.50727)
document.documentMode: 5
document.compatMode: BackCompat

```
### 浏览模式统计列表

| 相应的浏览模式|navigator.userAgent|备注|
|----|----|----|----|----|
|ie6|MSIE 6.0|
|ie7|MSIE 7.0|
|ie8|MSIE 8.0|
|ie8兼容性视图|MSIE 7.0|
|ie9|MSIE 9.0
|ie9兼容性视图|MSIE 7.0|
|ie10|MSIE 10.0;
|ie10兼容性视图|MSIE 7.0|
|ie11| Trident/7.0
|edge| Edge/14.14393|
|wp10|Windows Phone 10.0|
|wp8|Windows Phone 8|


### 文档模式列表

| 相应的文档模式|document.documentMode|document.compatMode|备注|
|----|----|----|----|----|
|ie5|5|BackCompat
|ie6|6|CSS1Compat
|ie7|7|CSS1Compat
|ie8|8|CSS1Compat
|杂项|5|BackCompat| ie10 Quirks为documentMode＝10
|ie9|9|CSS1Compat
|ie10|10|CSS1Compat
|ie11| undifined|CSS1Compat| edge下的ie11，documentMode＝11
|edge|undifined|CSS1Compat|ie11下，documentMode＝11
|wp10|undifined|CSS1Compat

### 真实浏览器版本

| 真实浏览器版本|navigator.userAgent|备注|
|----|----|----|----|----|
|ie6|MSIE 6.0|
|ie7|MSIE 7.0|
|ie8| Trident/4.0|
|ie9|  Trident/5.0
|ie10|  Trident/6.0
|ie11| Trident/7.0
|edge| Edge/14.14393|
|wp10|暂无|
|wp 8| 暂无||

## 结论：

因为我们考虑不兼容的很大因素是低版本的ie的渲染方式不标准，兼容性太差，所以不兼容。所以我认为当我们需要对某些低版本的ie进行处理的时候，应该综合3个指标考虑：真实浏览器版本->文档模式->浏览模式；

0. 对于真实浏览器版本小于8的可以引导到最新版浏览器下载页：[引导页](https://www.tmall.com/wow/portal/act/ali-page-updater)
0. 对于真实浏览器版大于8，而浏览模式或者文档模式和真实版本匹配不上的需要引导用户设置正确和下载最新浏览器
0. 页面渲染是按照文档模式渲染的，所以我们着重关注真实版本和文档模式

#### 设置浏览器的默认文档为最新的模式

```html
  <meta http-equiv="X-UA-Compatible" content="IE=edge" >

```
 





