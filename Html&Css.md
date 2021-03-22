# Html&Css

## HTML

### mata

meta用于设置网页中的元数据，元数据不是给用户看的

charset：指定网页的字符集

name：指定数据的名称

content：指定数据的内容

```html
<meta name="keywords" content="html5,css3">
//keywords(Keywords)是关键字，搜索html5会显示这个内容
<meta name="description" content="京东,css3">
//网站描述会在搜索引擎的搜索的结果中
//title的内容会是网页超链接的东西 
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org">
//重定向到另一个网站，3秒之后跳转
```

### 语义化标签

html标签应该关注标签的语义，而不是样式

h1-h6从大到小，重要性递减，h1最重要，h6最不重要

h1重要性仅次于title，一般页面中只有一个h1 

一般标题只会用到h1-h3，h4-h6很少用

页面中独占一行的是块元素

```html
<!--hgroup,标签用来分组，可以将一组相关的标题同时放入到hgroup-->
<hgroup>
    <h1>回乡偶书<h1>
    <h2>其一<h2>
</hgroup>
<!--<p>标签表示一个段落,独占一行-->
<!--<em>表示语音语调的一个加重，不会独占一行的叫做行内元素-->
        <!--strong表示加粗-->
        <!--blockquote表示长引用，块级元素-->
        <!--q表示短引用，行内元素-->
        <!--<br>表示换行-->
```

### 块和行内

块元素：对网页进行布局

行内元素：主要用来包裹文字

一般情况下会在块元素内放行内元素，而不会在行内元素中放块元素

块元素基本上什么都能放

p元素内不能放任何块元素

浏览器在在解析网页的时候，会对网页中不符合规范的内容进行修正

比如：

1、标签写在根元素外部

2、p嵌套了块元素

3、根元素出现了除head和body以外的子元素

### 语义化标签

布局标签

header：表示网页的头部

main：表示网页的主体部分，一个页面只有一个main

footer：表示网页的底部

nav：标识网页的导航

aside：和主体相关的其他内容（侧边栏）

article：表示一个独立的文章

section：表示一个独立的区块，上边的标签都不能表示时使用section

div：没有语义，就用来表示一个区块

span：行内元素无语义

### 列表

列表list：

1、铅笔

2、尺子

3、橡皮

在html中也有创建列表，html一共有三种

1、有序列表

2、无序列表

3、定义列表

有序列表ol

无序列表ul

列表项li

使用dl标签来创建一个定义列表

dt表示定义的内容

dd来对内容进行解释说明

列表之间可以互相嵌套

```html
<ul>
    <li>
        <ul>
            <li>
                <ul>
                </ul></li>
        </ul>
    </li>
    
</ul>
```

### 超链接简介

a：超链接，可以从一个页面跳转到其他页面，或者是当前页面的其他位置

使用a标签来定义超链接

属性：href指定跳转的目标路径

超链接也是一个行内元素，a可以嵌套它自身外的任何元素

./表示当前路径，如果不写./也不写../则就相当于写了./

./表示当前文件所在的目录

   -在这里当前页面就是09相对路径.html的陆行

   -./就等于09相对路径。html所在的目录path

../表示当前文件的上级目录

target属性：用来指定超链接打开的位置

可选值：

_self 默认值 在当前页面中打开超链接

_blank在一个新的网页中打开超链接

#点击超链接不会跳转，而是转到当前页面的顶部位置

id属性：每个标签都可以有一个id属性，每个标签到可以添加一个id唯一的，同意页面不能出现重复的id

```html
<a href="#bottom">去底部</a>
<a href="#p3">去第三个自然段</a>
<a id="bottom" href="#">回到顶部</a>
//#也可以作为占位符
<a href="#">占位符</a>
<a href="javascript:;">占位符</a>
```

### 图片标签

img标签

自结束标签，单标签

属于替换元素（块元素和行内元素之间，具有两种元素的特点）

src：写外部图片的途径，类似于href

alt：图片的描述，默认情况下不显示，有些浏览器会在图片无法加载时显示搜索引擎，搜索引擎会根据alt来识别图片，如果不写alt则图片不会被搜索引擎所搜索到

width：图片的宽（像素）

height：图片的高度

宽度和高度如果只修改了一个，则另一个会等比缩放

pc端不建议修改大小（内存，失真）

移动端经常需要对图片进行缩放

图片的格式：

jepg（jpg）：颜色丰富，不支持透明效果，不支持动图（显示照片）

gif：支持颜色比较少，支持简单透明，支持动图（颜色单一，动图）

png：支持颜色丰富，支持复杂透明，不支持动图（颜色丰富，复杂透明专为网页而生）

效果一样用小的，效果不一样用好的

webp：谷歌新推出的，专门用来表示网页中的一种格式，具备所有优点，文件还特别小，支持动图，透明。缺点兼容性不好IE不能用，谷歌，火狐，移动端可以用

base64：将图片进行base64进行编码，对数据进行加密，可以直接将图片转换为字符，通过字符的形式来引入图片，一般都是需要和网页一起加载出来。在网站找，编码的转化一下，也是在src里面。

### 内联框架

相当于在当前页面中引入一个其他页面，src指定引入网页路径，frameborder指定内联框架的边框。用的很少

```html
<iframe src="" width="" height="" frameborder="0">
    //frameborder的值0就是没有，1就是有
```

### 音频视频

audio标签：引入一个外部的音频文件

除了src，也可以使用以下的方法

```html
<audio src="./source/audio.mp3" controls autoplay loop>
    //controls是否允许用户控制播放。显示与不显示的区别
    //autoplay是否自动播放，如果设置了则页面打开时会自动播放，但目前大多数浏览器都不会自动播放
    //loop音乐是否循环播放
    //ie8以下不支持
 <audio controls>
     对不起，不支持audio标签
  <source src="MP3">
  <source src="ogg">
  </audio>
    //使用这种方法可以直接避免重复
    //优先级MP3高于ogg高于显示文字
  <embed src="mp3" type="audio/mp3" width="" height="">
    //老版本浏览器的,不好用
    //所以
<audio controls>
<source src="MP3">
<source src="ogg">
<embed src="mp3" type="audio/mp3" width="" height="">
</audio>

```

使用video引入视频文件

```html
<video controls>
    <source src="./aa.webm">
    <source src="./aa.mp4">
    <embed src="mp4" type="video/mp4" width="" height="">
</video>
```

在腾讯视频分享-》复制代码，用的就是iframe



## CSS

### 简介html5+css3

网页分成三部分：结构html，表现css，行为javascript

css层叠样式表

网也是一个多层的样式，css可以分别对每一层来设置样式，我们看到的是最上面的一层

使用css来修改元素的样式：

第一种方式（内联样式、行内样式）：

在标签内部通过style属性来设置元素的样式

问题：内联样式只能对一个标签生效，如果希望影响到多个元素，使用和修改都不方便

```html
<p style="color:red;font-size:60px;">不建议使用这种方式</p>
```

第二种方式：将样式写到head的style标签里面

通过css的选择器来选中元素并为其设置各种样式

可以同时为对个标签设置样式

但是不能跨页面使用

```html
<head>
<style>
    p{color:green}
    //对所有的p元素都改了
    </style>
</head>
```

第三种方式：外部样式表

可以将css样式编写到一个外部的css文件中，然后通过link标签来引入外部的css文件

外部样式表需要通过link标签进入引入，意味着只要想使用这些样式的网页 都可以对其进行引用，是样式可以在不同页面之间进行复用。

将样式编写到外部的css文件中，可以使用到浏览器的缓存机制，从而加快网页的加载速度，提高用户的体验。

css基本语法

style里面就不属于html的部分了，而遵守css的部分语法

/**/css注释

//html的注释

css的基本语法：

选择器 声明块

选择器，通过选择器可以选中页面中的指定元素

比如p就是选中所有的p元素

声明块，通过生命块来指定为元素设置的样式

名和值之间以：连接。以；结尾。

### 常用选择器

标签选择器

p{}、div{}

id选择器。

作用：根据元素的id属性值选中一个元素

语法：#id属性值{}

例子#box{}、#red{}

id是不能重复的，这样写不好，每个标签有唯一的id

class选择器：class一个标签属性，和id类似，不同的是class可以重复使用，可以通过class属性来为元素分组。

class比id更强大，class可以重复，id不能重复。

可以为一个元素指定多个class

```html
<h1 class=" blue abc">多个class</h1>
```

通配选择器

作用选中页面所有的元素。语法*

```css
//交集选择器
//训中复合多个条件的元素
//语法：选择器1{}
//标签.class选择器
//有元素选择器则必须标签.class选择器
div.red{}
//同时满足多个class
.a.b.c{}
/*div#boc{}*/
<div class>
</div>
/*选择器*分组（并集选择器）*/
h1,span{}

```

### 关系选择器

祖先元素：直接或间接包含后代元素

后代元素：直接或间接被祖先元素包含

兄弟元素：拥有相同的父元素

```css
div>span{}
//只要是div的span，都满足，都变化
div.box>span{}
//class是box的div，的span子元素
//语法：父元素>子元素
//很严格

//后代元素选择器
//祖先 后代
//只要是div里面的span都变化，无关乎是儿子还是孙子，不严格
div span{}

div>p>span{}

//选择则下一个兄弟
//语法：前一个+下一个
//p标签的紧挨着的下一个span，中间多一个别的元素则失效
p+span{}
//选择下面所有的兄弟元素
p~span{}

```

### 属性选择器

```html
<p title="abc">123</p>
```

把鼠标移到标题上会有提示

```css
p[title="abc"]{}
/*
[属性名]
[属性名=属性值]
[属性名^=属性值]以什么开头
[属性名$=属性值]以什么结尾
[属性名*=属性值]出现在任何位置
*/
```

### 伪类选择器

ul>li+table自动生成代码

：first-child表示第一个子元素

：last-child表示最后一个子元素

：nth-child（）选中第几个元素

  --特殊值：n 第n个 n的范围0到正无穷

​                    2n或even表示选中偶数位的元素

​                     2n+1或odd表示选中奇数位的元素  

![image-20210203111731149](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210203111731149.png)

：first-of-type找的是相同类型的第一个

：last-of-type找的是相同类型的最后一个

：nth-of-type找的是相同类型的第n个

：not（）否定伪类将符合条件的去除

### 超链接的伪类

1、没有访问过的链接

2、访问过的链接

```css
a:link{}
a:visited{}
a:hover{}
a:active
//link表示没有访问过的链接
//visited表示访问过的链接，由于隐私的原因，visited只能修改颜色，不能修改别的样式
//hover鼠标移入的状态
//active用来表示鼠标点击
```

### 伪元素

伪元素表示页面中一些特殊的并不真实存在的元素

：：first-letter表示第一个字母

：：first-line表示第一行

：：selection表示选中的内容

：：before元素的开始

：：after元素的最后

  -before和after必须结合content属性来使用 

![image-20210203113229508](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210203113229508.png)

```css
div：：before{}//永远在div的最前面

div：：after{}//永远在div的最后面
```

### 继承

样式的继承：我们为一个元素设置样式同时也会应用到它的后代元素上

继承是发生在祖先后代之间的

继承的设计是为了方便我们的开发，利用继承我们可以将一些统一的样式社会到共同的祖先元素上，这样只需设置一次即可让所有元素都具有该样式

注意：并不是所有的样式都会被继承：

比如 背景相关的，布局相关的这些样式都不会被继承。

### 选择器的权重

样式的冲突：通过不同的选择器，选中相同的元素，并且样式的值不同时，此时放生了样式的冲突。

选择器的权重

内联样式（标签内部style=""）  1000

id选择器（id#）  100

类和伪类选择器（class.）  10

元素选择器 （标签） 1

通配选择器  0

继承的样式 没有优先级

比较优先级时，需要将所有的选择器的优先级进行相加计算，最后优先级越高，则优先级显示（分组选择器单独计算）

选择器的累加不会超过最大的数量集，类选择器再高也不会超过id选择器

如果优先级计算相等，则优先使用靠下的选择器（代码位置靠下的）

可以再某一个样式的后面添加！important，则次样式会获得最高的优先级，超过内联样式，但是在开发中，这个要慎重使用，js都改不了

### 像素百分比



百分比：

也可以将属性值设置为相对于父元素属性的百分比

设置百分比会根据父元素的改变而改变

em和rem：

em是相对于自身字体大小来计算的

1em=1font-size

em会根据字体的大小的改变而改变

rem是相对于根元素的字体元素来计算的

### rgb

光的三原色红、绿、蓝

background-color：rgb（255,255,255）白色

rgba（红，绿，蓝，透明程度）

1表示完全不透明，0表示完全透明

十六进制的RGB:

语法：#红色绿色蓝色

颜色浓度通过00-ff

也可以通过两位两位重复进行简写

### HSL值和HSLA

在工业设计中使用hsl

H色相：（0-360）

S饱和度：（颜色的浓度0%-100%）

L亮度：（颜色的亮度0%-100%）

background-color：hsl（色相，饱和度，亮度）

background-color：hsla（色相，饱和度，亮度，透明度）

### 文档流（normal flow）

网页是多层的，一层压着一层

通过css可以分为每一层

用户只能看到最上面一层

最低下一层成为文档流，是网页的基础。我们所创建的元素默认都是在文档流中进行排列

我们的元素有两个状态：

在文档流中

不在文档流中（脱离文档流）

元素在文档流中的特点：

块元素

1、独占一行

2、默认宽度是父元素的全部

3、默认元素是被内容撑开（子元素）

行内元素

1、行内元素不会独占一行，只占自身的大小

2、从左向右排列，行内不能容纳所有的行内元素，则第二行继续从左向右

3、行内元素的默认宽度和高度都被内容撑开

### 盒子模型

css将页面的所有元素都设置为了一个矩形的盒子

将元素设置为矩形的盒子后，对也免得布局就变成了将不同的盒子摆放到不同的位置

每一个盒子都由以下几个部分组成：

内容区（content）：所有子元素和内容都在这里，width和height

内边距（padding）：内容区和边框之间的。padding-xxx，top、bottom、left、right内边距的设置会影响盒子的大小，背景颜色会延伸到内边距上。

边框（border）：属于盒子的边缘，边框里面属于盒子内部，反之外部。border-width边框宽度（默认值三个像素，可以指定四个方向的上的，像素上右下左顺时针，三个值不写左左右相等，两个值上下。border-xxx-width，xxx可以是top、right、bottom、left）。border-color边框颜色（上右下左规则和上面一样。若border-color省略不写则使用color）。border-style边框的样式（solid实线、dotted点状虚线、dashed虚线、double双线。默认值是none没有边框）。border简写属性没有顺序要求

```css
border：solid 10px orange
border-top：solid 10px orange
border-right：none
```

盒子的大小等于内容区+内边距+边框。外边距是不可见块，是盒子外部的。

外边距（margin）：

外边距不会影响盒子可见框的大小。但外边距会影响盒子的位置。margin-top上外边距，设置一个正直，元素会向下走。margin-left做外边距，设置一个正值，元素会向右移动。但设置右和下会移动其他元素，而不是自己的位置。margin-bottom下外边距，设置一个正值，下面的元素会向下移动。margin-right默认情况下不会有任何效果。

margin简写和padding一样

如果是负值向相反的方向移动

### 水平方向上的布局

决定属性：

margin-left+border-left+padding-left+width+margin-right+border-right+padding-right=父元素的宽度

等式必须成立，如多等式不成立，则称为过渡约束，则等式会自动调整：

调整的情况

这七个值没有auto的情况，则浏览器会自动调整margin-right的值

margin-left和width和margin-right会设置为auto

如果某个值设置为auto，则会自动调整auto的那个值使等式成立

如果宽度和一个外边距设置为auto，则狂赌会调整到最大，设置为auto的外边距会自动为0 

如果三个值都是auto，则外边距都是0，宽度最大

如果两个外边距设置为auto，宽度固定值，则外边距设置为相同的值。经常使用这种方法水平居中。

```css
width：xxxpx；

margin：0 auto；
```

### 垂直方向上的布局

默认情况下父元素的高度被内容隔开

如果子元素的大小超过了父元素，则子元素会从父元素中溢出

使用overflow属性来设置父元素如何处理溢出的子元素

可选值：

visible，默认值 子元素会从父元素中溢出，在父元素外部的位置上显示

hidden 移除内容将会被裁剪不会显示

scroll：生成两个滚动条，通过滚动条来查看完整的内容

auto：根据需要生成滚动条

overflow-x水平方向

overflow-y垂直方向

盒子模型：

外边距的重叠（折叠）：

垂直方向的外边距重叠现象

兄弟元素间相邻垂直外边距会取消两者之间的较大值（两者都是正值）（一正一负，取两者之和）（两者为负，取绝对值较大的）

兄弟元素的外重叠对开发是有利的，所以我们不需要进行处理

父子元素：

父子元素间相邻外边距，子元素的会传递给父元素（上外边距）

父子外边距的折叠会影响到也免得布局，必须要进行处理

1、用padding取代margin

2、不相邻，用border-top，再减去拉长的像素

### 行内元素的盒模型

行内元素不支持宽度和高度

行内元素可以设置padding，但垂直方向padding不会影响页面的布局

行内元素可以设置border，垂直方向的border不会影响页面布局

行内元素可以设置margin，垂直方向margin不会影响布局

把行内元素变成块元素：

display：

inline变成行内元素

block变成块元素

inline-block（行内块）将元素设置为行内块元素，既可以设置宽度和高度，又不会独占一行。不建议用

table将元素设置为一个表格

none元素不在页面中显示

visibility用来设置元素的显示状态

可选值：

visible 默认值，元素在页面中正常显示

hidden 元素在页面中隐藏不显示，但依旧占据页面的位置 

### 浏览器默认样式

默认浏览器样式会影响页面布局，通常情况下编写网页必须去掉浏览器默认样式（pc页面）

```css
body{margin:0;}

p{margin:0;}

ul{margin:0;

padding:0;

list-style：none；//去掉项目符号

}
//或者
*{
    margin:0;
    padding:0;
}
```

引入reset.css和normallize.css这是两个经典的重置样式表

text-decoration：none//去除超链接下划线

父元素12px，子元素14px。先继承，后重写，结果就是14px。

list-style：square//设置项目符号

![image-20210204213517753](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204213517753.png)

### 盒子的大小

box-sizing属性设置盒子的计算方式

可选值：

content-box默认值，宽度和高度用来设置内容区的大小

border-box 宽度和高度用来设置整个盒子可见框的大小，width和height指的是内容区和内边距，会压缩内容的大小

### 轮廓阴影和圆角

1、outline用来设置元素的轮廓线，用法和border一模一样

轮廓和边框不同的店，就是轮廓不会影响到可见框的大小。轮廓不会改变别的元素的位置。border会挤别的元素位置。

2、box-shadow：20px 10px  50px orange；

用来设置元素的阴影效果，阴影不会影响页面布局

第一个值 水平偏移量 设置阴影水平位置 正值向右负值向左

第二个值 垂直偏移量 设置阴影垂直位置 正值向右负值向左

第三个值 阴影的模糊半径

第四个值 阴影的颜色

3、border-radius用来设置圆角

border-xxx-xxx-radius

![image-20210204215717573](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204215717573.png)

四个值：左上顺时针

三个值：左上 剩下的 右下

两个值：左上右下  左下右上

### 浮动

通过浮动可以使一个元素香气父元素的左右移动

使用float属性来设置元素的浮动

可选值：none默认值不浮动。left元素向左浮动。right元素向右浮动。

注意：元素设置浮动之后，水平布局的等式便不需要强制成立。

元素设置浮动，会完全从文档流中脱离，不再占用文档流的位置，所以元素下边元素会自动上移。

![image-20210204220338743](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204220338743.png)

给上下的元素也设置float属性

![image-20210204220505464](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204220505464.png)

浮动的特点：

1、浮动元素会完全脱离文档流，不在占据文档流的位置

2、设置浮动以后回想父元素左侧或右侧移动

3、浮动元素默认不会从父元素移出

4、浮动元素左右移动，不会超过它前边的其他浮动元素

5、如果浮动元素的上边是一个没有浮动的块元素，则浮动元素无法上移

6、浮动元素不会超过上边的浮动的兄弟元素，最多就是和他一样高。

简单总结：浮动就上让页面中的元素水平排列，用于制作水平布局

### 浮动的特点

1、浮动不会盖住文字，文字汇总东环绕在元素的周围

可以利用浮动来设置文字环绕的效果。

2、元素设置浮动，会在文档流脱离，从文档流脱离，原色的特点也会变化。

脱离文档流特点：

块元素：

1、块元素不会独占一行

2、脱离文档流，块元素的宽度和高度默认都会被内容撑开

行内元素：

脱离文档流，会变成块元素，特点和块元素一样

.nav a:hover{

background-color:颜色//鼠标移入颜色改变

}

### 简单的布局

```html
<header>头部</header>
<main><main>
<main>
主体
    <nav>左侧导航</nav>
    <article>中间的内容</article>
    <aside>右侧边栏</aside>
</main>
<footer></footer>底部
```

重点：float属性。margin和各个部分width的大小

### 高度塌陷和BFC

高度塌陷问题：

在浮动布局中，父元素的默认高度是被子元素撑开的，

当子元素浮动后，其完全脱离文档流，子元素从文档流中脱离

将会无法撑起父元素的高度，导致父元素高度丢失

父元素高度丢失，下面的元素会自动上移，导致页面布局混乱

很常见的问题，这个问题必须要进行处理

BFC(block formatting context)会计格式化环境

BFC是一个css中的一个隐含的属性，可以为一个元素开启BFC，开启BFC会变成一个独立布局区域

开启BFC后的特点：

1、开启BFC不会被浮动元素所覆盖

2、开启BFC子元素和父元素外边距不会重叠

3、开启BFC元素可以包含浮动的子元素

通过特殊方法开启BFC：

1、设置元素的浮动（不推荐）

2、将元素设置为行内块元素（不推荐）

3、将元素overflow设置为非visible，hidden，副作用最小

![image-20210204224212649](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204224212649.png)

![image-20210204224303362](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204224303362.png)

### clear

如果不希望某个元素因为其他元素的浮动影响而改变位置

可以通过clear属性来清楚浮动的元素对当前元素所产生的影响

clear：

作用：清除浮动元素对当前元素所产生的影响

可选值：

left：清除左侧元素对当前元素的影响

right：清除右侧浮动元素对当前元素的影响

both：清除两侧中最大影响的那侧

原理：

设置清除浮动以后，浏览器会自动为元素添加一个上外边距，使得其位置不受其他元素影响

### 使用after伪类解决高度塌陷（基本完美的方式）

![image-20210204225351124](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204225351124.png)

用html解决css问题，解决高度塌陷。不建议使用。

```css
.box1::after{
    content:'';
    display:block;
    clear:both
}
```

这是用css解决css问题

### clearfix

table既可以解决高度塌陷，也可以解决外边距重叠

![image-20210204225956275](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210204225956275.png)

### 相对定位

定位（position）

定位是一种更加高级的布局手段

通过定位可以将元素摆放到页面的任意位置

使用position属性

可选值：

static默认值，元素静止的没有开启定位

relative 开启元素的相对定位

absolute 开启元素的绝对定位

fixed开启元素的固定定位

sticky开启元素的粘滞定位

相对定位：

position:relative

特点：

1、开启相对定位，如果不设置偏移量来设置元素的位置元素不会任何变化

2、相对定位参照语元素在文档流中的位置进行定位

3、相对定位会提升元素的层级

4、相对定位不会脱离文档流

5、相对定位不会改变元素的性质，行内还是块

偏移量offset

开启定位，通过偏移量来设置元素

top定位位置上边的位置

bottom定位位置下边的位置

left定位位置左边的位置

right定位位置右边的位置

### 绝对定位

position:absolute；

绝对定位的特点：

1、开启绝对定位，如果不设置偏移量元素的位置不会发生变化

2、开启后元素会从文档流脱离

3、绝对定位会改变元素的性质，行内变块，块的狂爱被内容撑开

4、绝对定位是元素提升一个层级

5、绝对定位相对于包含块进行定位。

包含块：正常情况下就是离当前元素最近的祖先块元素

绝对定位的包含块，离它最近的开启了定位的祖先元素，如果都没有就html元素。

### 固定定位

position:fixed;

固定定位也是一种绝对定位，所以固定定位大部分特点都和绝对定位一样。唯一不同的是固定定位永远参照浏览器的视口进行定位，不会随拖动滚动条而改变位置。

### 粘滞定位

position：sticky；

当元素的position属性设置为sticky时则开启元素的粘滞定位

粘滞定位和相对定位的特点基本一致，不同的是粘滞定位可以再元素到达某个位置是将其固定。

不能兼容所有浏览器，不推荐使用。

### 绝对定位元素的布局

水平布局：left+盒子（7个）+right=包容快区域的宽度

当我们开启了绝对定位后：

水平方向的布局等式就需要添加left和right

此规则与之前相比多了两个值

当发生过渡约束时，如果九个值没有auto则自动调整right使得等式满足。如果有auto，就调整auto所对应的那一项。

可以设置auto的值：margin、width、left、right

因为left和right的值默认是auto，座椅不知道left和right则等式不满足时，会自动调整这两个值

垂直方向也要满足：top+盒子（7个）+bottom

### 元素的层级

对于开启了定位元素，可以通过z-index属性来指定元素的层级

z-index需要一个证书作为参数，值越大元素等级越高

元素的层级越高越优先显示

z-index就是一个谁盖住谁的属性

如果各个元素的优先级一样，则靠下的盖住靠上的

祖先元素的层级再高也不会盖住后代元素

margin：100px auto；实现一个距离上面100px，居中对齐的效果

overflow：hidden；隐藏裁剪

position：absolute；//脱离文档流

.img-list li:nth-child(4){

z-index:1;}

通过调整层级来指定图片

行内元素不支持设定宽高，只有块元素支持设定宽高

float：left；也会脱离文档流

rgba（255,255,255，.6）透明的写法

开启相对定位，其子元素位置就是相对自己的

transparent颜色透明 

background-clip//将背景颜色是指内容区，边框环境内边距不再有背景色

### 字体族

p标签：

color颜色

font-size字体大小，font-size相关单位，em相当于当前元素的一个font-size，rem相当于根元素的一个font-size

font-family字体族：

serif衬线字体，更好看

sans-serif非衬线字体

monospace等宽字体

-制定字体类别，浏览器会自动使用该类别下的字体

有空格的字体加单引号，指定多个字体使用逗号隔开，有限使用第一个，第一个没有用第二个

windows下有fonts

```css
@font-face{
    //指定字体的名字
    font-family:'myfont';
    //服务器中字体的路径
    src:url('./font/路径') format("truetype");
}
/*font-face可以将服务器中的字体直接提供给用户去用
问题：
1、加载速度
2、版权。版权就体现在@font-face，而不是font-family
*/
```

### 图标字体iconfont

通过图片引入图标，但图片本身较大，使用不灵活

还可以将图片设置为字体，然后通过font-face的形式来对字体进行引入

这样我们就可以通过使用字体的形式来使用图标

fontawesome使用步骤：

1、下载

2、解压

3、将css和webfonts移动到项目中

4、将all.css引入到网页中

```html
<link rel="stylesheet" href="./fa/css/all.css">
<i class="fas fa-bell"></i>
或
<i class="fas fa-bell"></i>
//fas和fab是收费的
```

![image-20210207193835444](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207193835444.png)

![image-20210207194020543](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207194020543.png)

![image-20210207194209664](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207194209664.png)

### 图标库Fontawesome和阿里的iconfont

iconfont需要和原作者商量一下版权

![image-20210207201419994](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207201419994.png)

### 行高

行高指的是文字占有的实际高度

```css
//行高可以直接指定一个大小px em
//行高是指定的倍数，1.33
//字体框就是字体存在个各自，设置font-size实际上就是在设置字体的宽度
//行高会在字体框的上下平均分配
//可以将行高设置为和高度以一样的值，是单行文字在一个元素中垂直居中
//行高经常用来设置文字的行间距
//行间距=行高-字体大小
line-height:p;
```

### 字体的简写属性

如果不写行高，会默认用默认值，一个很小的值

字体大小和字体族必须写，别的随意可选

![image-20210207221617445](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207221617445.png)

### 文本的水平和垂直对齐

基线就是文字默认在基线上对齐

![image-20210207222033508](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207222033508.png)

### 文本的其他样式

![image-20210207222126316](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207222126316.png)

ie不兼容

![image-20210207222331342](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207222331342.png)

留白

![image-20210207222518541](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207222518541.png)

文本溢出显示省略号

![image-20210207223714906](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207223714906.png)

![image-20210207223732573](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207223732573.png)

解决高度塌陷问题

![image-20210207224151536](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207224151536.png)

指定样式的时候

.location .fas{

什么什么的

}

![image-20210207224938044](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207224938044.png)

![image-20210207225539131](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210207225539131.png)

### 背景

![image-20210208105426219](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208105426219.png)

background-clip背景的裁剪

![image-20210208144106777](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208144106777.png)

![image-20210208144339484](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208144339484.png)

![image-20210208144736414](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208144736414.png)

overflow:auto滚动条

![image-20210208145005342](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208145005342.png)

文字动，小猫不动

![image-20210208145117678](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208145117678.png)

![image-20210208145216365](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208145216365.png)

![image-20210208145326451](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208145326451.png)

![image-20210208145536766](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208145536766.png)

![image-20210208145502470](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208145502470.png)

margin：0 auto；

background-repeat：repeat-x；水平方向上重复

background-image：url（'路径'）；

或者直接

background：url（'路径'） repeat-x;

![image-20210208175202574](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208175202574.png)

![image-20210208175244854](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208175244854.png)

### 雪碧图

左中右三张图，同一个链接

![image-20210208223325154](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208223325154.png)

### 线性渐变

线性渐变默认水平方向

![image-20210208223934905](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208223934905.png)

![image-20210208224012065](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208224012065.png)

no-repeat没用，还是会重复

### 径向渐变

![image-20210208224223273](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208224223273.png)

![image-20210208224303874](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208224303874.png)

![image-20210208224325884](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208224325884.png)![image-20210208224533805](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208224533805.png)

![image-20210208224752526](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208224752526.png)



![image-20210208225129330](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208225129330.png)

导入图标字体

![image-20210208225515410](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208225515410.png)

偏移量，模糊半径

## HTML续

### 表格

![image-20210208232043228](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208232043228.png)

### 长表格

![image-20210208232247126](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208232247126.png)

thead和tbody和tfoot顺序可以互相转换

![image-20210208233531253](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208233531253.png)

### 表格的样式

边框合并，间距不生效

odd或2n+1

![image-20210208233838678](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208233838678.png)

![image-20210208233848735](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208233848735.png)

![image-20210208234118781](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208234118781.png)

### 表单

![image-20210208234431117](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208234431117.png)

![image-20210208234510474](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208234510474.png)

在form可以关闭所有自动补全

![image-20210208235037289](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210208235037289.png)

### 项目

```css
transition: height 3s;
```

当高度发生变化时，使用3秒钟进行过渡

overflow：hidden是高度为0

box-sizing默认是border-box，设置的是包含border的盒子，把border设置为none，就避免了

给input加padding，实现输入文本缩进效果

![image-20210209233455298](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210209233455298.png)



## 动画

过渡

auto不是一个有效属性

![image-20210209233927658](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210209233927658.png)

![image-20210209234252618](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210209234252618.png)

![image-20210209234447464](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210209234447464.png)

![image-20210209234533851](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210209234533851.png)

### 动画

![image-20210210184308505](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210210184308505.png)

![image-20210210184500975](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210210184500975.png)

![image-20210210184719845](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210210184719845.png)

![image-20210210184804460](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210210184804460.png)

两次时间有顺序，别的没有

图片会平铺，右上角那个点不会导致图片空白，同时需要注意不要设置repeat

![image-20210210235459008](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210210235459008.png)

![image-20210211000244904](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211000244904.png)

![image-20210211000359574](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211000359574.png)

![image-20210211000553953](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211000553953.png)

![image-20210211000809551](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211000809551.png)

![image-20210211001128456](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211001128456.png)

![image-20210211001244262](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211001244262.png)

![image-20210211001453176](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211001453176.png)

![image-20210211001643366](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211001643366.png)

### 鸭子表

![image-20210211001916348](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211001916348.png)

时下居中

![image-20210211002318380](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211002318380.png)

![image-20210211002335039](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211002335039.png)

### 复仇者联盟

![image-20210211002758572](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211002758572.png)

![image-20210211002825869](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211002825869.png)

### 裁剪

![image-20210211003234901](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211003234901.png)

### 弹性盒

![image-20210211174734971](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211174734971.png)

### 弹性容器的样式

![image-20210211174957997](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211174957997.png)

![image-20210211175122521](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211175122521.png)

![image-20210211175306848](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211175306848.png)

![image-20210211175959971](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211175959971.png)

![image-20210211180354804](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211180354804.png)

![image-20210211180444993](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211180444993.png)

### 弹性元素的样式

![image-20210211180751549](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211180751549.png)

![image-20210211180932477](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211180932477.png)

### 淘宝

justify-content:space-around设置主轴上的空白分布

display:flex;设置为弹性容器

### 像素

![image-20210211181747309](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211181747309.png)

### 移动端

![image-20210211182524996](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211182524996.png)

![image-20210211220058660](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211220058660.png)

![image-20210211220129679](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211220129679.png)

### vw单位

![image-20210211223913167](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211223913167.png)

### vw适配

![image-20210211225102969](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211225102969.png) 

### 实例页面

![image-20210211230405837](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211230405837.png)

![image-20210211230300251](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211230300251.png)

overflow：auto；设置图片滚动

![image-20210211231255708](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211231255708.png)

### 完成移动页面

![image-20210211231434673](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211231434673.png)

![image-20210211232102924](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211232102924.png)

![image-20210211232220712](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211232220712.png)

### 美图

![image-20210211232759320](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211232759320.png)