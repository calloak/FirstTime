# 学习 Git、Maven、GitHub、Intellij IDEA
<a id="Top"></a>
##目录
* [Git 环境配置](#Git 环境配置)
* [Maven 环境配置](#Maven 环境配置)
* [Intellij IDEA 环境配置](#Intellij IDEA 环境配置)
* [Git 使用](#Git 使用)

##一、<a id="Git 环境配置">Git 环境配置</a>

###1.安装  

Windows 版的 Git： 

　msysgit，包含模拟环境和 Git，只需要下载一个单独的 exe 安装程序，其他什么也不用装。 

###2.配置 host  

　需要修改 C:\Windows\System32\drivers\etc\hosts文件，并添加 " 218.58.-.- gitlab.trs.com "。 

***疑问：*** *为什么要在 host 文件中添加" "中的内容？*  
```bash
公司搭建的 git 服务器，添加后可以用本机 git 访问该 IP 地址，进行项目的管理。  
```
###3.配置 git 账户信息  

　git config --global user.name " sunm--- "，" "内为 git 用户名。  
　git config --global user.email " ponderman---@gmail.com "，" "内为 email。

###4.检查信息 

　config --global -l，显示本机 git 的用户信息。  


##二、<a id="Maven 环境配置">Maven 环境配置</a>

###1.下载、安装  

###2.配置环境变量  

使用 DOS 在本地测试 Maven 是否配置：  

　命令：mvn -v   

###3.配置在 IDEA  

菜单流程：  

　Run/Edit Configurations/+/Mave  

***疑问：*** *为什么不使用 IDEA 自带的 Maven？*
```bash
配置一些 IDEA-Maven 没有的特殊的作用，即创建 Maven 的 clean-install 组合来编译代码。
```
***疑问：*** *clean 和 install 有什么用？*
```bash
clean：让 Maven 清理 target 目录，因为 Maven 默认项目的输出目录为 target。
install：执行 resource 任务，任务为在 Run->Edit Config 中配置的项目路径资源- Working Directory。
```
　***－疑问：*** *为什么清理 target 目录？ target 目录有什么用？*
```bash  
　------------
```
　***－疑问：*** *为什么执行 install？*
```bash
　-----------
```
　－clean-install 流程是：  
　　首先执行 clean，然后 install，最后编译项目。  
  
***疑问：*** *为什么 IDEA-Maven 的 Maven 命令组合不好？*
```bash
--------
```

***注意：*** *每个项目都默认使用 IDEA 自带 Maven，每个都需要手动设置 Maven。*    


##三、<a id="Intellij IDEA 环境配置">Intellij IDEA 环境配置</a>

###1.Git 配置  

菜单路径：  

　settings/version control/git，配置 git.exe 路径。  
 
###2.GitHub 配置  

菜单路径：

　settings/version control/git hub，配置 GitHub 账户信息。  
 
##四、<a id="Git 使用">Git 使用</a> 

###1.客户端  

###2.命令行  

###3.Intellij IDEA  

**检出项目菜单路径：**  

　VCS/Check Out/GitHub  

**提交项目菜单路径：**  

　VCS/Import Into/Share Porject  

**文件颜色：**  

　红色：新建文件，未 add，commit，未 push 服务器。  
　绿色：首次 add 到暂存区，但未 commit 到本地分支，未 push 服务器。  
　蓝色：有过 commit，或者已经 commit+push 服务器，并且本地文件做了修改。  
　白色：有过 commit，或者已经 commit+push 服务器，并且本地文件和本地分支，或服务器一致。

**Push：**  

　流程：首先，必须 add 到暂存区；然后，commit 到本地分支，填写 Git 账号和提交信息；最后，如果本地文件做了修改，首先需要 commit 到本地分支，然后 push 到服务器 。  

　冲突：-----  

**Pull：**  

　流程：项目菜单 VCS/Git/Pull。  

　冲突：-----  
　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　[返回顶部](#Top)
