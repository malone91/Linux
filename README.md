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

linux系统也有位数之分，所以在linux上安装一些软件，比如jdk之类的就需要注意下版本。

查看linux系统位数最简单的命令（这里以redhat为例，不同版本linux命令也许不同）


复制代码
命令1：getconf LONG_BIT
结果：64

命令2：uname -a
结果：Linux Test004MUJUP 2.6.32-431.23.3.el6.x86_64 #1 SMP Wed Jul 16 06:12:23 EDT 2014 x86_64 x86_64 x86_64 GNU/Linux

命令3：uname -r
结果：2.6.32-431.23.3.el6.x86_64

命令4：cat /proc/version
结果：Linux version 2.6.32-431.23.3.el6.x86_64 (mockbuild@x86-027.build.eng.bos.redhat.com) (gcc version 4.4.7 20120313 (Red Hat 4.4.7-4) (GCC) ) #1 SMP Wed Jul 16 06:12:23 EDT 2014
复制代码
x86_64则说明你是64位内核, 跑的是64位的系统.
i386, i686说明你是32位的内核, 跑的是32位的系统
