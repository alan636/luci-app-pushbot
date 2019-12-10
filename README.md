# 说明
- 用于 OpenWRT/LEDE 路由器上进行 Server酱 微信推送的插件
- 基于 serverchan 提供的接口发送信息，Server酱说明：http://sc.ftqq.com/1.version
- 已经自带 luci
- 脚本基于斐讯 k3 制作，不同系统不同设备，请自行修改部分代码

#### 主要功能
- 路由 ip 变动推送
- 设备别名
- 设备上下线推送
- CPU 负载、温度监视
- 定时推送设备运行状态
- MAC 白名单、黑名单、仅检测某接口设备
- 免打扰时间

#### 已知BUG

- 多拨环境下无法获取 wan ip，详情查看https://github.com/tty228/luci-app-serverchan/issues/8
- 设备温度文件基于斐讯K3，其他设备如遇到设备温度无法正常读取，请自行修改
“cut -c1-2 /sys/class/thermal/thermal_zone0/temp” @KFERMercer 
- 潘多拉等系统，请将脚本开头sh改成bash
- 昨天反复测试了一下，因权限问题不能启动的bug已经不存在了，但无法启动的 bug 依然存在（目前已知我电脑上的 Ubuntu 中保存代码会导致无法启动，原因可能是换行符等符号不一致，shell 的语法有点令人蛋疼）
- 使用 `sh -n /usr/bin/serverchan/serverchan` 命令检查代码会显示代码出错，简直智障，如果遇到请随便使用什么文本编辑工具重新复制保存
- 修改定时推送设置的时候不会即使生效，需要重新启动才会操作crontab

#### ps

- 新功能不考虑添加
- 好久没有折腾，飞机到期，编译环境不可用
- 沉迷怀旧服
- 别问了，再问就是我太懒
- 欢迎各种代码提交
- 提交bug时请带上日志跟设备
