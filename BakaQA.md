# 关于ResukiSU改名为BakaSU的常见问题说明

## 为什么要换掉ResukiSU这个名字
与sukisu切割。 

开发者原话：  I've received a lot of personal attacks because of this name.

## 为什么要改成BakaSU
新名称采用投票形式由用户选出，BakaSU由用户提出，并在两轮投票中保持最高票数。

## 变与不变
管理器、群组、官网等使用的ResukiSU的名称和图标将被全部更换。下游内核构建仓库也将逐步同步更改。 \
访问原ResukiSU安装脚本或github仓库将自动重定向到BakaSU，新官网域名为 https://bakasu.org/

管理器软件包名和签名保持不变，避免给终端用户带来更高的迁移成本。 \
管理器的KernelSU备选图标保留

## 作为终端用户如何迁移
取决于你当前的root方式，基本与常规uapi版本更新没有区别。
### 1.LKM模式
下载最新BakaSU管理器，打开后会提示需要更新内核，点击安装，LKM直接安装后重启即可
### 2.Built-in模式
下载最新BakaSU管理器，打开后会提示需要更新内核，点击安装，刷入更名后源码编译的Anykernel3并重启即可 \
如果刷入新编译的AK3还是提示需要更新内核，检查工作流是否固定了ResukiSU版本而不是使用文档建议的安装脚本 \
对于自行构建内核的用户，可以保持原ResukiSU的安装脚本地址不变，运行时将自动重定向至最新BakaSU
### 3.越狱模式
Ghostlock方式：下载安装最新BakaSU管理器，重启，使用Ghostlock越狱

关SELinux越狱：下载安装最新BakaSU管理器，重启（fastboot关闭SELinux），打开管理器点击越狱
