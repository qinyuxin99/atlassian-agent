Atlassian Agent
Support (almost any version, include 8.0):
JIRA Software FAQ
JIRA Core
JIRA Service Desk
JIRA plugin: Capture
JIRA plugin: Training
JIRA plugin: Portfolio
Confluence Windows特别注意
Confluence plugin: Questions
Confluence plugin: Team Calendars
Bamboo FAQ
Bitbucket FAQ
FishEye FAQ
Crowd FAQ
Crucible FAQ
Third party plugins

使用说明
优势
支持Atlassian家几乎所有产品，同时支持插件（包括插件市场的第三方插件）。
支持DataCenter模式。
相比较于传统的crack来说可以很容易的升级你的服务，而不用重新再次破解。
提供基于java的命令行 keygen，更方便在终端环境使用。
开源项目，你知道破解时都做了什么。
直接下载
直接下载本项目release包。
自行编译
Clone本项目源码，pom.xml同级目录执行mvn package后即可进行编译。
使用target目录产出的atlassian-agent-jar-with-dependencies.jar，而非atlassian-agent.jar！
如果你不知道我在说什么，最好还是直接下载我编译好的包。
使用帮助
破解需要成套使用，不能只破解插件，要先使用atlassian-agent.jar破解服务。
如果你已经获得atlassian-agent.jar，可以试着执行java -jar atlassian-agent.jar看看输出的帮助。
这里的帮助以Atlassian家的Confluence服务为例。
配置Agent
将atlassian-agent.jar放在一个你不会随便删除的位置（你服务器上的所有Atlassian服务可共享同一个atlassian-agent.jar）。
设置环境变量JAVA_OPTS（这其实是Java的环境变量，用来指定其启动java程序时附带的参数），把-javaagent参数附带上。具体可以这么做：
你可以把：export JAVA_OPTS="-javaagent:/path/to/atlassian-agent.jar ${JAVA_OPTS}"这样的命令放到.bashrc或.bash_profile这样的文件内。
你可以把：export JAVA_OPTS="-javaagent:/path/to/atlassian-agent.jar ${JAVA_OPTS}"这样的命令放到服务安装所在bin目录下的setenv.sh或setenv.bat（供windows使用）中。
你还可以直接命令行执行：JAVA_OPTS="-javaagent:/path/to/atlassian-agent.jar" /path/to/start-confluence.sh来启动你的服务。
或者你所知的其他修改环境变量的方法，但如果你机器上有无关的服务，则不建议修改全局JAVA_OPTS环境变量。
总之你想办法把-javaagent参数附带到要启动的java进程上。
配置完成请重启你的Confluence服务。
如果你想验证是否配置成功，可以这么做：
执行类似命令：ps aux|grep java 找到对应的进程看看-javaagent参数是否正确附上。
在软件安装目录类似：/path/to/confluence/logs/catalina.outTomcat日志内应该能找到：========= agent working =========的输出字样。
使用KeyGen
你得确认已经配置好agent，参考上面说明。
当你试着执行java -jar /path/to/atlassian-agent.jar时应该可以看到输出的KeyGen参数帮助。
请仔细看看每个参数的作用，特别是-p参数的取值范围。-p参数内容最好用引号包住，否则可能影响参数解析。
第三方插件将其应用密钥/插件关键字作为-p参数。如：-p 'com.gliffy.integration.confluence'
在Atlassian服务安装时你应该能看到类似：AAAA-BBBB-CCCC-DDDD的server id，请留意。
提供了正确的参数运行KeyGen会在终端输出计算好的激活码。
将生成的激活码复制出来去激活你要使用的服务。
举个栗子：java -jar atlassian-agent.jar -p conf -m aaa@bbb.com -n my_name -o https://zhile.io -s ABCD-1234-EFGH-5678
申明
本项目只做个人学习研究之用，不得用于商业用途！
商业使用请向Atlassian购买正版，谢谢合作！
本项目使用GNU General Public License v3.0开源许可！
不允许说我代码写的糟糕，对我来说PHP才是世界上最好的语言（不服来辩）。
交流
给本项目发issue。
欢迎你来一起完善这个项目，请发PR。
你可以加入QQ群：30347511 和我实时交流。
访问网站：https://zhile.io 给我留言。
热心网友教程（感谢原作者，侵删！）
热心大佬的一键安装配置脚本
confluence 安装及破解
【黑科技】Atlassian产品线全破解
通过Docker安装JIRA和Confluence（破解版）
通过Docker安装JIRA和Confluence（破解版）


其他版本请前往以下Gitee网址进行下载：

https://gitee.com/pengzhile/atlassian-agent/releases


亲测，可破解jira8.13.7版本！！！！
