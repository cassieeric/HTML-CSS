# 一篇文章教会你使用html+css3制作炫酷效果

## 一、前言

在浏览一些网站的时候，经常会看到很多的炫酷的效果去装饰页面，使它看起来更高端大气一些。比如，艺龙就采用了图片上加载文字，点击图片使把对应的图片放大，使用户清晰，直观的看到内容。这种效果该怎么做呢？

今天教大家用简单的html+css3结合制作艺龙的页面效果。![](html+css3结合制作炫酷效果.assets/1.png)

## 二、项目准备

1.图片：新建img文件，准备自己喜欢的五张图，保存在文件夹。

2.软件：Dreamweaver

## 三、实现的目标

运行时：图片显示缩略图。文字显示在上面。

点击时：把对应的图片显示并放大，点击文字有详细的介绍。

## 四、项目实现

#### 1. 创建div 存放图片和文件，添加class属性。

```HTML
<body>
<div  class="show">
<div class="wap">
	<div class="box" >
		<img src="images/img1.jpg">
		<span class='ba'>
	</div>
	<div class="box">
		<img src="images/img2.jpg">
		<span class='ba'></span>
		
	</div>
	<div class="box">
		<img src="images/img3.jpg">
		<span class='ba'></span>
	</div>
	<div class="box">
		<img src="images/img4.jpg">
		<span class='ba'></span>
	</div>
	<div class="box">
		<img src="images/img5.jpg">
		<span class='ba'></span>
	</div>
	</div>
</div>
</body>
```

#### 2. 添加文字。

```HTML
<span class='ba'>功夫熊猫</span>
<span class='ba'>飞屋环游记</span>
<span class='ba'>汽车总动员</span>
<span class='ba'>玩具总动员</span>
<span class='ba'>机器人</span>
```

### 添加css样式。

#### 1. 设置body的背景颜色为灰色。

```css
body
	{
		background: #ccc;
	}
```

#### 2. 设置box的宽，边框，边框阴影，加载动画过渡效果。

```css
.box{
		float: left;
		width: 160px;
		transition: all 0.5s;
		border: 1px solid #fff; #边框
		box-shadow: -5px 0px 10px 0px #000; #阴影
		position: relative;
	}
```

#### 3. 添加外层div 样式。

添加overflow属性，防止内容溢出。

```css
.wap{
		width: 999999999px;
		overflow: hidden;
	}
	.show{
		width: 800px;
		height: 320px;
		overflow: hidden;
		margin: 200px auto;
		box-shadow: 5px 5px 10px 4px #000;
	}
```

#### 4. 文字样式。 

设置高，宽，行高设置跟高一样， 文字才能居中显示。设置文字背景颜色，大小。

```css
.ba{
       width: 640px;
       height: 50px;
       line-height: 50px;
		color: #fff;
		background: rgba(0,0,0,0.5);
        bottom: 0;
        left: 0;
		position: absolute;
		text-indent: 2em;		
	}
```

#### 5. 添加鼠标移上去的效果样式。

```css

    .ba:hover{	  
       height: 320px;
       transition: all 0.5s;
	}
	.show:hover .box{
		width: 40px;

	}
		
	.show .box:hover{
		width: 640px;

	}
```

#### 6. 添加详细介绍文字。（text文件自取）。

## 五、效果展示。

1点击f12运行到浏览器![image-20200503131837268](html+css3结合制作炫酷效果.assets/2.png)

2.点击图片放大。![image-20200503131910340](html+css3结合制作炫酷效果.assets/3.png)

3.点击文字，详细介绍。![image-20200503131949587](html+css3结合制作炫酷效果.assets/4.png)

## 六、总结

1. 本项目，就鼠标点击事件遇到的一些难点进行了分析及提供解决方案。

2. 欢迎大家积极尝试，有时候看到别人实现起来很简单，但是到自己动手实现的时候，总会有各种各样的问题，切勿眼高手低，勤动手，才可以理解的更加深刻。

3. html+css也可以做出网站页面的效果，在上面显示图片标题的地方不能用绝对定位，于是用的relative定位，这个地方是布局的核心部分，否则无法将文字放在图片之上。
4. 代码很简单，希望对你有所启发。