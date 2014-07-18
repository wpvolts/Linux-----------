Linux  解压缩&安装问题
================

解压缩
------

    unzip adt-bundle-l.zip -d /home/administrator/work/adt2/
    //这是zip的
    sudo tar -xzvf '/下载/jdk-7u40.tar.gz' -C /home/hadoop/software/java/ 
    //tar.gz

安装问题
------

    出现：
    E: 无法打开锁文件 /var/lib/dpkg/lock - open (13 Permission denied)
    E: Unable to lock the administration directory (/var/lib/dpkg/)

    
    解决方案：
    sudo rm -rf /var/lib/dpkg/lock
    
    sudo rm -rf /var/cache/apt/archives/lock
    
    sudo apt-get update 
    
    最后运行：sudo dpkg --configure -a  重新配置（系统会提醒）
    
    ps：参见[http://blog.csdn.net/feng2375/article/details/7929480](http://blog.csdn.net/feng2375/article/details/7929480)
