docker run -d -p 8180:8080 -p 50000:50000 -v /home/jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock jenkinsci/blueocean

1、mac使用netstat查看端口的使用情况：
a）如果需要查询inet，netstat -anvf inet
b）如果需要查询TCP， netstat -anvp tcp
c）如果需要查询UDP，netstat -anvp udp

2、Tomcat服务器设置用户名和密码：
https://blog.csdn.net/sinat_27933301/article/details/79764827

<role rolename="admin-gui"/>
<role rolename="manager-gui"/>
<user username="admin" password="admin" roles="admin-gui,manager-gui"/>


IntelliJ IDEA创建maven web项目（IDEA新手适用
https://blog.csdn.net/czc9309/article/details/80304074