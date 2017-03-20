### 1 基本规范

<a name="缩进"></a>
#### 1.1 缩进
**建议** 使用一个Tab进行缩进，根据自己的编码习惯设置IDE/Text Editor indent => `tabsize = 4/2 whitespace`，这样无论是2空格缩进还是4空格都能保持一致，本规范推荐使用1 tabsize = 4 whitespace缩进。

```css
/* bad */
.container {
  color: red;
}

/* good */
.container {
    color: red;
}
```

**[⬆ back to top](#top)**
<a name="声明块"></a>
#### 1.2 声明块
**强制** 声明块左括号前加一个空格，右括号后新起一行。

```css
/* bad */
.container{color: red;}

/* good */
.container {
    color: red;
}
```

**[⬆ back to top](#top)**
<a name="空格"></a>
#### 1.3 空格
**强制** 属性后加一个空格。

```css
/* bad */
.container {
    color:red;
}

/* good */
.container {
    color: red;
}
```

**[⬆ back to top](#top)**
<a name="组合选择器"></a>
#### 1.4 组合选择器
**建议** 组合选择器应当为每个独立选择器换行。

```css
/* bad */
.header, .content, .footer, .slide {
    color: red;
}

/* good */
.header,
.content,
.footer,
.slide {
    color: red;
}
```

**[⬆ back to top](#top)**
<a name="颜色"></a>
#### 1.5 颜色
**强制** 使用16进制小写，能缩写使用缩写。

```css
/* bad */
.container {
    color: #FFFFFF;
    background-color: rgb(0,0,0);
}

/* good */
.container {
    color: #fff;
    background-color: #000;
}
```

**[⬆ back to top](#top)**
<a name="数值"></a>
#### 数值
**强制** 不要为值为0添加单位，小数点省略0。

```css
/* bad */
.container {
    font-size: 0px;
    opacity: 0.5;
}

/* good */
.container {
    font-size: 0;
    opacity: .5;
}
```

**[⬆ back to top](#top)**
<a name="注释"></a>
#### 注释
**建议** 注释前后分割符加上空格
```css
/*bad*/
/* good */
```
