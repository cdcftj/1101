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
