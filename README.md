## 通过SSH登录
1. 生成SSH Key
```
ssh-keygen -t rsa -b 4096 -C "你的邮箱"
vim ~/.ssh/id_rsa.pub
```

2. 复制所有内容，然后`:q`回车退出
3. 到GitHub右上角点Settings
4. 找到SSH and GPG keys
5. 把复制的内容粘贴到key部分，随便起一个名字，点`Add SSH Key`确认

## 使用清华大学镜像源

1. `vim /etc/apt/sources.list`
2. 按i键进入“插入”模式
3. 复制以下内容到文件中：
```
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

# 预发布软件源，不建议启用
# deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
```
4. 输入`:wq`保存并退出
