# 学习一门语言 
## <font color=red>JavaScript是弱类型 解释性语言,是基于对象的一门编程语言。</font>
## 变量
- 定义变量  `给变量赋值是什么类型 这个变量就是什么类型`
 ``` js
 let num = 10;  //完整的表达式 let 关键字  用来定义变量  = 号  用来给变量赋值
    console.log(num);
    let str = '中华民族伟大复兴！'; //单引号和双引号 在js里 没有区别 
    console.log(str);
    let bEat = true; 
    console.log(bEat);
    //定义一个对象 键值对形式  key ： value  
    let obj = {
        'name' : '李白',
        age : 2000    
    }
    console.log(obj.name);
    //函数  1 定义函数  2 执行函数
    //定义一个函数 function+函数名 + 小括号 + 大括号
    function func(){
        let num1 = 100;
        console.log(num1);
    }
    //调用函数  函数名+小括号
    func();
    // 函数参数   数学 y = f（x）  
    function getNum(n){
        n *= 10;
        console.log(n);
    }
    getNum(20);  //意味着把20 赋值给 n
``` 
## 数据类型
# 数据类型
- 数值型 `number`
- 字符串型 `string` 
- 布尔值 `boolean`
- 对象 `Object`
- 函数 `function`
# 运算符
## 运算符号：
- 单目：`只有一个表达式`
```js
    let num = 100;
 
    console.log(num);

    let n = 200;
    n++;  // ++ -- 
    console.log(n);
```
- 双目：`两个表达式组成 + ，-， *， /，%`
 ```js
  let num1 = 100;
    let num2 = 200;
    let sum = num1 + num2;
    let n = 100;
    let m = n % 3; // 1
    console.log(sum,m);
    num %= 2;  //num自己乘2 并且赋值给自己  += -= /= %= 
```
- 三目：`三个表达式组成`
```js
    let a = 1;
    let b = 10;
    let num = a>b ? a : b; //判断第一个表达式是否为真
```
# 语句
 
## 顺序结构：`代码从上往下，一行一行地执行。`
## 选择结构：`条件语句，选择一些代码来执行。`
### if 语句   `选择是否执行代码块里的内容`
```js
    if(10< 20){ //小括号内的表达式 如果为真 就执行大括号里的内容 反之不执行
        console.log('输出一行字');
    } 
```

### if else 语句
```js
    if(10 > 20){ //如果小括号内为真 那么执行这个大括号的内容
        console.log(1111);
    }
    else{ //否则 就执行这个大括号的内容
        console.log(2222);
    }
```
### if  else if  else if ………… else`需要找到一个小括号里是真的表达式 执行对应的大括号里的内容如果都没有找到 就什么都不执行`
 ```js
    if ('A') {
        //角色向左走
    }
    else if('D'){
        //角色向右走
    }
    else if('S'){
        //角色向下走
    }
    else if('W'){
        //角色向上走
    }
    else {
        //默认
        //return;
    }
```
### switch语句  `break一定要有 `
```js
 switch (key) {
        case 'A':
            //角色向左走
            break;
        case 'S':
            //角色向下走
            break;
        case 'D':
            //角色向右走
            break;
        case 'W':
            //角色向上走
            break;
        default:
            //默认
            break;
    }
```
- 循环结构：`用来重复执行一些代码`
### for `小括号 三个表达式`
    1. 定义一个变量 并初始化值
    2. 判断条件 如果是真 就执行大括号里的代码 
    3. 档大括号里的代码 执行完毕 就会执行表达式3
    4. 表达式3执行完之后 再判断表达式2是否为真 如果为真  就执行大括号里的代码………………
    5. 如果表达式2为假 那么 结束这个for语句
```js
    for (let i = 0; i < 10; i++) {
        let a;
        let b;
        console.log(i);
    }
```
### 嵌套for循环

```js
    for (let i = 1; i < 10; i++) {
        for (let j = 1; j <= i; j++) {
            document.write(j + 'x' + i + '=' +  i * j + '&nbsp&nbsp&nbsp&nbsp');   
        } 
        document.write('</br>');
    }
```
### while循环
`当小括号内的表达式 为真 那么执行大括号里的代码 执行完之后 
    再次判断小括号内的表达式 如果为真  那么执行大括号里的代码 执行完之后
    如果小括号内为假  结束while语句`
```js
    let num  = 0;
    while (num<10) {
        console.log(num);
        num ++;
    }
```
### 嵌套while
```js
    let i = 1;
    let j = 1;
    while (i<10) {
        while (j<=i) {
            j++;   
            
            console.log(i*j);
        }
        i++;
    }
```
## 跳转语句：break, continue,return
### break : `打断循环 结束循环`
```js
    for (let i = 0; i < 10; i++) {
        if (i===8) {
            break; //  当i的值为8时 跳出循环 结束for语句
        }
        console.log(i);
    }

    for (let i = 0; i < 10; i++) {
        if (i===8) {
            continue; //  当i的值为8时 什么都不执行 直接结束代码块 进入循环的下一次
        }
        console.log(i);
    }
```
### return`函数返回值`
```js
    function getAge(){
        return 10;
    }

    let a = getAge();
    console.log(a);

    function show(){
        console.log(1111);
        return; //结束函数
        console.log(2222);
    }
    show();
```
    
