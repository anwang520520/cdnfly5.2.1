CdnFly5.2.1主控+5.1.18节点安装教程
			

<h2>一、换源</h2>

```
bash <(curl -sSL https://gitee.com/SuperManito/LinuxMirrors/raw/main/ChangeMirrors.sh)
```

<h2>二、添加虚拟内存</h2>

```
yum -y install wget && wget -O set_swap.sh --no-check-certificate https://soft.mengclaw.com/Bash/set_swap.sh && bash set_swap.sh
```

<h2>三、主控安装</h2>


注意：cdnfly主控和被控节点暂时仅支持Centos-7和Ubuntu 16.04系统。

安装完管理账号：admin，密码：admin。测试账号：ceshi，密码：123456！


https://raw.githubusercontent.com/anwang520520/cdnfly5.2.1/master/master.sh

```
curl -fsSL https://raw.githubusercontent.com/anwang520520/cdnfly5.2.1/master/master.sh -o master.sh && chmod +x master.sh && ./master.sh --es-dir /home/es
```

<h2>四、节点安装</h2>

看后台--&gt;系统管理--&gt;系统升级相应的安装命令

![节点安装教程](https://imgs.5205230.xyz/img/20241230120013881.png)

本文件介绍内容只用于学习交流，若有侵权，请联系删除！
