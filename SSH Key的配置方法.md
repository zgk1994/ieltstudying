### 一、设置git的user name和email

```
git config --global user.name "Luke.Deng"
git config --global user.email  "xiangshuo1992@gmail.com"
```

### 二、检查是否存在SSH Key

```
cd ~/.ssh
ls
或者
ll
//看是否存在 id_rsa 和 id_rsa.pub文件，如果存在，说明已经有SSH Key
```

### 三、如果没有SSH Key，则需要先生成一下

> 在2022年3月15日之后，github不再支持[SHA-1](https://so.csdn.net/so/search?q=SHA-1&spm=1001.2101.3001.7020)的加密方式了。将SHA-1的加密方式修改为`ECDSA`的方式.

```
ssh-keygen -t ecdsa -b 521 -C "your_email@example.com"
```

### 四、获取SSH Key

```
cat id_ecdsa.pub
```

