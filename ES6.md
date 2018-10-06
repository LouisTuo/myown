#### <center>js笔记</center>
1. this
this代表当前对象，但是在事件中代表的是当前对象
2. 排他性
* 使用id或者index
``` js
     window.onload = function () {
            var button = document.getElementsByClassName("button");
            for(var i = 0; i<button.length;i++){ //异步
                button[i].id = i;
                button[i].onclick = function () {
                    alert("你点了"+this.id+"按钮");
                }
            }
        }
```
*  使用闭包
``` js
window.onload = function () {
        var button = document.getElementsByClassName("button");
        for(var i = 0; i<button.length;i++){ //异步
            (function (i) {
                button[i].onclick = function () {
                    alert("你点了"+i+"按钮");
                }
            })(i);
        }
    }
```
3. 数组高级API
``` js
    //1.判断数组类型
    var arr = [1,2,4];
    console.log(typeof arr); //object
    console.log(arr instanceof Array); //true
    var arr2 = new Array();
    console.log(Array.isArray(arr2)); //Array判断是否是数组

    //2.toString 转化成string，每个用，分割
    var arr3 = [1,3,"我是","hello"];
    console.log(arr3.toString()); 
    
    //3. valueOf() 返回数组对象本身
    var arr4 =  arr.valueOf();
    console.log(arr4);
    
    //4.join() 方法用于把数组中的所有元素放入一个字符串
    var arr5 = arr3.join("-");
    console.log(arr5);

    //5.indexOf()和lastIndexOf()
```
4. 字符串string




#### <center>ES6</center>

##### 1.兼容性
 编译和转换：
- 在线编译
- 提前编译
##### 2.ES6语法
1. 变量
2. 函数
3. 数组
4. 字符串
5. 面向对象
6. Promise
7. generator
8. 模块化

##### 3.通信相关
```
数据交互的几种方式:
1. 表单
2. Ajax，麻烦，安全
3. JsonP，简单，有风险
4. WebSocket
```
