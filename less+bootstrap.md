# css中的less

有一个插件叫做easy-less

![image-20210211164856296](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211164856296.png)

![image-20210211165641081](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211165641081.png)

![image-20210211170845868](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211170845868.png)

![image-20210211170907471](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211170907471.png)

![image-20210211171549482](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211171549482.png)

![image-20210211171839847](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211171839847.png)

![image-20210211171748299](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211171748299.png)



# less

less，sass，stylus

less既可以在nodejs上面，也可以在浏览器上面

http://koala-app.com/这是一个工具叫做考拉，能把less编译成css

```less
/*这是想暴露出去的注释，可以编译进去*/

//这是见不得人的注释，这种类型的注释不能够被编译，是仅供开发人员看的
```

```less
/*这是定义变量的方法*/
/*指定颜色，参数，选择器*/
@color:deeppink;
@m:margin;
@selector:#wrap;
```

嵌套模式要用&符号

less的混合：

1、普通混合

2、不带输出的混合

3、带参数的混合

4、带参数并有默认输出的混合

5、带多个参数的混合

6、命名参数，在下面的形参里面（@c：pink）

7、匹配模式，在共有的函数里面使用@_

8、arguments变量

```less
.border(@1,@2,@3){
  border:@arguments;//这个函数就是这么用的，等同于border:@1,@2,@3;
}
#wrap .sjx{
  .border(1px,solid,black);
}
```

rel是stylesheet，type是text/css这个不能改

less运算：

less可以进行加减乘除运算

```less
#wrap .sjx{
  width: (100+100px);
}
```



![image-20210211234922762](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211234922762.png)

less避免编译

![image-20210211233348423](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233348423.png)

![image-20210211233441904](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233441904.png)

![image-20210211233528523](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233528523.png)

![image-20210211233545801](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233545801.png)

![image-20210211233602549](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233602549.png)

![image-20210211233623501](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233623501.png)

![image-20210211233259082](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233259082.png)

![image-20210211233643443](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233643443.png)

![image-20210211233848992](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233848992.png)

![image-20210211233906627](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211233906627.png)

![image-20210211234109517](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211234109517.png)

![image-20210211234159686](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211234159686.png)

![image-20210211234940990](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211234940990.png)



避免编译

![image-20210211234847398](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210211234847398.png)

# Bootstarp

![image-20210213111308892](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210213111308892.png)

![image-20210213110817646](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210213110817646.png)

栅格化系统

![image-20210213110919323](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210213110919323.png)

![image-20210213112514806](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210213112514806.png)

![image-20210213112854611](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210213112854611.png)

F:\BaiduNetdiskDownload\bootstrap\code\pre\03_bootstrap\demo

![image-20210214111229203](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210214111229203.png)

行&列

![image-20210214112730832](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210214112730832.png)

![image-20210214113026771](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210214113026771.png)

![image-20210214113237429](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210214113237429.png)

![image-20210214163739178](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210214163739178.png)

```html
<!--col-lg-pull-9偏移9个col，pull修改right-->
<!--col-lg-push-9偏移9个col，push修改left-->
向左拉，向右推
```

![image-20210215000706713](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215000706713.png)

![image-20210215000739735](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215000739735.png)

自定义栅格系统

把所有的col改为damu-col

响应式工具

![image-20210215172445557](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215172445557.png)

到一定的值会隐藏

![image-20210215172607021](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215172607021.png)

![image-20210215172719307](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215172719307.png)

所以自定义的话只写.clearfix不加（）

![image-20210215220445469](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215220445469.png)

![image-20210215221813869](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215221813869.png)

我们会默认width：100%和auto差不多

![image-20210215224127992](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215224127992.png)

![image-20210215224616618](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215224616618.png)

![image-20210215224849672](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215224849672.png)

![image-20210215224939795](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215224939795.png)

bootstrap-3.3.7/less/variables.less

这个文件里面修改槽宽，然后编译bootstrap-3.3.7/less/bootstrap.less这个文件

![image-20210215225818616](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215225818616.png)

这样一种方式不修改源码，修改了变量槽宽

最后在html的link修改路径

![image-20210215231556736](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215231556736.png)

![image-20210215234034512](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215234034512.png)

这里是参数

还有jqury的方法

![image-20210215234515867](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215234515867.png)

![image-20210215234812309](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\image-20210215234812309.png)

jqurey的写法