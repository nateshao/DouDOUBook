# Shell

## 脚本加密

最近有个需求，就是需要实现脚本的安全性，防止脚本被篡改或者一些数据泄露。那么最终怎么去实现这个需求呢，最终的实现效果需要**令脚本不可读但是可执行**。

### 加密方法介绍

经过一番搜索，Shell脚本加密常用的三种方法，gzexe，shc，upx。

#### 第一种，gzexe

特点是不用安装，加解密及其简单，命令简单粗暴

````shell
# 首先创建一个脚本，执行脚本需要赋可执行权
$ echo "echo test" > l.sh
# 加密
$ gzexe l.sh
# 解密
$ gzexe -d l.sh
````