# 饥人谷JS基础语法（第一节课）
## 什么是表达式和语句
一般来说，表达式与语句的区别不是特别明显。 表达式是一组代码的集合，它返回一个值。（ps：定义可能不好理解，可以参考一下示例：[js的表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_Operators)）

JavaScript 程序的执行单位为行（line），也就是一行一行地执行。一般情况下，每一行就是一个语句。它是为了完成某种任务而进行的操作
## 标识符的规则
标识符（identifier）指的是用来识别各种值的合法名称。最常见的标识符就是变量名。

标识符有一套命名规则，不符合规则的就是非法标识符。JavaScript 引擎遇到非法标识符，就会报错。

简单说，标识符命名规则如下：
>第一个字符，可以是任意 Unicode 字母（包括英文字母和其他语言的字母），以及美元符号（$）和下划线（_）。
>第二个字符及后面的字符，除了 Unicode 字母、美元符号和下划线，还可以用数字0-9。
## if else 语句
if else 语句是一种条件语句，if结构先判断一个表达式的布尔值，然后根据布尔值的真伪，执行不同的语句。在if代码块后面，还可以跟一个else代码块，表示不满足条件时，所要执行的代码。
## while for 语句
While语句包括一个循环条件和一段代码块，只要条件为真，就不断循环执行代码块。
```javascript
while (条件) {
  语句;
}
```
## break continue
break语句和continue语句都具有跳转作用，可以让代码不按既有的顺序执行。

break语句用于跳出代码块或循环。

```javascript
var i = 0;

while(i < 100) {
  console.log('i 当前为：' + i);
  i++;
  if (i === 10) break;
}
```
上面代码只会执行10次循环，一旦i等于10，就会跳出循环。


continue语句用于立即终止本轮循环，返回循环结构的头部，开始下一轮循环。
```javascript
var i = 0;

while (i < 100){
  i++;
  if (i % 2 === 0) continue;
  console.log('i 当前为：' + i);
}
```

上面代码只有在i为奇数时，才会输出i的值。如果i为偶数，则直接进入下一轮循环。

如果存在多重循环，不带参数的break语句和continue语句都只针对最内层循环。
## label
JavaScript 语言允许，语句的前面有标签（label），相当于定位符，用于跳转到程序的任意位置，标签的格式如下。

```javascript
label:
  语句
```
