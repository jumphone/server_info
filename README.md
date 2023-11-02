# server_info
server_info

    

    yum install epel-release -y
    yum install gcc-gfortran -y
    yum group install "Development Tools" -y
    yum install readline-devel -y
    yum install xorg-x11-server-devel libX11-devel libXt-devel dbus-devel -y
    yum install bzip2-devel -y
    yum install xz-devel -y
    yum install pcre2-devel -y
    yum install java-devel -y



   
    yum install httpd -y
    yum -y install mod_ssl
    yum install openssl-devel -y
    yum install mariadb-devel -y
    
    yum install epel-release -y
    yum install python-devel python3-devel -y    
    pip3 install uwsgi    
    yum install nginx -y

    # https://blog.csdn.net/qq_56905650/article/details/131300819
    # CentOS安装配置MySQL
    
    wget https://repo.mysql.com//mysql80-community-release-el7-1.noarch.rpm
    rpm -ivh mysql80-community-release-el7-1.noarch.rpm
    
    yum -y install mysql mysql-server --nogpgcheck

    systemctl start mysqld
    grep 'temporary password' /var/log/mysqld.log
    mysql -uroot -p'pwd'

    # https://chrisshennan.com/blog/fixing-authentication-plugin-cachingsha2password-cannot-be-loaded-errors
    # Fixing "Authentication plugin 'caching_sha2_password' cannot be loaded" errors
    
    vi /etc/my.cnf
    default_authentication_plugin=mysql_native_password

    systemctl restart mysqld

    #https://stackoverflow.com/questions/49963383/authentication-plugin-caching-sha2-password
    ALTER USER root@'localhost'
    IDENTIFIED WITH mysql_native_password
    BY 'pw';

    systemctl stop httpd.service
    systemctl start nginx.service

    #djangoblog/settings.py
    USE_TZ = False
    
