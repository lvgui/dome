# dome
dom编程艺术
首先这个例子基本算是仿照《JavaScript DOM编程艺术》Jeremy Keith 上的图片库做的例子，我个人感觉这本书是神书，本书通过简单的几个例子为我们阐述了JavaScript如何编程的，
本例子以图片这个例子致敬这本神书。
这个书神奇的为我阐述了很多小例子
<h1>Snapshots</h1>
<ul id="imagegallery">
	<li>
		<a href="images/1.jpg" title="金克斯">金克斯</a>
	</li>
	<li>
		<a href="images/2.jpg" title="大熊">大熊</a>
	</li>
	<li>
		<a href="images/3.jpg" title="瑞文">瑞文</a>
	</li>
	<li>
		<a href="images/4.jpg" title="omg">omg</a>
	</li>			
</ul>
以前让我实现的我估计用一些蹩脚的也可以实现这个效果，效果看起来是一样的，但差的不是一星半点啊
这个例子让我懂得编程是一门艺术性质的语言，编程即是一门艺术，和书法、绘画一样也是一门艺术。
function addLoadEvent(func) {
	var oldonload = window.onload;
	if (typeof window.onload != 'function'){
		window.onload = func;
	}else{
		window.onload = function () {
			oldonload();
			func();
		}
	}
}
这个是一般都不会想象的设置，window.onload 这个函数说起来我也知道，一个页面只能有一个window.onload这个函数，我大约会在页面加载这个函数，但是后边的人在家js用window.onload这个函数会没有效果或者网页的动画没了，就是这些简单的函数才构建了艺术的灵魂。致敬这些伟大的艺术家。
接下来一个insertAfter即将这个艺术推向了高潮，“技术活，当赏！”短小就构建了一个神奇的功能，10行左右代码。噫吁戏，危乎高哉！
function insertAfter(newElement,targetElement) {
	var parent = targetElement.parentNode;
	if (parent.lastChlid == targetElement) {
		parent.appendChild(newElement);
	}else{
		parent.insertBefore(newElement,targetElement.nextSibling);
	}

}
接下来三个主函数写的非常严谨，考虑的非常严谨，争取做到读者能实现所有的功能，兼容各种主流浏览器，艺术也是严谨的。
一些的小的细节也把握的非常到位，这可谓是无愧这个书名--DOM编程艺术。
整个项目全用JavaScript原生去实现的，在这个各种编程武器层出不穷的情况下，不要迷失，简单的武器我们将至用到如火纯青的地步。
