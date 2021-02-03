ssh-keygen ：[Location](~/.ssh/id_rsa)

manual [URL](https://wangdoc.com/ssh/key.html)

1. ssh-keygen -t ： 指定密钥加密的算法（dsa | rsa）
2. 注意修改权限，防止其他人读取：chmod 600 ~/.ssh/xxx
3. ssh-keygen -b ： 指定密钥的二进制[位数](数值越大，安全系数越高，但加密解密的开销越大。至少应为 1024，安全可设为 2048 或更高)
4. ssh-keygen -C ： 为密钥文件指定新的注释，[格式](username@host)
5. ssh-keygen -f ： 指定生成的私钥文件。

转发：

1. ssh -D ：动态转发
   1. 例：ssh -D local_port server_host -N
   2. 即：动态转发，不登陆远程 Shell，不执行命令
2. ssh -L ： 本地转发
3. ssh -R ： 远程转发