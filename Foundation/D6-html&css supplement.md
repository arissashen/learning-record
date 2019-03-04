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
>转换为不显示元素：none  

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

### CSS的三大特性

继承性：子元素可以继承父元素的样式，且不是所有属性都能被继承，且不是所有子元素都有继承性  
层叠性：**在权重相同的情况下**，同一元素，同一属性，后写的CSS样式会覆盖先写的CSS样式
>该情况下，先写的CSS样式中若有后写的CSS样式中没有的属性，则该属性未被覆盖，即只覆盖相同的元素属性，未覆盖到的仍保留   
>> 先写的：height:100px;  后写的：没有height属性；   --> 显示：height:100px;  

优先级：！important>行内样式>id选择器>类选择器>标签选择器>通配符>继承  

### 文字样式

行高：line-height
>将行高大小设置为当前元素的高度时，可实现单行文本在当前元素中垂直方向居中显示

字体颜色：color

字体大小：font-size
>单位为px
>浏览器有一个最小的显示字体（Chrome为12）

水平对齐方式：text-align
>值：left、center、right

字体粗细：font-weight
>值：数值（100-900）、关键字（正常normal、加粗bold）

字体类型：font-family
>值：宋体 等

```html
<head>
	<meta charset="UTF-8">
	<title>文字样式</title>
	<style type="text/css">
		div{
			color:#000;    <!-- 字体颜色 -->
			width:80px;
			height:200px;
			background: mistyrose;
			line-height: 200px;    <!-- 单行文本在当前元素中垂直方向居中显示 -->
			font-size: 30px;    <!-- 字体大小 -->
			text-align: center;    <!-- 水平对齐方式 -->
			font-weight: bold;    <!-- 字体粗细 -->
			font-family: "楷体";    <!-- 字体类型 -->
		}		
	</style>
</head>
<body>
	<div>行高</div>
</body>
```

### 字体样式缩写

font:文字粗细 大小/行高 字体名称;
```html
<style type="text/css">
	div{
		font:bold 20px/200px '楷体'
	}		
</style>
```

### CSS中的文字阴影

text-shadow:x y r color
>x：表示阴影在水平方向的偏移量，水平向左为负值，水平向右为正值，单位为px
>y：表示阴影在垂直方向的偏移量，垂直向上为负值，垂直向下为正值，单位为px
>r：表示阴影的模糊程度，数值越大，阴影越模糊，单位为px
>color：表示阴影的颜色

C3允许一段文字有多层阴影，用逗号隔开

### 页面各个区块之间有空行

方法1：页面的区块分别用div包裹起来，各个div分别设置不同的class选择器的属性值
```html
<style type="text/css">
	.box1{
		margin-bottom:10px;    <!-- margin-bottom:该div元素与下一个元素之间有10px的距离 -->
	}
	.box2{
		margin-top:10px;    <!-- margin-top:该div元素与上一个元素之间有10px的距离 -->
	}
</style>
```

方法2：margin：第一个属性
```html
<style type="text/css">
	.box{
		margin:100px auto;    <!-- margin的第一个属性100px表示该div元素与上一个元素和下一个元素之间的距离为100px -->
				     <!-- margin的第二个属性auto表示该div元素与网页的左边和右边的距离为平均分配，即水平居中显示 -->
	}
</style>
```
