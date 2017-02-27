## JavaScript Code Style

### 1 基本编码风格

#### 1.1 缩进
**建议**使用一个Tab进行缩进，根据自己的编码习惯设置IDE/Text Editor indent => `Tab = 4/2 whitespace`。

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

#### 1.2 空格与换行
**强制**二元运算符两侧必须要有一个空格，一元运算符与操作对象之间不应该有空格。

```javascript
// bad
var z=x+y;
var a = ! z;

// good
var z = x + y;
var a = !z;
```

**强制**块代码`{`之前必须要有一个空格。

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
**强制**在对象创建时，属性中的 : 之后必须有空格，: 之前不允许有空格。

```javascript
// good
var obj = {
    a: 1,
    b: 2,
    c: 3
};

// bad
var obj = {
    a : 1,
    b:2,
    c :3
};
```
**建议**非匿名函数声明及调用函数名与()之前不应该存在空格。

```javascript
// bad
function foo () {}
foo ();

// good
function foo() {}
foo();
```
**强制**函数参数之间由逗号空格隔开。

```javascript
// bad
function foo(a,b,c) {}
foo(a,b,c);

// good
function foo(a, b, c) {}
foo(a, b, c);
```

**建议**功能逻辑不同的代码块应该换行，提高阅读性。

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
**强制**在 `if / else / for / do / while` 语句中，即使只有一行，也不得省略块 {...}。

```javascript
// bad
if (condition) return;

// good
if (condition) {
	return;
}
```

#### 1.3 命名
**强制**变量、函数使用camelCase

```javascript
// bad
var usertoken;
var function = getusertoken() {};

// good
var userToken;
var function = getUserToken() {};
```

**强制**类、组件使用PascalCase命名。

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
**强制**枚举变量使用PascalCase，属性使用全大写。

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
####
