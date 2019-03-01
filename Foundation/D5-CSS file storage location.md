## CSS文件存放位置

### 外链CSS

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
