# demo
learning javaScript

<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title>选项卡</title>
		<style type="text/css">
			body,div,ul,li{margin: 0;padding: 0;}
			#Body{width: 800px;height: auto;overflow: hidden;border: 2px solid #CCCCCC;margin: auto;}
			#Body #Title{width: 100%;height: 42px;background: darkgoldenrod;}
			#Body #Title li{list-style: none;float: left;width: 160px;line-height: 40px;text-align: center;cursor: pointer;}
			#Body #Title .cur{background: #ccc; color: white;border-bottom: 2px solid black;}
			.container{width: auto;height: auto;overflow: hidden;}
			.container ul{display: none;padding-left: 30px;padding-top: 15px;padding-bottom: 40px;}
			.container .con_show{display: block;line-height: 30px;}
		</style>
	</head>
	<body>
		<div id="Body">
			<ul id="Title">
				<li class="cur">第一课</li>
				<li>第二课</li>
				<li>第三课</li>
			</ul>
			<div class="container">
				<ul class="con_show">
					<li>网页特效原理分析</li>
	                <li>响应用户操作</li>
	                <li>提示框效果</li>
	                <li>事件驱动</li>
	                <li>元素属性操作</li>
	                <li>动手编写第一个JS特效</li>
	                <li>引入函数</li>
	                <li>网页换肤效果</li>
	                <li>展开/收缩播放列表效果</li>
				</ul>
				<ul>
	                <li>改变网页背景颜色</li>
	                <li>函数传参</li>
	                <li>高重用性函数的编写</li>
	                <li>126邮箱全选效果</li>
	                <li>循环及遍历操作</li>
	                <li>调试器的简单使用</li>
	                <li>典型循环的构成</li>
	                <li>for循环配合if判断</li>
	                <li>className的使用</li>
	                <li>innerHTML的使用</li>
	                <li>戛纳印象效果</li>
	                <li>数组</li>
	                <li>字符串连接</li>
	            </ul>
				<ul>
	                <li>JavaScript组成：ECMAScript、DOM、BOM，JavaScript兼容性来源</li>
	                <li>JavaScript出现的位置、优缺点</li>
	                <li>变量、类型、typeof、数据类型转换、变量作用域</li>
	                <li>闭包：什么是闭包、简单应用、闭包缺点</li>
	                <li>运算符：算术、赋值、关系、逻辑、其他运算符</li>
	                <li>程序流程控制：判断、循环、跳出</li>
	                <li>命名规范：命名规范及必要性、匈牙利命名法</li>
	                <li>函数详解：函数构成、调用、事件、传参数、可变参、返回值</li>
	                <li>定时器的使用：setInterval、setTimeout</li>
	                <li>定时器应用：站长站导航效果</li>
	                <li>定时器应用：自动播放的选项卡</li>
	                <li>定时器应用：数码时钟</li>
	                <li>程序调试方法</li>
	            </ul>
			</div>
		</div>
	</body>
</html>
<script type="text/javascript">
	var oLi = document.getElementsByTagName("li");
	var oCon = document.getElementsByClassName("container")[0];
	var oUl = oCon.getElementsByTagName("ul");
	//1.for循环遍历获取到每一个元素
	for (var i = 0 ; i < oLi.length ; i++) {
		//2.创建一个伪元素记录
		oLi[i].index = i;
		oLi[i].onmousemove = function(){
			//3.循环遍历清除每一个Li标签的class
			for (var i = 0 ; i < oLi.length ; i++) {
				oLi[i].className = "";
			}
			//4.循环遍历清除每一个Ul的class
			for (var i = 0 ; i < oUl.length ; i++) {
				oUl[i].className = "";
			}
			this.className = "cur";
			oUl[this.index].className = "con_show";
		}
	}
</script>
