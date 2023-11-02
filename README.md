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



    wget https://repo.mysql.com//mysql80-community-release-el7-1.noarch.rpm
    rpm -ivh mysql80-community-release-el7-1.noarch.rpm
    
    yum install httpd -y
    yum -y install mod_ssl
    yum install openssl-devel -y
    yum install mariadb-devel -y
    
    yum install epel-release -y
    yum install python-devel python3-devel -y    
    pip3 install uwsgi    
    yum install nginx -y
