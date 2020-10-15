https://blog.csdn.net/xuonline4196/article/details/88918355
(注意：jdk版本为1.8或者11)
1、卸载旧jenkins
  查询以前是否安装jenkins
     rpm -qa |grep jenkins
  卸载 jenkins
     rpm -e jenkins
  彻底删除jenkins残留文件
     find / -iname jenkins | xargs -n 1000 rm -rf

2、在jenkins配置文件中配置jdk路径
  vim /etc/init.d/jenkins
      candiadates="jdk路径"  修改jdk这条记录
3、配置Jenkins的端口：
  vim /etc/sysconfig/jenkins
    JENKINS_PORT="8088"

4、修改jenkins默认的操作用户
  vim /etc/sysconfig/jenkins
    JENKINS_USER="ROOT"

5、修改权限：
chown -R root /var/log/jenkins
chgrp -R root /var/log/jenkins
chown -R root /var/lib/jenkins
chgrp -R root /var/lib/jenkins
chown -R root /var/cache/jenkins
chgrp -R root /var/cache/jenkins

6、安装fontconfig
  yum install fontconfig

问题解决：
https://blog.csdn.net/qq_44959735/article/details/104363491

yum install fontconfig

