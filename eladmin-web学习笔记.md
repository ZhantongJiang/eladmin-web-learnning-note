# eladmin-web

## 目录

* [1. 依赖](#1)
  * [1.1 js-cookie](#1.1)
  * [1.2 normalize.css](#1.2)
  * [1.3 mavon-editor](#1.3)
  * [1.4 vue-highlightjs](#1.4)
  * [1.5 clipboard](#1.5)
  * [1.6 codemirror](#1.6)
  * [1.7 fuse.js](#fuse.js)
  * [1.8 jsencrypt](#1.8)
  * [1.9 path-to-regexp](#1.9)
  * [1.10 qs](#1.10)
  * [1.11 screenfull](#1.11)
  * [1.12 vue-count-to](#1.12)
  * [1.13 vue-echarts](#1.13)
  * [1.14 vue-image-crop-upload](#1.14)
  * [1.15 wangeditor](#1.15)
  * [1.16 其他](#1.16)
* [2.  目录结构](#2)
* [3. vue-router](#3)
* [4. vuex](#4)
  * [4.1 require.context](#4.1)
  * [4.2 目录结构](#4.2)
* [5. 功能模块](#5)
  * [5.1 登录登出](#5.1)
  * [5.2 layout](#5.2)
  * [5.3 首页 dashboard](#5.3)
  * [5.4 增删改查的封装](#5.4)
  * [5.5 系统管理 system](#5.5)
* [6. css](#6)
  * [6.1 svg图标的使用](#6.1)
  * [6.2 bootstrap responsive web design](#6.2)
* [7. 缺陷](#7)







<h2 id="1">依赖</h2>

<h3 id="1.1">js-cookie</h3>

[https://www.npmjs.com/package/js-cookie](https://www.npmjs.com/package/js-cookie)

轻量级处理cookie的API

项目中：配置信息（setting.js）或用户信息存储于cookie中



<h3 id="1.2">normalize.css √</h3>

[http://necolas.github.io/normalize.css/](http://necolas.github.io/normalize.css/)

类似于reset.css，比reset.css更适用于H5，且能跨浏览器达到高度一致性



<h3 id="1.3">mavon-editor</h3>

[https://www.npmjs.com/package/mavon-editor](https://www.npmjs.com/package/mavon-editor)

基于vue的markdown编辑器

项目中：组件管理->Markdown



<h3 id="1.4">vue-highlightjs</h3>

[https://highlightjs.org/](https://highlightjs.org/)

页面中代码高亮插件，支持189种语言和94种样式，插件和样式要分别引入到项目中

项目中：系统监控->异常日志（errorLog.vue）；系统管理->任务调度->日志（log.vue）



<h3 id="1.5">clipboard</h3>

[http://www.clipboardjs.cn/](http://www.clipboardjs.cn/)

拷贝文字工具

项目中：组件管理->图标库



<h3 id="1.6">codemirror</h3>

[https://codemirror.net/](https://codemirror.net/)

支持语法高亮的代码编辑器，支持超过100种语言

项目中：组件管理->Yaml编辑器



<h3 id="1.7">fuse.js</h3>

[https://fusejs.io/](https://fusejs.io/)

模糊搜索工具库，可以设置模糊搜索的匹配选项以及结果的展示方式，支持多关键字范围内的搜索，功能很强大

项目中：header搜索引擎



<h3 id="1.8">jsencrypt</h3>

[http://travistidwell.com/jsencrypt/](http://travistidwell.com/jsencrypt/)

RSA加密工具

项目中：主要用于项目中所有入参为password的加密



<h3 id="1.9">path-to-regexp</h3>

[https://github.com/pillarjs/path-to-regexp](https://github.com/pillarjs/path-to-regexp)

将路径转换成正则表达式的工具

项目中：为了兼容el-breadcrumb不支持路由设置为:id的缺陷，使用pathToRegexp.compile方法用对象来填充已有路径规则



<h3 id="1.10">qs √</h3>

[https://www.npmjs.com/package/qs](https://www.npmjs.com/package/qs)

序列化工具，与JSON.stringify()、JSON.parse()类似，可以将对象转化成链接中key=value的形式，或者将不规则的字符串'foo[bar][baz\]=foobarbaz'转化成对象

项目中：将对象生成为get请求中的参数



<h3 id="1.11">screenfull</h3>

[https://github.com/sindresorhus/screenfull.js/](https://github.com/sindresorhus/screenfull.js/)

全屏工具

项目中：header中全屏入口（src/components/Screenfull/index.vue）



<h3 id="1.12">vue-count-to √</h3>

[https://www.npmjs.com/package/vue-count-to](https://www.npmjs.com/package/vue-count-to)

数字滚动动画效果插件

项目中：首页4个数字总计展示



<h3 id="1.13">vue-echarts</h3>

[https://github.com/ecomfe/vue-echarts](https://github.com/ecomfe/vue-echarts)

基于 ECharts v4.1.0+ 开发，依赖 Vue.js v2.2.6+的图表组件

项目中：系统监控->服务监控



<h3 id="1.14">vue-image-crop-upload</h3>

[https://www.npmjs.com/package/vue-image-crop-upload](https://www.npmjs.com/package/vue-image-crop-upload)

pc端图片剪裁上传组件

项目中：个人中心



<h3 id="1.15">wangeditor</h3>

[http://www.wangeditor.com/](http://www.wangeditor.com/)

Web富文本编辑器

项目中：组件管理->富文本



<h3 id="1.16">其他</h3>

package.json中安装但项目中无具体引用的依赖：

* [connect](https://www.npmjs.com/package/connect) nodejs中间件的模块化组件
* [file-saver](https://www.npmjs.com/package/file-saver) 在浏览器上生成文件并保存到本地的插件
* [js-beautify](https://www.npmjs.com/package/js-beautify) 前端美化工具，支持html、js、css的自动化排版
* [jszip](https://stuk.github.io/jszip/) 创建、读取和编辑.zip文件的插件
* [sortablejs](http://www.sortablejs.com/) 拖拽库
* [vue-cropper](https://github.com/xyxiao001/vue-cropper) 图片裁剪插件
* [vue-splitpane](https://www.npmjs.com/package/vue-splitpane) 垂直水平分割窗口的插件
* [vuedraggable](https://www.npmjs.com/package/vuedraggable) 基于Sortable.js实现拖拽功能的组件
* [xlsx](https://github.com/SheetJS/sheetjs) 读取xls或xlsx文件







<h2 id="2">目录结构</h2>

* [.editorconfig](https://editorconfig.org/) 代码风格配置文件，可协同不同的开发人员、编辑器使用统一的代码风格进行编码 √
* [.env.development]([https://cli.vuejs.org/zh/guide/mode-and-env.html#%E6%A8%A1%E5%BC%8F](https://cli.vuejs.org/zh/guide/mode-and-env.html#模式))
* [.env.production]([https://cli.vuejs.org/zh/guide/mode-and-env.html#%E6%A8%A1%E5%BC%8F](https://cli.vuejs.org/zh/guide/mode-and-env.html#模式)) 用于vue-cli-service build 和 vue-cli-service test:e2e
* [.eslintignore](.eslintignore)
* [.eslintrc.js](https://eslint.org/docs/rules/) （.eslintrc.{js,yml,json}）
* [.gitignore](https://github.com/github/gitignore)
* [.travis.yml](http://www.ruanyifeng.com/blog/2017/12/travis_ci_tutorial.html) 在线托管的持续集成服务，绑定Github项目，抓取新的代码自动进行测试构建，自动部署到测试环境。每次提交新的代码，都能及时发现问题并修复
* [babel.config.js](https://www.babeljs.cn/docs/7.2.0/config-files#project-wide-configuration)
* [jest.config.js](https://jestjs.io/docs/en/configuration#docsNav) 在vue项目中使用jest测试单文件组件[vue-test-utils](https://vue-test-utils.vuejs.org/zh/guides/testing-single-file-components-with-jest.html) √
* LICENSE
* package.json
* package-lock.json
* [plopfile.js](https://plopjs.com/documentation/) 自动生成文件模板的工具plop的配置项 √
* [postcss.config.js](https://github.com/postcss/postcss-loader) 转化CSS的工具[postcss](https://www.postcss.com.cn/)
* README.md
* vue.config.js
* /src
  * /api 接口请求模块合集
  * /assets 静态资源（图片、图标、css）
  * /components 组件合集
  * /layout 页面布局
  * /mixins 混合（复用方法合集） √
  * /router 路由
  * /store vux
  * /utils 工具合集
  * /views 功能模块对应页面
  * App.vue
  * main.js
  * settings.js 平台配置信息（登录状态、平台信息、请求配置等等非响应式数据） √







<h2 id="3">vue-router</h2>

路由定义方式：routes声明中只定义了每个用户都有的固定的几个路由，类似于菜单中这样通过角色管理添加的路由，则通过调用接口后使用addRoutes的方式动态添加路由







<h2 id="4">vuex</h2>

<h3 id="4.1">require.context √</h3>

[https://webpack.docschina.org/guides/dependency-management/#requirecontext](https://webpack.docschina.org/guides/dependency-management/#requirecontext)

```javascript
/*
 * 用来实现自动化导入模块的可以获取一个特定的上下文的webpack API
 * 参数：
 * 		{String} directory 读取文件的路径
 *		{Boolean} useSubdirectories 是否遍历文件的子目录
 * 		{RegExp} RegExp 匹配文件的正则
 * 		{"sync" | "eager" | "weak" | "async-weak" | "lazy" | "lazy-once"} mode 模块加载模式
 * 返回值：
 * 		一个（require）函数（包含三个属性：resolve, keys, id），接收一个参数：request：
 * 				resolve 是一个函数，它返回 request 被解析后得到的模块 id；
 * 				keys 是一个函数，它返回一个所有匹配成功的数组集，由所有可能被此 context module 处理的请求组成
 *				id 是一个字符串，主要用在module.hot.accept
 */
require.context(directory, useSubdirectories, RegExp, mode)
```

<h3 id="4.2">目录结构</h3>

* index.js 导入相关依赖文件，生成并导出new Vuex.Store()实例
* getter.js 相关依赖文件中的getter合集 √
* /modules
  * api.js 项目中功能实现相关的api配置合集
  * app.js 项目窗口（桌面）相关
  * permission.js 用户权限相关
  * settings.js 项目窗口（桌面）配置相关
  * tagsView.js 标签页功能相关
  * user.js 用户信息相关







<h2 id="5">功能模块</h2>

<h3 id="5.1">登录登出</h3>

#### 登录

1. 访问条件：cookie中没有token的信息时会进入到login页面
2. /login后通常还接一个redirect参数，用来返回上一次访问的页面 √
3. “记住我”通过cookie实现
4. 登录中按钮的交互状态：loading + 更改文字 √
5. 密码传参的时候要加密

#### 登出

触发登出的三种情境：

* 用户手动退出
* 访问接口状态为401
* 个人中心重置密码成功后



<h3 id="5.2">layout</h3>

#### 菜单

1. [el-scrollbar](https://github.com/ElemeFE/element/tree/dev/packages/scrollbar) √

   Element未公开组件，滚动条样式统一

2. vue实例[functional]([https://cn.vuejs.org/v2/guide/render-function.html#%E5%87%BD%E6%95%B0%E5%BC%8F%E7%BB%84%E4%BB%B6](https://cn.vuejs.org/v2/guide/render-function.html#函数式组件))属性 √

   组件无状态（没有data）、无实例（没有this上下文）

3. [component]([https://cn.vuejs.org/v2/guide/components.html#%E5%8A%A8%E6%80%81%E7%BB%84%E4%BB%B6](https://cn.vuejs.org/v2/guide/components.html#动态组件))动态组件 √

4. [mixin](https://cn.vuejs.org/v2/guide/mixins.html)混入 √

   * 数据对象在内部会进行递归合并，并在发生冲突时以组件数据优先

   * 同名钩子函数将合并为一个数组，因此都将被调用，混入对象的钩子将在组件自身钩子**之前**调用

     * 值为对象的选项，例如 `methods`、`components` 和 `directives`，将被合并为同一个对象。两个对象键名冲突时，取组件对象的键值对

   * **使用模块作用域保持不允许外部访问的函数的私有性。如果无法做到这一点，就始终为插件、混入等不考虑作为对外公共 API 的自定义私有 property 使用 `$_` 前缀。并附带一个命名空间以回避和其它作者的冲突 (比如 `$_yourPluginName_`)**

     > [官方Vue代码风格指南](https://cn.vuejs.org/v2/style-guide/index.html#%E8%A7%84%E5%88%99%E5%BD%92%E7%B1%B) 可作为代码书写规格的标准 √

5. [document.hidden](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/hidden)

   value：

   * false：document.visibilityState属性返回“visible”时
   * true：document.visibilityState属性返回除“visible”时

   该属性只是出于历史原因而保留的，建议使用document.visibilityState去判断 √

   > [Page Visibility API 教程——阮一峰](http://www.ruanyifeng.com/blog/2018/10/page_visibility_api.html)

#### 导航栏

1. 面包屑过渡效果使用[transition-group](https://cn.vuejs.org/v2/api/#transition-group)实现 √
2. 字符串比较的时候有些场景可以采用：目标值.toLocaleLowerCase === 参定值.toLocaleLowerCase（或toLocaleUpperCase方法） √
3. [path.resolve](#http://nodejs.cn/api/path.html#path_path_resolve_paths)将路径或路径片段的序列解析为绝对路径
4. [深度作用选择器]([https://vue-loader.vuejs.org/zh/guide/scoped-css.html#%E6%B7%B1%E5%BA%A6%E4%BD%9C%E7%94%A8%E9%80%89%E6%8B%A9%E5%99%A8](https://vue-loader.vuejs.org/zh/guide/scoped-css.html#深度作用选择器))

#### tag标签页

1. [.middle鼠标中键点击修饰符](https://cn.vuejs.org/v2/api/#v-on)

   原生js中，用[mousedown事件](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/mousedown_event)的button属性去监听：0 为左键、1 为中键、2 为右键
   
2. [wheel鼠标滚轮事件](https://developer.mozilla.org/zh-CN/docs/Web/API/WheelEvent)

   `WheelEvent` 接口表示用户滚动鼠标滚轮或类似输入设备时触发的事件；继承了*父接口[`MouseEvent`](https://developer.mozilla.org/zh-CN/docs/Web/API/MouseEvent)、[`UIEvent`](https://developer.mozilla.org/zh-CN/docs/Web/API/UIEvent)、[`Event`](https://developer.mozilla.org/zh-CN/docs/Web/API/Event)的属性*

   对于这个方法的用户界面事件的标准尚处于起草阶段，各家浏览器未统一标准，且与鼠标设置的滚动单位有关（实际高度=滚动单位*行高（40）待验证）

3. [contextmenu（鼠标）右键事件](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/oncontextmenu)

   全局事件，可以设置或禁用（preventDefault）

4. [getBoundingClientRect相对视口位置](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/getBoundingClientRect)

5. 整体思路：

   按路由meta中noCache属性分为两种类型（两种类型不是排斥关系）：浏览过的标签页visitedViews、keepAlive的标签页cachedViews。对这两种标签页类型分别提供增删改的方法以控制不同路由的跳转，同时提供了`右键功能`以便快速整理过多的标签页，（标签页过多时）并对当前选中的标签页的位置进行控制







<h3 id="5.3">首页 dashboard</h3>

#### mixin

1. [transitionend](https://developer.mozilla.org/zh-CN/docs/Web/Events/transitionend)

   其中事件参数event为[TransitionEvent](https://developer.mozilla.org/zh-CN/docs/Web/API/TransitionEvent)

   项目中当transition监听的属性为width时触发，即菜单栏收缩或展开时触发

#### echarts

注意在组件销毁的同时销毁图表

```javascript
beforeDestroy() {
    if (!this.chart) {
      return
    }
    this.chart.dispose()
    this.chart = null
}
```







<h3 id="5.4">
    增删改查的封装
</h3>

#### crud

1. [Vue.observable( object )](https://cn.vuejs.org/v2/api/#Vue-observable)

   使一个对象可响应

   在Vue2.x中入参的object与方法返回的对象是同一个，但在Vue3.x中返回的对象具有拦截器属性，所以推荐使用**返回的对象**而不是源数据

2. 待









<h3 id="5.5">
    系统管理 system
</h3>









<h2 id="6">
  css
</h2>

<h3 id="6.1">svg图标的使用</h3>

1. 步骤（待验证，参考教程[https://panjiachen.github.io/vue-element-admin-site/zh/feature/component/svg-icon.html](https://panjiachen.github.io/vue-element-admin-site/zh/feature/component/svg-icon.html)）：

   1. 安装解析svg类型图标的依赖库[svg-sprite-loader](https://github.com/JetBrains/svg-sprite-loader)
2. 配置webpack
   3. 构造文件目录及svg组件

2. svg压缩工具[svgo](https://github.com/svg/svgo)（参考教程[SVG精简压缩工具svgo简介和初体验](https://www.zhangxinxu.com/wordpress/2016/02/svg-compress-tool-svgo-experience/)）

<h3 id="6.2">bootstrap responsive web design</h3>

[Bootstrap响应式设计参考]([https://github.com/ZhantongJiang/eladmin-web-learnning-note/blob/master/bootstrap%204%20responsive%20web%20design%40www.java1234.com.pdf](https://github.com/ZhantongJiang/eladmin-web-learnning-note/blob/master/bootstrap 4 responsive web design%40www.java1234.com.pdf))







<h2 id="7">缺陷</h2>

1. 在非首页的标签页设置布局，回跳到404页面，crud报错
2. navbar搜索框的选项没有过滤有子菜单的菜单，因没有匹配路由的页面，导致选中时跳转至404 
3. utils/validate.js isvalidPhone校验手机号方式已过期
