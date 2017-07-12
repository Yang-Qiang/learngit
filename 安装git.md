windows git 直接去官网就行，地址如下：
https://git-scm.com

Linux系统 git下载地址如下 https://www.kernel.org/pub/software/scm/git/ 。

若是条件允许，从源代码安装有很多好处，至少可以安装最新的版本。Git 的每个版本都在不断尝试改进用户体验，所以能通过源代码自己编译安装最新版本就再好不过了。有些 Linux 版本自带的安装包更新起来并不及时，所以除非你在用最新的 distro 或者 backports，那么从源代码安装其实该算是最佳选择。

Git 的工作需要调用 curl，zlib，openssl，expat，libiconv 等库的代码，所以需要先安装这些依赖工具。在有 yum 的系统上（比如 Fedora）或者有 apt-get 的系统上（比如 Debian 体系），可以用下面的命令安装：

$ yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel

$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev

然后编译并安装：

$ tar -zxf git-2.12.3.tar.gz
$ cd git-2.12.3
$ make prefix=/usr/local all
$ sudo make prefix=/usr/local install


如果要在 Linux 上安装预编译好的 Git 二进制安装包，可以直接用系统提供的包管理工具。在 Fedora 上用 yum 安装：

$ yum install git-core

在 Ubuntu 这类 Debian 体系的系统上，可以用 apt-get 安装：

$ apt-get install git
