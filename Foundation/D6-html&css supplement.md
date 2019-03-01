## html&css的补充

### 布局标签的补充

div标签
>双标签
>容积大

span标签
>双标签
>容积小

**段落标签里不能包含标题标签**

### HTML元素分类

块元素
>同时存在多个块元素时，每个块元素都会独占一行显示，且默认情况下其宽高属性起作用

行内元素
>同时存在多个行内元素时，这些元素都会显示在同一行并自动折行，默认情况下其宽高属性不起作用（背景属性起作用）

行内块元素
>同时存在多个行内块元素时，这些元素会显示在同一行，默认情况下其宽高属性起作用

### 元素展示类型的转换

display属性值
>转换为块元素：block
>转换为行内元素：inline	
>转换为行内块元素：inline-block

```html
<head>
	<style type="text/css">
		span{
			width:100px;
			height:100px;
			
			display:block;		
		}
	</style>
</head>  
```

### 简单选择器权重

id选择器 > 类名选择器 > 标签名选择器

### CSS的三大特性

继承性：子元素可以继承父元素的样式，且不是所有属性都能被继承，且不是所有子元素都有继承性  
层叠性：在权重相同的情况下，同一元素，同一属性，后写的CSS样式会覆盖先写的CSS样式
>该情况下，先写的CSS样式中若有后写的CSS样式中没有的属性，则该属性未被覆盖，即只覆盖相同的元素属性，未覆盖到的仍保留   
>> 先写的：height:100px;  后写的：没有height属性；   --> 显示：height:100px;  

优先级：！important>行内样式>id选择器>类选择器>标签选择器>通配符>继承  

### CSS文件存放位置
外链CSS

**在当前html页面使用link单标签引入外部CSS文件**
>link单标签放在<head>内<title>下

html文件：
```html
<head>
	<link rel="stylesheet" type="text/css" href="XXX.css" />    <!-- href的值使用相对路径 -->
</head>
```

css文件：  **注意外链CSS文件当中不需要写style标签**
```  
div{
	width:100px;
	height:100px;
	background-color:seagreeen;
}
```

### 行内CSS

将CSS代码写在具体的html标签上
>**style的内容不能手段换行**

```html
<html>
	<body>
		<div style="color:red;width:100px;height:50px;background-color:pink;">div标签</div>
		<!-- style="A;B;C;D" -->
	</body>
</html>
```

### CSS存放位置不同时的权重

!important可以将样式的权重提至最高（**感叹号是英文模式**）  
>p{color:pink!important;}

在没有!important的情况下，行内CSS的权重最高，而外链CSS和内嵌CSS的权重取决于各自所使用的选择器的权重
