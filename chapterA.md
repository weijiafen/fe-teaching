<h1>GIT 操作</h1>
<p>GIT 是什么，Github是什么？自己百度吧。总之这就是一个存放代码的线上仓库。配置好之后拉取github上的代码是很简单的事情。主要是方便多人协同开发</p>
<p>安装git 并把线上仓库拉取到本地：</p>
<ol>
	<li>
		<p>安装msysgit,直接next</p>
		<blockquote>
			下载地址：https://git-for-windows.github.io/
		</blockquote>
	</li>
	<li>
		<p>注册并登陆github</p>
		<blockquote>
			https://github.com/
		</blockquote>
	</li>
	<li>
		<p>生成SSH</p>
		<ol>
			<li>在随意目录下新建一个文件夹gittest</li>
			<li>鼠标右键“Git bash”</li>
			<li>输入ssh-keygen -t rsa -C "xxxxxx@yy.com"  #建议填写自己真实有效的邮箱地址，一直回车</li>
			<li>测试ssh keys是否设置成功。<br/>
$ ssh -T git@github.com
输出：The authenticity of host 'github.com (192.30.252.129)' can't be established.
RSA key fingerprint is 16:27:xx:xx:xx:xx:xx:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)? 
<br/>yes #确认你是否继续联系，输入yes</li>
			
		</ol>
	</li>
	<li>
		<p>打开C/User/administrator/ssh中的id_rsa.pub文件，复制里面的内容</p>
	</li>
	<li>
				
		<p>登陆github，点击右上角头像setting。点击左边SSH and GPG keys,点击new ssh key，title任意填，把key复制进来，保存。</p>
	</li>
	<li>
		<p>
			在Git bash窗口输入
			<blockquote>git config --global user.name "your name"<br/>
			git config --global user.email "your email"  #配置你的姓名和邮箱 <br/></blockquote>
			以上就配置成功了。拉取github上的项目只需重复以下步骤
		</p>
	</li>
	<li>
		<p>在Git bash窗口输入
		<blockquote> git clone git@github.com:weijiafen/fe-teaching.git  </blockquote>
			<br/>
			github.com:weijiafen/fe-teaching.git 为你要拉的项目github地址
		</p>
	</li>
	<li>
		<p>查看gittest目录下多了fe-teaching文件夹，进入该文件夹，右键git bash（此时git bash的目录在这里），git pull命令为更新代码，提交的话可以右键git GUI,五个按钮从上往下按一遍就将代码提交到github上面了。更多分支合并等操作请自行学习吧哈哈。</p>
	</li>
</ol>
<a href="./README.md">返回目录</a>