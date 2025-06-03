# Mac安装

## 环境要求
- Mac mini m4
- Homebrew
- Temurin JDK 17
- Temurin JDK 24

## JDK环境安装

- 查看对应版本号

```shell
brew search temurin
```

- 安装JDK17

```shell
brew install --cask temurin@17
```
**--cask​​: 指定安装的是一个 ​​Cask​​（macOS 应用包），而不是普通的软件包（Formula）**


- 安装JDK24

下面命令默认安装最新版本（截止目前最新为24）

```shell
brew install --cask temurin
```

- 查看所有安装后的版本

```shell
/usr/libexec/java_home -V
```

- 配置Java环境变量

编辑 ～/.zshrc文件

```shell
vim ~/.zshrc
```

追加下面的内容

```text
# 命名别名
alias java17='export JAVA_HOME=$(/usr/libexec/java_home -v 17); echo "Switched to JDK 17"'
alias java24='export JAVA_HOME=$(/usr/libexec/java_home -v 24); echo "Switched to JDK 24"'
# 默认使用JDK17
java17
export PATH=$JAVA_HOME/bin:$PATH
```

# 总结
至此，上面的我们完成对于Mac里的Java环境的搭建。除了上面的使用brew进行搭建JDK环境之外，还有其他方式搭建，例如jenv、sdkman等第三方工具，亦或者通过手动安装。我这里采用brew安装，是因为当前我不想安装太多的第三方工具，并且目前对于我来说，brew搭建已经能够满足我的开发需求，已经足够方便了。
