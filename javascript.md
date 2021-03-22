# javascript

F:\BaiduNetdiskDownload\javascript\源码、课件、笔记、工具\源码、课件、笔记、工具\源码

### js简介

![image-20210219095748287](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219095748287.png)

![image-20210219095830753](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219095830753.png)

![image-20210219095941568](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219095941568.png)

![image-20210219100009689](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100009689.png)

![image-20210219100019848](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100019848.png)

![image-20210219100116737](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100116737.png)

![image-20210219100131166](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100131166.png)

![image-20210219100103615](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100103615.png)

### helloworld

![image-20210219100432889](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100432889.png)

三条语句按顺序执行

### js编写位置

![image-20210219100716793](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100716793.png)

![image-20210219100859657](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219100859657.png)

![image-20210219101937489](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219101937489.png)

### 类型

null是Object

undefined是undefined

null和undefined没有tostring，只能调用string方法

### 运算

加法转化为string拼串，其他算法都转化为number

### 优先级

![image-20210219114632260](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219114632260.png)

### 求质数

```
var result = Math.sqrt(97);
//求97的指数，先求开方
//1*97
//2*48.5
//...
//9*1.0x
//10*9.7
//所以求到9就停，之后的不用再求了
```

```
//终止计时器
//console.timeEnd()用来停止一个计时器，需要一个计时器的名字作为参数
console.timeEnd("test");
```

### 对象属性

![image-20210219155406314](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219155406314.png)

## 函数

![image-20210219160153729](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219160153729.png)

这是一种写法，构造函数方法，但不太好

### 函数调用

```
function fun3(){
   //在函数内部再声明一个函数
   function fun4(){
      alert("我是fun4");
   }
   
   //将fun4函数对象作为返回值返回
   return fun4;
}

a = fun3();
//console.log(a);
//a();
fun3()();
```

### 立即执行函数

![image-20210219161441700](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219161441700.png)

### 枚举对象的属性

![image-20210219161758276](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219161758276.png)

### 变量的提前声明

![image-20210219162010025](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219162010025.png)

var和function会被最先执行

### this

this就是window

```
/*
 * 解析器在调用函数每次都会向函数内部传递进一个隐含的参数,
 *     这个隐含的参数就是this，this指向的是一个对象，
 *     这个对象我们称为函数执行的 上下文对象，
 *     根据函数的调用方式的不同，this会指向不同的对象
 *        1.以函数的形式调用时，this永远都是window
 *        2.以方法的形式调用时，this就是调用方法的那个对象
 */
```

### 工厂方法创建对象都是object对象

```
/*
 * 使用工厂方法创建对象
 *     通过该方法可以大批量的创建对象
 */
```

![image-20210219164342716](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219164342716.png)

### 原型对象

![image-20210219165234378](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219165234378.png)

类.prototype.属性

将对象共有的属性添加到类中

![image-20210219165354890](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219165354890.png)

原型的原型就是尽头了

### 数组

```
/*
 * 修改length
 *     如果修改的length大于原长度，则多出部分会空出来
 *  如果修改的length小于原长度，则多出的元素会被删除
 */
```

### 数组方法

pop和push在后面加减，unshift（加）和shift（减）往前加减

### foreach方法

```
//创建一个数组
var arr = ["孙悟空","猪八戒","沙和尚","唐僧","白骨精"];

/*
 * forEach()方法需要一个函数作为参数
 *     - 像这种函数，由我们创建但是不由我们调用的，我们称为回调函数
 *     - 数组中有几个元素函数就会执行几次，每次执行时，浏览器会将遍历到的元素
 *        以实参的形式传递进来，我们可以来定义形参，来读取这些内容
 *     - 浏览器会在回调函数中传递三个参数：
 *        第一个参数，就是当前正在遍历的元素
 *        第二个参数，就是当前正在遍历的元素的索引
 *        第三个参数，就是正在遍历的数组
 *        
 */
arr.forEach(function(value , index , obj){
   console.log(value);
});
```

### sort方法

![image-20210219172113416](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219172113416.png)

这是升序的，把1和-1交换就是逆序的

![image-20210219172255304](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219172255304.png)

更优化的方法

### call和apply

![image-20210219172647265](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219172647265.png)

### argument一个神奇的参数

通过形式参数函数方法，调用实际参数

![image-20210219173016410](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219173016410.png)

判断该当前的函数是不是fun

### DOM

![image-20210219194120400](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219194120400.png)

![image-20210219194205715](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219194205715.png)

### 文档的加载

![image-20210219200458698](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219200458698.png)

### 两个文本方法的区别

![image-20210219202305936](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219202305936.png)

### a的索引问题

![image-20210219210803586](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219210803586.png)

### 样式修改

![image-20210219211047130](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219211047130.png)

![image-20210219212231009](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219212231009.png)

![image-20210219213615723](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210219213615723.png)

# javascript高级

### 原型链

![image-20210223161910069](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210223161910069.png)

![image-20210223163210893](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210223163210893.png)

![image-20210223164231801](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210223164231801.png)

# js模块化

F:\BaiduNetdiskDownload\js模块化\源码\code\code

npm init -y或npm init 创建package.json

npm install uniq --save

这里的--save表示把依赖写道package.json里面

node app.js运行指令