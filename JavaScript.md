## JavaScript Code Style Guide
<a name="top"></a>

0. [基本编码风格](#基本编码风格)
	- [缩进](#缩进)
	- [空格与换行](#空格与换行)
	- [命名](#命名)
	- [分号](#分号)
	- [逗号](#逗号)
	- [引号](#引号)
	- [变量](#变量)
	- [比较](#比较)

1. [Objects](#objects)
2. [Arrays](#arrays)
3. [Functions](#functions)
4. [Class](#class)
5. [jQuery](#jquery)

<a name="基本编码风格"></a>
### 1 基本编码风格

#### 1.1 缩进
**建议** 使用一个Tab进行缩进，根据自己的编码习惯设置IDE/Text Editor indent => `tabsize = 4/2 whitespace`，这样无论是2空格缩进还是4空格都能保持一致。

```javascript
// bad
function foo() {
  console.log('test');
}

// good
function foo() {
    console.log('test');
}
```
**[⬆ back to top](#top)**
<a name="空格与换行"></a>
#### 1.2 空格与换行
**强制** 二元运算符两侧必须要有一个空格，一元运算符与操作对象之间不应该有空格。

```javascript
// bad
var z=x+y;
var a = ! z;

// good
var z = x + y;
var a = !z;
```

**强制** 块代码`{`之前必须要有一个空格。

```javascript
// bad
if(condition){}

// good
if (condition) {}
```

**强制**`if / else / for / while / function / switch / do / try / catch / finally` 关键字后，必须有一个空格。

```javascript
// bad
function(){}
while(true){}

// good
function () {}
while (true) {}
```
**强制** 在对象创建时，属性中的 : 之后必须有空格，: 之前不允许有空格。

```javascript
// bad
var obj = {
    a : 1,
    b:2,
    c :3
};

// good
var obj = {
    a: 1,
    b: 2,
    c: 3
};
```
**建议** 非匿名函数声明及调用函数名与()之前不应该存在空格。

```javascript
// bad
function foo () {}
foo ();

// good
function foo() {}
foo();
```
**强制** 函数参数之间由逗号空格隔开。

```javascript
// bad
function foo(a,b,c) {}
foo(a,b,c);

// good
function foo(a, b, c) {}
foo(a, b, c);
```

**建议** 功能逻辑不同的代码块应该换行，提高阅读性。

```javascript
// bad
function getDataset(el) {
    if (el === undefined) {
        return;
    }
    // logic
}

// good
function getDataset(el) {
    if (el === undefined) {
        return;
    }

    // logic
}
```
**强制** 在 `if / else / for / do / while` 语句中，即使只有一行，也不得省略块 {...}。

```javascript
// bad
if (condition) return;

// good
if (condition) {
    return;
}
```
**[⬆ back to top](#top)**
<a name="命名"></a>
#### 1.3 命名
**强制** 变量、函数使用camelCase

```javascript
// bad
var usertoken;
var function = getusertoken() {};

// good
var userToken;
var function = getUserToken() {};
```

**强制** 类、组件使用PascalCase命名。

```javascript
// bad
var myCard = function(name) {
    this.name = name;
}

// good
var MyCard = function(name) {
    this.name = name;
}
```
**强制** 枚举变量使用PascalCase，属性使用全大写。

```javascript
// bad
var testState = {
    a: 1,
    b: 2
};

// good
var TestState = {
    A: 1,
    B: 2
};
```
**[⬆ back to top](#top)**
<a name="分号"></a>
#### 1.4 分号
**强制** 所有语句、函数表达式后面必须加分号，IIFE(immediately invoked function expressions)格式模块前后必须加一个分号[#1](https://github.com/Jiavan/style-guide/issues/1)。

```javascript
// bad
var a = 0
var foo = function() {}
(function() {})()

// good
var a = 0;
var foo = function() {};
;(function() {})();
```
**[⬆ back to top](#top)**
<a name="逗号"></a>
#### 1.5 逗号
**建议** 数组元素或者对象属性最后一个不要多引入一个逗号。

```javascript
// bad
var obj = {
    a: 1,
    b: 2,
};
var arr = [1, 2, 3,];

// good
var obj = {
    a: 1,
    b: 2
};
var arr = [1, 2, 3];
```
**[⬆ back to top](#top)**
<a name="引号"></a>
#### 1.6 引号
**强制** 字符串类型值使用单引号。

```javascript
// bad
var str = "test";
var arr = ["test0", "test1"];
var obj = {
    a: "test",
    b: "test"
};

// good
var str = 'test';
var arr = ['test0', 'test1'];
var obj = {
    a: 'test',
    b: 'test'
};
```
**[⬆ back to top](#top)**
<a name="变量"></a>
#### 1.7 变量
**强制** 在模块中使用var来声明一个非全局变量，全局变量请挂在在window对象上。

```javascript
// bad
a = 1;

// good
var a = 1;
window.b = 2;
```

**建议** 都使用var来声明一个变量。

```javascript
// bad
var name, age, email;

// bad
var name,
    age,
    email;

// good
var name;
var age;
var email;
```
**[⬆ back to top](#top)**
<a name="比较操作"></a>
#### 1.8 比较操作
**强制** 使用`===``!==`来进行比较而不是`==``!=`。

```javascript
// bad
var x = '0';
x == 0; // => true

// good
var x = '0';
x === 0; // => true
```
**[⬆ back to top](#top)**
<a name="objects"></a>
### 2 Objects
**建议** 使用字面意义的方式来创建对象。

```javascript
// bad
var obj = new Object();

// good
var obj = {};
```
**[⬆ back to top](#top)**
<a name="arrays"></a>
### 3 Arrays
**建议** 使用字面意义的方式创建数组。

```javascript
// bad
var arr = new Array();

// good
var arr = [];
```

**建议** 使用slice方法拷贝数组。

```javascript
var len = items.length;
var itemsCopy = [];
var i;

// bad
for (i = 0; i < len; i++) {
    itemsCopy[i] = items[i];
}

// good
itemsCopy = items.slice();
```

**建议** 添加数组元素使用push方法。

```javascript
// bad
arr[arr.length] = 'test';

// good
arr.push('test');
```

**建议** 使用slice方法将一个类数组对象转换为数组。

```javascript
function foo() {
    var args = Array.prototype.slice.call(arguments);
}
```
**[⬆ back to top](#top)**
<a name="functions"></a>
### 4 Functions
**强制** 不要在if语句中声明一个函数，应该使用函数表达式。

```javascript
// bad
if (flag) {
    function foo() {}
}

// good
if (flag) {
    var foo = function foo() {};
}
```
**建议** 函数表达式后面跟上函数名，这会有利于调试bug。

```javascript
// bad
var foo = function() {};

// good
var foo = function foo() {};
```
**[⬆ back to top](#top)**
<a name="class"></name>

### 5 Class
**建议** 不要使用下划线来标识一个私有成员方法或者成员属性，JavaScript中根本不存在私有成员的概览，实际上他们都是public的。

```javascript
// bad
function Person() {
    this._name; // => public
    this._getName = function() {}; // => public
}

// good
function Person() {
    this.name; // => public
    this.getName = function() {}; // => public
}
```
**[⬆ back to top](#top)**
<a name="jquery"></a>
### 6 jQuery
**强制** jQuery对象前加$进行标识。

```javascript
// bad
var body = $('body');

// good
var $body = $('body');
```

**强制** 缓存jQuery对象。

```javascript
// bad
$('.container').addClass('test');
$('.container').css({'background-color': 'pink'});
$('.container').hide();

// good
var $container = $('.container');
$container.addClass('test').css({'background-color': 'pink'}).hide();
```
**[⬆ back to top](#top)**

----
## 参考
- Airbnb [https://github.com/airbnb/javascript](https://github.com/airbnb/javascript)
- fex-team [https://github.com/fex-team/styleguide/blob/master/javascript.md](https://github.com/fex-team/styleguide/blob/master/javascript.md)
