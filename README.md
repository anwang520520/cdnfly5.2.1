CdnFly5.2.1主控+5.1.18节点安装教程
			
由于之前公开，导致大家滥用，甚至拿去卖，现在有偿授权，一个主控10元。
           
本系统主控 IP 需要自助添加白名单：<a href="https://api.5205230.xyz" target="_blank">前往添加白名单。</a>
账号密码都要自己注册
有任何问题可以联系飞机：<a href="https://t.me/mikeuse" target="_blank">@mikeuse</a>

<h2>一、换源</h2>

bash <(curl -sSL https://gitee.com/SuperManito/LinuxMirrors/raw/main/ChangeMirrors.sh)
	
<h2>二、添加虚拟内存</h2>

yum -y install wget && wget -O set_swap.sh --no-check-certificate https://soft.mengclaw.com/Bash/set_swap.sh && bash set_swap.sh

<h2>三、主控安装</h2>


注意：cdnfly主控和被控节点暂时仅支持Centos-7和Ubuntu 16.04系统。

安装完管理账号：admin，密码：admin。测试账号：ceshi，密码：123456！

curl -fsSL auth.5205230.xyz/cdnfly/master.sh -o master.sh && chmod +x master.sh && ./master.sh --es-dir /home/es

<h2>四、节点安装</h2>

看后台--&gt;系统管理--&gt;系统升级相应的安装命令
