# jquery

F:\BaiduNetdiskDownload\jQuery\源码_课件\源码_课件\jQueryTest

![image-20210217093842572](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217093842572.png)

![image-20210217095536513](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217095536513.png)

### jquery函数的使用

![image-20210217100352491](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217100352491.png)

### jquery对象的使用

![image-20210217102309325](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217102309325.png)

![image-20210217102426608](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217102426608.png)

```
1. jQuery对象是一个包含所有匹配的任意多个dom元素的伪数组对象
2. 基本行为
  * size()/length: 包含的DOM元素个数
  * [index]/get(index): 得到对应位置的DOM元素
  * each(): 遍历包含的所有DOM元素
  * index(): 得到在所在兄弟元素中的下标
```

![image-20210217103431293](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217103431293.png)

### 基本选择器

![image-20210217103516806](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217103516806.png)

![image-20210217103623217](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217103623217.png)

### 层次选择器

![image-20210217103738964](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217103738964.png)

### 过滤选择器

![image-20210217103810987](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217103810987.png)

![image-20210217105112698](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217105112698.png)

### 表单选择器

![image-20210217103851481](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217103851481.png)

![image-20210217105725921](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217105725921.png)

冒号加关键字，表单选择器自成一派

### 工具方法

![image-20210217112818213](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217112818213.png)

![image-20210217204314289](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217204314289.png)

![image-20210217204530598](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217204530598.png)

### day01复习

1. 了解jQuery

  * 是什么: What?
    * 一个JS函数库: write less, do more
    * 封装简化DOM操作(CRUD) / Ajax
  * 为什么用它: why?
    * 强大选择器: 方便快速查找DOM元素
    * 隐式遍历(迭代): 一次操作多个元素
    * 读写合一: 读数据/写数据用的是一个函数
    * 链式调用: 可以通过.不断调用jQuery对象的方法
    * 事件处理
    * DOM操作(CUD)
    * 样式操作
    * 动画
    * 浏览器兼容
  * 如何使用: How?
    * 引入jQuery库
      * 本地引入与CDN远程引入
      * 测试版与生产版(压缩版)
    * 使用jQuery
      * 使用jQuery函数: $/jQuery
      * 使用jQuery对象: $xxx(执行$()得到的)

2. jQuery的2把利器

  * jQuery函数: $/jQuery

    * jQuery向外暴露的就是jQuery函数, 可以直接使用
    * 当成一般函数使用人: $(param)
      * param是function: 相当于window.onload = function(文档加载完成的监听)
      * param是选择器字符串: 查找所有匹配的DOM元素, 返回包含所有DOM元素的jQuery对象
      * param是DOM元素: 将DOM元素对象包装为jQuery对象返回  $(this)
      * param是标签字符串: 创建标签DOM元素对象并包装为jQuery对象返回
    * 当成对象使用: $.xxx
      * each(obj/arr, function(key, value){})
      * trim(str)

  * jQuery对象

    * 包含所有匹配的n个DOM元素的伪数组对象

    * 执行$()返回的就是jQuery对象

    * 基本行为:

      * length/size(): 得到dom元素的个数

      * [index]: 得到指定下标对应的dom元素

      * each(function(index, domEle){}): 遍历所有dom元素

      * index(): 得到当前dom元素在所有兄弟中的下标

3. 选择器

  * 是什么?
    * 有特定语法规则(css选择器)的字符串
    * 用来查找某个/些DOM元素: $(selector)
  * 分类
    * 基本
      * #id
      * tagName/*
      * .class
      * selector1,selector2,selector3: 并集
      * selector1selector2selector3: 交集
    * 层次
      * 找子孙后代, 兄弟元素
      * selector1>selector2: 子元素
      * selector1 selector2: 后代元素
    * 过滤
      * 在原有匹配元素中筛选出其中一些
      * :first
      * :last
      * :eq(index)
      * :lt
      * :gt
      * :odd
      * :even
      * :not(selector)
      * :hidden隐式
      * :visible可视
      * [attrName]属性过滤
      * [attrName=value]
    * 表单
      * :input
      * :text
      * :checkbox
      * :radio
      * :checked: 选中的

4. 属性/文本

  * 操作标签的属性, 标签体文本
  * attr(name) / attr(name, value): 读写非布尔值的标签属性
  * prop(name) / prop(name, value): 读写布尔值的标签属性
  * removeAttr(name)/removeProp(name): 删除属性
  * addClass(classValue): 添加class
  * removeClass(classValue): 移除指定class
  * val() / val(value): 读写标签的value
  * html() / html(htmlString): 读写标签体文本

### offset和position

![image-20210217205907654](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217205907654.png)

### scroll

![image-20210217210529655](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217210529655.png)

![image-20210217210708967](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217210708967.png)

### 元素的尺寸

```
<!--
1. 内容尺寸
  height(): height
  width(): width
2. 内部尺寸
  innerHeight(): height+padding
  innerWidth(): width+padding
3. 外部尺寸
  outerHeight(false/true): height+padding+border  如果是true, 加上margin
  outerWidth(false/true): width+padding+border 如果是true, 加上margin
-->
```

过滤和筛选

![image-20210217212057358](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217212057358.png)

![image-20210217212113277](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217212113277.png)

两种写法

### jquery对象查找

```
<!--
在已经匹配出的元素集合中根据选择器查找孩子/父母/兄弟标签
1. children(): 子标签中找
2. find() : 后代标签中找
3. parent() : 父标签
4. prevAll() : 前面所有的兄弟标签
5. nextAll() : 后面所有的兄弟标签
6. siblings() : 前后所有的兄弟标签
-->
```

### 文档增删改

```
<!--
1. 添加/替换元素
  * append(content)
    向当前匹配的所有元素内部的最后插入指定内容
  * prepend(content)
    向当前匹配的所有元素内部的最前面插入指定内容
  * before(content)
    将指定内容插入到当前所有匹配元素的前面
  * after(content)
    将指定内容插入到当前所有匹配元素的后面替换节点
  * replaceWith(content)
    用指定内容替换所有匹配的标签删除节点
2. 删除元素
  * empty()
    删除所有匹配元素的子元素
  * remove()
    删除所有匹配的元素
-->
```

### 事件绑定

```
<!--
1. 事件绑定(2种)：
  * eventName(function(){})
    绑定对应事件名的监听,    例如：$('#div').click(function(){});
  * on(eventName, funcion(){})
    通用的绑定事件监听, 例如：$('#div').on('click', function(){})
  * 优缺点:
    eventName: 编码方便, 但只能加一个监听, 且有的事件监听不支持
    on: 编码不方便, 可以添加多个监听, 且更通用
2. 事件解绑：
  * off(eventName)
3. 事件的坐标
  * event.clientX, event.clientY  相对于视口的左上角
  * event.pageX, event.pageY  相对于页面的左上角
  * event.offsetX, event.offsetY 相对于事件元素左上角
4. 事件相关处理
  * 停止事件冒泡 : event.stopPropagation()
  * 阻止事件默认行为 : event.preventDefault()
-->
```

### 事件面试题

![image-20210217215429628](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217215429628.png)

![image-20210217215747482](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217215747482.png)

### 事件委托

```
<!--
1. 事件委托:
  * 将多个子元素(li)的事件监听委托给父辈元素(ul)处理
  * 监听回调是加在了父辈元素上
  * 当操作任何一个子元素(li)时, 事件会冒泡到父辈元素(ul)
  * 父辈元素不会直接处理事件, 而是根据event.target得到发生事件的子元素(li), 通过这个子元素调用事件回调函数
2. 事件委托的2方:
  * 委托方: 业主  li
  * 被委托方: 中介  ul
3. 使用事件委托的好处
  * 添加新的子元素, 自动有事件响应处理
  * 减少事件监听的数量: n==>1
4. jQuery的事件委托API
  * 设置事件委托: $(parentSelector).delegate(childrenSelector, eventName, callback)
  * 移除事件委托: $(parentSelector).undelegate(eventName)
-->
```

### day02复习

1. CSS模块

  * style样式
    * css(styleName): 根据样式名得到对应的值
    * css(styleName, value): 设置一个样式
    * css({多个样式对}): 设置多个样式
  * 位置坐标
    * offset(): 读/写当前元素坐标(原点是页面左上角)
    * position(): 读当前元素坐标(原点是父元素左上角)
    * scrollTop()/scrollLeft(): 读/写元素/页面的滚动条坐标
  * 尺寸
    * width()/height(): width/height
    * innerWidth()/innerHeight(): width + padding
    * outerWidth()/outerHeight(): width + padding + border

2. 筛选模块

  * 过滤
    * 在jQuery对象内部的元素中找出部分匹配的元素, 并封装成新的jQuery对象返回
    * first()
    * last()
    * eq(index)
    * filter(selector): 对当前元素提要求
    * not(selector): 对当前元素提要求, 并取反
    * has(selector): 对子孙元素提要求
  * 查找
    * 查找jQuery对象内部的元素的子孙/兄弟/父母元素, 并封装成新的jQuery对象返回
    * children(selector): 子元素
    * find(selector): 后代元素
    * preAll(selector): 前的所有兄弟
    * siblings(selector): 所有兄弟
    * parent(): 父元素

3. 文档处理(CUD)模块

  * 增加
    * append() / appendTo(): 插入后部
    * preppend() / preppendTo(): 插入前部
    * before(): 插到前面
    * after(): 插到后面
  * 删除
    * remove(): 将自己及内部的孩子都删除
    * empty(): 掏空(自己还在)
  * 更新
    * replaceWith()

4. 事件模块

  * 绑定事件
    * eventName(function(){})
    * on('eventName', function(){})
    * 常用: click, mouseenter/mouseleave mouseover/mouseout focus/blur
    * hover(function(){}, function(){})
  * 解绑事件
    * off('eventName')
  * 事件委托
    * 理解: 将子元素的事件委托给父辈元素处理
      * 事件监听绑定在父元素上, 但事件发生在子元素上
      * 事件会冒泡到父元素
      * 但最终调用的事件回调函数的是子元素: event.target
    * 好处
      * 新增的元素没有事件监听
      * 减少监听的数量(n==>1)
    * 编码
      * delegate(selector, 'eventName', function(event){}) // 回调函数中的this是子元素
      * undelegate('eventName')
  * 事件坐标
    * event.offsetX: 原点是当前元素左上角
    * event.clientX: 原点是窗口左上角
    * event.pageX: 原点是页面左上角
  * 事件相关
    * 停止事件冒泡: event.stopPropagation()
    * 阻止事件的默认行为: event.preventDefault()

### 动画

```
<!--
淡入淡出: 不断改变元素的透明度来实现的
1. fadeIn(): 带动画的显示
2. fadeOut(): 带动画隐藏
3. fadeToggle(): 带动画切换显示/隐藏
-->
```

```
<!--
滑动动画
1. slideDown(): 带动画的展开
2. slideUp(): 带动画的收缩
3. slideToggle(): 带动画的切换展开/收缩
-->
```

```
<!--
显示隐藏，默认没有动画
1. show(): (不)带动画的显示
2. hide(): (不)带动画的隐藏
3. toggle(): (不)带动画的切换显示/隐藏
-->
```

### 自定义动画

```
<!--
jQuery动画本质 : 在指定时间内不断改变元素样式值来实现的
1. animate(): 自定义动画效果的动画
2. stop(): 停止动画

-->
```

### 多库共存

```
<!--
问题 : 如果有2个库都有$, 就存在冲突
解决 : jQuery库可以释放$的使用权, 让另一个库可以正常使用, 此时jQuery库只能使用jQuery了
API : jQuery.noConflict()
-->
```

### onload和ready（面试高频）

```
<!--
区别: window.onload与 $(document).ready()
  * window.onload
    * 包括页面的图片加载完后才会回调(晚)
    * 只能有一个监听回调
  * $(document).ready()
    * 等同于: $(function(){})
    * 页面加载完就回调(早)
    * 可以有多个监听回调
-->
```

### jquery插件

![image-20210217223002581](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217223002581.png)

### jquery-validation

![image-20210217230900162](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217230900162.png)

![image-20210217230948867](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217230948867.png)

### jquery ui

![image-20210217231521519](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217231521519.png)

F:\BaiduNetdiskDownload\jQuery\源码_课件\源码_课件\jQueryTest\prepare\插件\jqueryUI\jqueryUI_test\test.html

### layui

![image-20210217231830041](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217231830041.png)

### day03复习

* 动画效果
  * 在一定的时间内, 不断改变元素样式
  * slideDown()/slideUp()/slideToggle()
  * fadeOut()/fadeIn()/fadeToggle()
  * show()/hide()/toggle()
  * animate({结束时的样式}, time, fun)
  * stop()

* 插件机制
  * 扩展jQuery函数对象的方法
    $.extend({
      xxx: fuction () {} // this是$
    })
    $.xxx()
  * 扩展jQuery对象的方法
    $.fn.extend({
      xxx: function(){}  // this是jQuery对象
    })
    $obj.xxx()

* jQuery文档的结构图

![image-20210217232458039](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210217232458039.png)

# AJAX

### 课程介绍

![image-20210218202801343](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218202801343.png)

ajax就是能够在页面不刷新的情况下更新页面内容

ajax爬虫爬不到

![image-20210218203952394](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218203952394.png)

![image-20210218204119060](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218204119060.png)

1、进入目录

2、执行node xxx.js启动node服务器

### nodemon的使用

1、安装

npm install -g nodemon

nodemon server.js

2、因为ie走缓存，chrome不走缓存

![image-20210218232941544](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218232941544.png)

这种方式，添加了时间戳，不走缓存了

### 网络超时

![image-20210218234000444](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218234000444.png)

### 发送和取消

![image-20210218234223603](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218234223603.png)

### 重复发送

![image-20210218234503760](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218234503760.png)

![image-20210218235344470](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218235344470.png)

这样就可以发送自定义的头

### axios

![image-20210218235504287](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210218235504287.png)