# linux环境安装  

### 基础环境

M：安装完linux之后，需要做什么呢？

Z：能连接，并且带有JDK的环境

1. 首先看一下是否能ping通网络，查看本机ip

   ``192.168.175.134``  

2. yum安装 JDK  ``yum  install  java-1.8.0-openjdk   java-1.8.0-openjdk-devel``  

   配置jdk环境变量：``vi /etc/profile  ``

   添加以下内容，JAVA_HOME指向jdk位置，一般默认为/usr/lib/jvm/..

   ```properties
   #set java environment  
   JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk-1.8.0.181-3.b13.el6_10.i386
   PATH=$PATH:$JAVA_HOME/bin  
   CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar  
   export JAVA_HOME  CLASSPATH  PATH  
   ```

3. 关闭防火墙   

   ```properties
   关闭 /开启/重启防火墙
   service iptables stop 
   service iptables start 
   service iptables restart  
   永久关闭防火墙
   /sbin/service iptables stop
   chkconfig iptables off
   ```

4. 安装make  ``yum -y install gcc automake autoconf libtool make``     

5. 安装g++  ``yum install gcc gcc-c++``   


安装欠缺的命令





M：怎么查看jdk环境是否配置成功呢？

Z：用``java -version``能查看版本信息即可   











