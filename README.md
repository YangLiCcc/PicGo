# PicGo
用于PicGo图床

***

# &#x270D;PicGo ＋ GitHub 搭建个人图床工具

写在前面的话&#x1F440;

> 在搭建个人博客或是其他项目的过程中，发现如果项目中应用图片过多的话，仅仅使用本地图片的方法，占用空间实在是太大了。另一方面，使用网络上的图床工具在运维上多少也有些不便...而使用云服务器搭建图床工具，成本又些许高了。于是采用了GitHub＋PicGo的方式搭建图床工具，好处是其免费、背靠GitHub和微软 相对比较稳定、操作便捷 使用Git运维 ... 但缺陷就是其隐私性，你的图片别人可以访问。

# 搭建过程

## 1、 GitHub仓库设置

> 流程： 新建 public 仓库 → 创建 token → 复制 token 备用

### 1.1 新建仓库

点击GitHub主页左上角的 ` new ` 或者 右上角 <font color="red"> + </font> ` New repository ` 创建新仓库



填写仓库信息，这里需要注意的是，仓库必须得设置为<font color="red">Public</font>，因为后面通过客户端访问属于外部访问，因此无法访问<font color="red">Private</font>，这样的话图片上传会出错。



### 1.2 新建 token 并复制保存

此时仓库已经建立，点击右上角头像，然后进入设置；` Settings -> Developer settings -> Personal access tokens -> Generate new token `

也可以之间点击链接访问[创建token](https://github.com/settings/tokens)



然后复制生成的一串token字符，<font color="red">这个token只出现一次</font>，所以建议还是复制保存一下

## 2、PicGo 客户端配置

### 2.1 下载 & 安装

前往[PicGo官网](https://molunerfinn.com/PicGo/)下载并安装PicGo

PicGo是一个开源免费的图床上传工具，个人感觉还是比较轻便好用

安装过程就不多解释了 ... 

### 2.2 配置



* ` 设定仓库名 ` 即刚才新建的仓库名
* ` 设定分支名` 默认<font color="red">main</font>
* ` 设定Token` 即刚才复制的那一串token字符
* ` 指定存储路径` 选填，即指定在GitHub上的存储路径，我设置的是img/，这样上传的图片就都会存储到img文件夹下
* ` 设定自定义域名` 选填。由于国内访问GitHub比较慢，这里建议采用CDN加速的方法更改访问域名。我是用的是[jsDelivr]，有需的小伙伴可以访问官网文档或是直接改写 ` https://cdn.jsdelivr.net/gh/user/repo@version ` 使用。<font color="yellow">` user ` 改成你的GitHub用户名， ` repo@version ` 改成仓库名</font>

最后点击<font color="blue">确定</font>就可以了，也可以点击<font color="green">设为默认图床</font>将GitHub图床设为默认。

### 2.3 其他设置

如图，我个人比较建议打开的两项设置

* ` 上传前重命名 ` 可以在上传图片之前将你要上传的图片进行重命名的操作，只改变上传后在仓库的名称，不改变原文件名称；

* ` 上传后自动复制URL ` 对于写Markdown文档或是敲代码时直接引用上传后的图片比较友好

其他设置就按需自己配置咯&#x1F60F;
