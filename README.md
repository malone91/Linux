# Linux 平时用到的指令（敲的时候增加）

ifconfig 查询IP

getconf LONG_BIT 查询Linux系统位数

uptime 系统运行时间 和 平均负载

cd .. 进入上级目录

pwd 当前目录

date 系统当前时间

tar -zxvf xxx.tar.gz 解压tar.gz文件，-z：有gzip属性的，-x：解压，-v：显示所有过程，-f: 使用文件名字

mkdir xxx 生成xxx文件夹

whoami 显示当前Linux用户

crontab -l  查看Linux的定时任务列表,查看该用户下的crontab服务是否创建成功：

00 01 * * 6 /usr/local/jboss-4.0.5.GA/bin/shutdown.sh -S

01 01 * * 6 /usr/local/jboss-4.0.5.GA/bin/run.sh

分钟（0-59）
小时（0-28）
日期（1-31）
月份（1-12）
星期几（0-6，其中0代表星期日）
第六个字段是一个要在适当时间执行的字符串

crontab -r 表示删除用户的定时任务，当执行此命令后，所有用户下面的定时任务会被删除，执行crontab -l后会提示用户：“no crontab for admin”

crontab -e  编辑crontab服务文件，保存文件并并退出

ps -ax | grep cron

/sbin/service crond start
