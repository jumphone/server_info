# server_info
server_info
    yum install httpd -y
    
    yum install epel-release -y
    yum install python-devel python3-devel -y    
    pip3 install uwsgi    
    yum install nginx -y

    yum install epel-release -y
    yum install gcc-gfortran -y
    yum group install "Development Tools" -y
    yum install readline-devel -y
    yum install xorg-x11-server-devel libX11-devel libXt-devel dbus-devel -y
    yum install bzip2-devel -y
    yum install xz-devel -y
    yum install pcre2-devel -y
    yum install java-devel -y
    
    
