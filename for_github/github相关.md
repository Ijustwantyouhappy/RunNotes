# 油猴脚本
1. GitHub 菜单汉化

# git clone太慢
用`hub.fastgit.org`替换掉`github.com`，例如：
- 原先链接：`https://github.com/PaddlePaddle/PaddleSeg.git`
- 加速链接：`https://hub.fastgit.org/PaddlePaddle/PaddleSeg.git`

# github加载缓慢
1. 查询相关网站的ip<br>
    在 https://www.ipaddress.com 上分别搜索：
    - github.global.ssl.fastly.net
    - github.com
2. 打开本地hosts文件
    - mac: `sudo vim /private/etc/hosts`
    - windows: `C:\Windows\System32\drivers\etc\hosts`
3. 在hosts文件中添加步骤1中查询到的ip，形如：
    ```
    140.82.114.4	github.com
    199.232.5.194	github.global.ssl.fastly.net
    ```
4. 刷新DNS缓存
    - mac: `dscacheutil -flushcache`
    - windows: `ipconfig /flushdns`
5. 检查效果<br>
    在命令行执行`ping github.com`，查看延迟和丢包率，可以看到有所好转。

# github网页图片加载不出来
查看加载不出来的图片的地址，搜索其二级域名对应的ip，将其添加到hosts文件中，和上述步骤类似。维基百科上图片无法加载也是一样的处理。
