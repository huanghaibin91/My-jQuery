# My-jQuery
jQuery笔记

----------

- $只是”jQuery”的别名，它是jQuery的选择器

- onload()和document.ready()的区别有以下两点：

	- 我们可以在页面中使用多个document.ready()，但只能使用一次onload()
	
	- document.ready()函数在页面DOM元素加载完以后就会被调用，而onload()函数则要在所有的关联资源（包括图像、音频）加载完毕后才会调用
	
## 选择器 ##
	
- jQuery中`:fisrt`、`:first-child`和方法`first()`的区别：`$(ul li:first)`选中的是第一个ul元素的第一个li子元素，然后添加样式，不论这个元素在本页面有多少个，它只找第一个而`$(ul li:first-child)`选择的是所有ul下面的第一个子元素是li的元素，有两个ul父元素，ul_1,ul_2他们都拥有各自的子元素li。最后是`first()`它和`:first` 类似，`$(ul li).first()`获取的第一个ul元素的第一个li子元素，不管有多少个本元素

- `prev + next`选择器next的查找范围必须是与"prev元素"相邻的下一个元素，并且必须是"prev元素"的同辈元素。`prev ~ siblings`选择器siblings的查找范围必须是"prev元素"之后的元素，并且是同辈元素(即与"prev元素"有同一个的父元素)

- $.fn是指jquery的命名空间，加上fn上的方法及属性，会对jquery实例每一个有效。如扩展`$.fn.abc()`那么你可以这样子：`$("#div").abc()`;通常使用`extend`方法扩展.`$.fx`是指jquery的特效。如果使用显示、滑动、淡入淡出、动画等。`$.fx.off`可以关闭动画，其实是直接显示结果