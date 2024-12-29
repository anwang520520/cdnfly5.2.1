CdnFly5.2.1主控+5.1.18节点安装教程
			
由于之前公开，导致大家滥用，甚至拿去卖，现在有偿授权，一个主控10元。
           
本系统主控 IP 需要自助添加白名单：<a href="https://api.5205230.xyz" target="_blank">前往添加白名单。</a>
账号密码都要自己注册
有任何问题可以联系飞机：<a href="https://t.me/mikeuse" target="_blank">@mikeuse</a>
一、换源
bash <(curl -sSL https://gitee.com/SuperManito/LinuxMirrors/raw/main/ChangeMirrors.sh)
            <h2>二、添加虚拟内存</h2>
            yum -y install wget && wget -O set_swap.sh --no-check-certificate https://soft.mengclaw.com/Bash/set_swap.sh && bash set_swap.sh
            <h2>三、主控安装</h2>
 <p class="description">
              注意：cdnfly主控和被控节点暂时仅支持Centos-7和Ubuntu 16.04系统。
            </p>
<header>
 <p class="description">
              安装完管理账号：admin，密码：admin。测试账号：ceshi，密码：123456！
            </p>
</header>

            <pre><code id="code-6">curl -fsSL auth.5205230.xyz/cdnfly/master.sh -o master.sh && chmod +x master.sh && ./master.sh --es-dir /home/es</code><button class="copy-btn" data-target="code-6">复制</button></pre>
        </section>
        <section>
            <h2>四、节点安装</h2>
            <h3>节点安装命令</h3>
            <p>看后台--&gt;系统管理--&gt;系统升级相应的安装命令</p>
        </section>
        <footer>
            <p>由 <a href="https://t.me/mikeuse">@mikeuse</a> 提供 | 版权所有 &copy; 2024，本文件介绍内容只用于学习交流，若有侵权，请联系删除！</p>
        </footer>
    </article>

    <script>
        // 复制功能优化
        document.querySelectorAll('.copy-btn').forEach(button => {
            button.addEventListener('click', () => {
                const targetId = button.getAttribute('data-target');
                const codeBlock = document.getElementById(targetId);
                const textToCopy = codeBlock.textContent.trim();

                // 使用较老的 execCommand 方法确保兼容性
                const textarea = document.createElement('textarea');
                textarea.value = textToCopy;
                document.body.appendChild(textarea);
                textarea.select();
                try {
                    document.execCommand('copy');
                    button.textContent = '已复制';
                    setTimeout(() => button.textContent = '复制', 2000);
                } catch (err) {
                    console.error("复制失败: ", err);
                    alert('复制失败，请手动复制！');
                }
                document.body.removeChild(textarea);
            });
        });
    </script>
</body>
</html>
