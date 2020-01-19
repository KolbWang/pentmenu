## 工具名称：pentmenu

## 工具作用：dos攻击

## 工具下载：https://github.com/kolbwang/pentmenu.git



## 环境需求：

> - bash
> - sudo
> - curl
> - netcat (必须支持'-k'选项)
> - hping3 (或 'nping' 可以用来代替洪水攻击)
> - openssl
> - stunnel
> - nmap
> - whois (不是必需的)
> - nslookup (或者 'host' 命令)
> - ike-scan

## 如何使用：

- 解压数据包

  ```
  root@kali:~#  unzip pentmenu-master
  ```

- 赋予执行权限并执行脚本

  ```
  root@kali:~#  cd pentmenu-master/
  root@kali:~/pentmenu-master#  chmod 755 pentmenu
  root@kali:~/pentmenu-master#  ./pentmenu
  ```

## 模块介绍：

> 1) ICMP Echo Flood  # 使用hping3启动针对目标的传统ICMP Echo洪水
>  2) ICMP Blacknurse  # 使用hping3对目标发动ICMP洪水
>  3) TCP SYN Flood      # 使用hping3发送大量TCP SYN数据包
>  4) TCP ACK Flood      # 提供与SYN flood相同的选项，但设置ACK（确认）TCP标志
>  5) TCP RST Flood      # 提供与SYN flood相同的选项，但设置RST（重置）TCP标志
>  6) TCP XMAS Flood  # 类似于3)和4)，但发送所有TCP标记的（CWR，ECN，URG，ACK，PSH，RST，SYN，FIN）
>  7) UDP Flood             # 非常类似于TCP SYN Flood，而是将UDP数据包发送到指定的 host : port
>  8) SSL DOS                # 使用OpenSSL尝试DOS目标 host : port
>  9) Slowloris               # 使用netcat将HTTP Headers慢慢发送到目标主机：port，目的是使资源匮乏
>  10) IPsec DOS           # 使用ike-scan尝试使用主模式和来自随机源IP的主动模式第1阶段数据包来泛洪指定的IP
>  11) Distraction Scan  # 这不是DOS攻击，只是使用hping3从您选择的欺骗IP启动多个TCP SYN扫描
>  12) DNS NXDOMAIN Flood  # 此攻击使用dig，通过向不存在的域发送大量DNS查询对您的DNS进行压力测试
>  13) Go back               # 返回上一级菜单



请不要发起一些恶意的行为:grinning:
本脚本仅供测试，研究，任何使用本贴内容进行操作产生的一切后果与责任与本人无关