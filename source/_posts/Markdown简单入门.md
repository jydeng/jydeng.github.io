---
title: Markdown简单入门
date: 2017-12-29 17:34:12
tags: 工具
---

# Markdown 简单入门
[TOC]

## 标题
在行首插入 1到6个 ```#```，分别表示标题1到标题6

### 有序列表
在行首增加 ```1.``` ```2.``` ```3.``` 数字加上英文句点,表示有序列表
1. 有序列表
2. 有序列表
3. 有序列表

### 无序列表
在行首添加 ```*``` 或者 ```-``` 表示无序列表
* 无序列表
- 无序列表

### 插入图片
直接粘贴图片,或者可以使用标准的Markdown语法 ```![](link) ```
![](http://cdn.wiz.cn/wp-content/uploads/2015/06/wiz_logo.png) 

### 插入链接
链接和图片类似 ```[txt](link)```
[为知笔记](http://www.wiz.cn)

### 字体效果
粗体：文字前后添加 ```**```
斜体：文字前后添加 ```*```
删除线：文字前后添加 ```~~```

### 引用
在行首添加 ```>``` 表示引用

### 表格
使用换行和 | 来表示表格
```| 姓名|年龄 | 职业 || 张三 | 18| 码农 |```

| 姓名|年龄 | 职业 |
|-|-|-|
| 张三 | 18| 码农 |

### 代码
使用键盘左边三个反单引号表示代码，也可以在后面指定语言

### 提取目录
使用```[TOC]```会自动提取目录，开头的目录就是这样实现的，这个功能好强大，瞬间被圈粉了


### Mathjax 公式
可以创建行内公式 ```$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$``` 
块级公式
```$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$1.  `$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$```

$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$

$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$1.  `$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$`

### 流程图
flow
st=>start: Start
e=>end: End
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes or No?
io=>inputoutput: catch something...
st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1 
将以上流程代码用三个反单引号包裹即可

注意：
1) 关键词（start、end、operation、subroutine、condition和inputoutput）后的冒号后要紧跟一个空格。
2) 使用->来连接两个元素，对于condition类型，有yes和no两个分支，如示例中的cond(yes)和cond(no)。
更多关于流程图的语法说明：http://adrai.github.io/flowchart.js/


```flow
st=>start: Start
e=>end: End
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes or No?
io=>inputoutput: catch something...
st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1
```

### 时序图
sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
将以上流程代码用三个反单引号包裹即可
更多关于时序图的语法说明：http://bramp.github.io/js-sequence-diagrams

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!```

### 脚注
在要添加注释的词语后面增加```[^1]```,结尾加上 ```[^1]:注释内容```
这个在为知笔记上支持好像不是很好











