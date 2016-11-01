2016-11-1
##day01

###推荐技术网站

>github.com
>
>stackoverflow.com

###shell

学完shell 可以说了解linux。

外壳：帮助操作电脑 的工具。

####1、bash

命令得是英文目录

命令格式[-options]  [参数]

如：mkdir blog
新建一个文件夹叫blog

>常用命令：

- pwd：查看当前目录
- cd：切换目录
	-  cd+..：为上级目录
	-  cd+盘符：切换盘符
- ls：查看当前目录下的内容
- mkdir(make directory)创建目录
- touch：创建文件
- cat：查看文件全部内容
- rm(remove)：删除文件
- rmdir(remove directory)：删除文件夹
- mv(move)：移动文件或重命名 mv 01.html ../b    mv 01.html 02.html
- cp(copy)：复制 cp 02.html ./01.html
- head：查看文件前几行 head -5 01.html
- tail：查看文件后几行 tail -5 01.html
- tab：自动补全，连按两次会将所有匹配内容显示出来
- history：查看操作历史
- curl：网络请求 curl http://www.baidu.com

####2、vi编辑器

vi 文件名 进入vi编辑模式
a/i进入编辑模式
esc推出编辑模式
shift+: wq保存退出

>常用命令：

- vi 文件路径
- w：底行模式保存 
- q：底行模式退出

>版本管理工具：

####3、git、svn

####git

- git init：仓库
  + git config user.name "username"
  + git config user.email "email"
  + git config --list
  + git config --global user.name username
  + git config --global user.email email


- 代码提交到仓库
  + git add 文件
  + git commit -m "注释"
  + git commit -a -m "注释"
  
- git status：查看存储状态

- 添加忽略文件
  + .gitignore后缀的文件 添加：/隐藏的文件名

- 比对文件差异
  + git diff
  + git diff --catched
  + git diff 版本号1 版本号2 文件路径
  + 
- 查看日志  
  + git log：更改的每一步版本号
  + git log --oneline：简洁形式
  

- 版本回退
 + git reset --hard Head~1
 + git reset --hard Head~2
 + git reset --hard Head~0
 + git reset --hard 版本号
 + git reflog

###day02

- git分支
	+ git branch 分支名：创建分支
	+ git checkout 分支名： 切换分支
	+ git merge 分支名：合并分支（返回到master主版本，合并）
	+ git branch -d 分支名：删除分支
- github和git管理
	+ 1、git push 远程服务器地址 分支
	+ 2、git remote add 变量名 远程服务器地址（给远程地址设个变量名）；git push 变量名 分支（在push时加上-u参数，就会默认建立本地当前分支与远程指定分支的关联,下一次push时就不需要输入分支名了）git push 变量名
	
###day03

####angular

- 指令
	+ ng- 开头的标签里面的属性的扩展形式称之为指令
	+ ng-app：告诉angular从这里开始管理了 
	+ ng-model：绑定input输入框的值
	+ ng-click：添加点击事件
	+ ng-init：初始化一个对象的值

- angular表达式
	+ 拼接字符串
	+ 数组
	+ 计算
	+ 不能是对象

>模块化

- 模块(module)
	+ angular.module('myApp',[])
	+ angular.module('myApp',[]).controller('demoController',function($scope){})
	 第一个参数，是控制器的名字，第二个参数，是一个回调函数，在回调函数里写我们想要的js代码。


>控制器(controller)

>双向数据绑定

- 数据模型的值发生改变，就会导致页面值的改变.
  页面值的改变，就会导致数据模型值的改变，这各种相互影响的关系就是双向数据绑定。
- ng-model

> 单向数据绑定

- 使用表达式显示数据模型的值。

>什么是 MVC 思想

- M:Model 模型  :数据存储，一些业务逻辑
- V:View  视图 ：就是用来展示数据
- C:Controller 控制器: 调度业务逻辑

>数据模型的调用

- 数据模型的建立

- $watch		
	+ $scope.$watch('数据模型名的字符串形式',function(变化后的值,变化前的值){}) 
	+ $scope.$watch里的回调函数会默认执行一次。
