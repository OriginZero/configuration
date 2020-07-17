# configuration 善用搜索
## Linux
### 换源
> Ubuntu
```sh
# 进入源所在目录
cd /etc/apt/
# 备份当前源
sudo cp sources.list sources.list.bak
# 编辑源
sudo vim sources.list
# 删除原有源，添加如下的源
#...对应版本
# 更新系统
sudo apt-get update && sudo apt-get upgrade
sudo apt update && sudo apt upgrade
  ```
+ Ubuntu18.04 源
  ```sh
    #中科大
    deb https://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
  ```
+ Ubuntu20.04 源
    ```sh
    # 清华源
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
    # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
    # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
    # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse
    # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse
    # 预发布软件源，不建议启用
    # deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
    # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse


    # 阿里源
    deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse


    # 中科大
    deb https://mirrors.ustc.edu.cn/ubuntu/ focal main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ focal-security main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-security main restricted universe multiverse
    deb https://mirrors.ustc.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
    deb-src https://mirrors.ustc.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse


    # 163网易
    deb http://mirrors.163.com/ubuntu/ focal main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ focal-security main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ focal-updates main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ focal-proposed main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ focal-backports main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ focal main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ focal-security main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ focal-updates main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ focal-proposed main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ focal-backports main restricted universe multiverse
    ```
+ Manjaro 换源
    ```sh
    # Manjaro比较容易一条命令
    sudo pacman-mirrors -i -c China -m rank
    ```


## WSL

## Java配置

## Web配置
### Linux快速安装Node.js (LTS v12.x)
```sh
# Using Ubuntu
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs

# Using Debian, as root
curl -sL https://deb.nodesource.com/setup_lts.x | bash -
apt-get install -y nodejs
```
[Github项目地址(包含其他版本)](https://github.com/nodesource/distributions)
### NPM换源
```sh
# 更换为淘宝源
npm config set registry https://registry.npm.taobao.org
# 查看是否生效
npm config list
```

## Git配置
### 初次运行
```sh
# 配置用户名
git config --global user.name "OriginZero"
# 配置邮箱
git config --global user.email "example@outlook.com"
```

### 配置SSH
#### 为本机生成密钥SSH
```sh
ssh-keygen -t rsa -C "example@outlook.com"
```
得到`id_rsa`和`id_rsa.pub`两个文件，在工作目录下的`.ssh`中。
+ Windows 目录
    ```
    C:\Users\username\.shh\
    ```
+ Linux 目录
    ```
    ~/.ssh/
    ```
#### 将密钥内容复制到添加至Github || Gitlab
> 将.ssh/id_rsa.pub 内容复制到github或者gitlab中

一般在 `头像 > settings > ssh keys` 下

### [Git常见操作](https://juejin.im/post/5d5d61e96fb9a06ace5254bd#heading-26)
## 广告过滤规则
> 在浏览器拓展插件中添加
```sh
# 乘风广告规则
https://gitee.com/xinggsf/Adblock-Rule/raw/master/rule.txt
# 乘风视频广告过滤规则
https://gitee.com/xinggsf/Adblock-Rule/raw/master/mv.txt
```
