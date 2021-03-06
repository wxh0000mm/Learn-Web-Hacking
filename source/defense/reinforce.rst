加固检查
========================================

网络设备
----------------------------------------
- 及时检查系统版本号
- 敏感服务设置访问IP/MAC白名单
- 开启权限分级控制
- 关闭不必要的服务
- 打开操作日志
- 配置异常告警
- 关闭ICMP回应

操作系统
----------------------------------------

Linux
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 无用用户/用户组检查
- 敏感文件权限配置
    - /etc/passwd
    - /etc/shadow
    - ~/.ssh/
    - /var/log/messages
    - /var/log/secure
    - /var/log/maillog
    - /var/log/cron
    - /var/log/spooler
    - /var/log/boot.log
- 日志是否打开
- 及时安装补丁
- 开机自启
    - /etc/init.d
- 检查系统时钟

Windows
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 异常进程监控
- 异常启动项监控
- 异常服务监控
- 配置系统日志
- 用户账户
    - 设置口令有效期
    - 设置口令强度限制
    - 设置口令重试次数
- 安装EMET
- 启用PowerShell日志
- 限制以下敏感文件的下载和执行
    - ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, pif, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh, exe, pif
- 限制会调起wscript的后缀
    - bat, js, jse, vbe, vbs, wsf, wsh

应用
----------------------------------------

FTP
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 禁止匿名登录
- 修改Banner

SSH
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 是否禁用ROOT登录
- 是否禁用密码连接

MySQL
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 文件写权限设置
- 用户授权表管理
- 日志是否启用
- 版本是否最新

Web中间件
----------------------------------------

Apache
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 版本号隐藏
- 版本是否最新
- 禁用部分HTTP动词
- 关闭Trace
- 禁止 ``server-status``
- 上传文件大小限制
- 目录权限设置
- 是否允许路由重写
- 是否允许列目录
- 日志配置
- 配置超时时间防DoS

Nginx
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 禁用部分HTTP动词
- 禁用目录遍历
- 检查重定向配置
- 配置超时时间防DoS

IIS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 版本是否最新
- 日志配置
- 用户口令配置
- ASP.NET功能配置
- 配置超时时间防DoS

JBoss
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- jmx console配置
- web console配置

Tomcat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- 禁用部分HTTP动词
- 禁止列目录
- 禁止manager功能
- 用户密码配置
- 用户权限配置
- 配置超时时间防DoS

参考链接
----------------------------------------
- `awesome windows domain hardening <https://github.com/PaulSec/awesome-windows-domain-hardening>`_
