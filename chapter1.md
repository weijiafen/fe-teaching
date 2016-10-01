<h1>HTML篇(一)</h1>
<h2>先从新建一个html文件开始</h2>
<p>话不多说先上手
<ol>
	<li>在桌面右键新建一个记事本，命名为test.html。此处把.txt后缀名改成.html。有些电脑不显示文件后缀名，自行百度。</li>
	<li>创建之后对文件右键，打开方式->记事本。</li>
	<li>输入<br/>
<pre>
	&lt;html>
		&lt;head>&lt;/head>
		&lt;body>
			&lt;h1>hello world&lt;/h1>
			&lt;h2>hello world&lt;/h2>
			&lt;h3>hello world&lt;/h3>
			&lt;h4>hello world&lt;/h4>
			&lt;h5>hello world&lt;/h5>
			&lt;h6>hello world&lt;/h6>
		&lt;/body>
	&lt;/html>
</pre>
保存
	</li>
	<li>双击打开，或者直接拖动到浏览器打开</li>
</ol>
</p>
<p>到这里你发现了。浏览器里只出现了从大到小的6句hello world，那些尖括号里面的东西都不见了。这是因为浏览器能够解析html文件，将html标签解析成具备特定功能的命令<br/>
现在可以参照着概念啃了。
<ol>
	<li>HTML 指的是超文本标记语言 (Hyper Text Markup Language)</li>
	<li>HTML 不是一种编程语言，而是一种标记语言 (markup language)</li>
	<li>标记语言是一套标记标签 (markup tag)</li>
	<li>HTML 使用标记标签来描述网页</li>
</ol>
编程语言是像C语言那样，拥有变量，函数，运算等逻辑操作的语言。而标记语言没有什么逻辑性可言，处理好标签的嵌套关系，就能组织好一个网页的结构。所以上手等级一颗星都不到。
&lt;html>是根标签，包含住所有的子标签，head是头部标签，里面放网页的配置信息，内容不会出现在网页中。body是主体标签，里面放网页中的所有元素。上面只是个简单的例子，真正的网页标签的嵌套可以非常深。你可以随便打开一个网页，右键查看源代码。
</p>
<h2>接下来扫一下常用的标签</h2>
<p>所有标签可以扫一遍w3school：<code>http://www.w3school.com.cn/html/html_intro.asp</code></p>
<p>
	HTML标签分块元素和内联元素（内联元素其实还分替换内联元素和非替换内联元素）两种，最明显的特征就是块元素会自动换行，块元素后面的标签会自动换到下一行，而内联元素不换行，写在内联元素后面的标签紧跟在内联元素右边。其他的特征在CSS篇会更详细深入。至于哪些是块元素，哪些是内联元素，自己一个个试试就知道了。<br/>
	&lt;div>是一个容器，熟悉PS的童鞋可以联想一下图层。没有具体的特征，只是用来包裹住其他标签。<br/>
	&lt;p>是一个段落，用来包裹住一段文字。<br/>
	&lt;span>用来包裹文字，但不换行<br/>
	&lt;h1>到h6，用来包裹文字标题。字体从大到小。标题的作用是有利于<a href="http://baike.baidu.com/link?url=388NV_quGc__xJAU7uweiLGgF3vbq0aAEusTbKi2layF_GFI_1sgtQPH4Acqm6pqK_3G-3FyLXbCHXDVOtdIMa">SEO</a>，一个网页最好只有一个h1标题。<br/>
	&lt;br/>表示换行<br/>
	&lt;hr/>表示一条分割线<br/>
	好了，现在可以做一个小任务：创建一个html文件并随便嵌套以上的标签和文字吧,文本用中文试试？<br/>
	我想你应该不会蠢到写出&lt;p>&lt;span>&lt;/p>&lt;/span>这样的嵌套关系吧？很明显这是不正确的嵌套关系。双标签开始后必须结束最近的那个标签，单标签如&lt;br/>开始即是结束。<br/>
	如果你完成了上面的小任务一定遇到了一个问题，中文为什么是乱码的？解决方法是在head标签里面加上这么一句<br/>
	</p>
	<blockquote>
		&lt;meta charset='utf-8'/>
		或&lt;meta charset="gb2312" />
	</blockquote>
	<a href="http://baike.baidu.com/link?url=PfC1p4N4sU53AzpyOUwLCL75DPESVkd-Uemjc7CLL0FUje2eh05Wbjst7degZWXd3XR6Ad3vlW1rdFDDVP9xIDdZoOWKwLZDYVr76GzWYLU-QwSS0Muk1sEzcyKCk5m8">字符编码</a>是一个很又是另一个话题了，在这里你可以简单地记住这两个能够让网页的中文正确地显示，其中utf-8是用得比较多的。
	<p>
	接下来介绍的标签是列表和表格。列表有有序列表&lt;ol>和无序列表&lt;ul>两种，使用的方式如下：
	
	</p>
	<blockquote>
		&lt;ol>
			&lt;li>第一项&lt;li>
			&lt;li>第二项&lt;li>
			&lt;li>第三项&lt;li>
		&lt;ol>
		&lt;ul>
			&lt;li>第一项&lt;li>
			&lt;li>第二项&lt;li>
			&lt;li>第三项&lt;li>
		&lt;ul>
	</blockquote>
	<code>关于编辑器。对于初学者我始终坚持可以用记事本来编辑网页的，每一个字母都要手敲会让你记得更深一些。好用的编辑器固然让你写起来很快很爽，但是基本功还是要打，不要太依赖工具。等你记得牢大部分标签的时候，推荐用sublime text吧</code>

（待续。。。）
<a href="./README.md">返回目录</a>
<a href="./chapter2.md">下一章</a>