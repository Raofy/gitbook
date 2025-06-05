# 1. Mac安装

## 1.1 环境要求
- Mac mini m4
- gvm（全称：go version manager）

## 1.2. go1.22环境安装

- 安装gvm工具

```shell
bash < <(curl -s https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
```

- 配置启用

```shell
source /Users/raofy/.gvm/scripts/gvm
```

- 环境生效

```shell
source ~/.zshrc
```

-  安装go1.22.12版本

```shell
# 查看远程可安装版本
gvm listall
# 安装go
gvm install go1.22.12 -B
```

- 设置默认的go版本

```shell
vim ~/.zshrc
```

**添加内容 ``go use go1.22.12 --default``**

```shell
source ~/.zshrc
```

- 验证是否安装成功

```shell
gvm list
```
# 2. gvm常用操作指令

# 3. 总结
本章主要记录了安装gvm和通过gvm安装go版本的相关操作。在Mac中可以通过Homebrew也可以更加快速的安装多个go版本，gvm和Homebrew都可以管理多个go版本，这里选用了gvm，使用gvm能够提供更加细粒化的管理，可以对于某个工程设置对应的版本。



