# configuration

## Java配置


## Web配置
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
#### 将密钥内容添加至Github || Gitlab
> 将.ssh/id_rsa.pub 内容添加到github或者gitlab中

一般在 `头像 > settings > ssh keys` 下
## 广告过滤规则
> 浏览器拓展插件
```sh
# 乘风广告规则
https://gitee.com/xinggsf/Adblock-Rule/raw/master/rule.txt
# 乘风视频广告过滤规则
https://gitee.com/xinggsf/Adblock-Rule/raw/master/mv.txt
```
