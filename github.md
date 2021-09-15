# github使用

## 创建文件

## 初始化仓库

`git init ` 进行仓库初始化，初始化以后会生成.git文件

<img src="C:\Users\要你管\AppData\Roaming\Typora\typora-user-images\image-20210915094635319.png" alt="image-20210915094635319" style="zoom: 67%;" />

## 一.git的基本操作

### 1. 添加文件

`git add <name>`可以把文件name添加到仓库中

`git add -A ` 是把所有新增，删除都添加到仓库中

### 2.修改文件并提交

1. 修改文件
2. `git add -A` 添加所有修改 或者可以 `git add <name>` 添加对name文件的修改
3. `git commit -m "描述"`添加对修改的描述
4. `git push` 提交代码到github远程仓库

### 3.从远程仓库获取代码

`git pull`

### 4.克隆仓库

1. 打开`github`的仓库网站，复制仓库网址

   ![image-20210915104549202](C:\Users\要你管\AppData\Roaming\Typora\typora-user-images\image-20210915104549202.png)

2. 进入想放仓库的目录，执行`git clone https://github.com/zhangmeih/learn.git`, 这里跟的参数是仓库的网址

3. <img src="C:\Users\要你管\AppData\Roaming\Typora\typora-user-images\image-20210915105338663.png" alt="image-20210915105338663" style="zoom: 67%;" />

   clone路径下出现了仓库的内容

### 5. ssh密钥生成

1. `输入ssh krygen`  然后一直回车，即可生成密钥

2. 密钥查看Windows密钥位置: `c:/用户/用户名/.ssh` ![image-20210915110319185](C:\Users\要你管\AppData\Roaming\Typora\typora-user-images\image-20210915110319185.png)

   .pub后缀是公钥，另一个是私钥

3. 打开`id_rsa.pub`，复制
4. 回到github -> 右上头像处 -> settings -> SSH and GPG keys -> new SSH key -> 把公钥粘贴过去

### 6.添加用户

在仓库中找到settings -> Manage access -> 要求用户(输入用户邮箱或者账号)

![image-20210915112339962](C:\Users\要你管\AppData\Roaming\Typora\typora-user-images\image-20210915112339962.png)

### http和ssh两种克隆方式的不同

从github上clone一个项目到本地的时候，有use HTTPS和use SSH两种方式，这两种主要是在push项目到github上时有所不同。完成一个push操作，需要对其内容进行安全管理，这里提供了ssh和https两种方式。而在clone项目到本地时，做出选择后，就已经决定了push的方式。

 ssh使用了RSA，即非对称加密的方式，存在一个公钥和私钥。可以生成一个本地的一组秘钥，然后将公钥复制到github的settings/profile下。

使用https方式，每次需要验证用户身份信息。