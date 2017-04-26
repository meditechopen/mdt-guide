# Hướng dẫn khai báo repo trên clients để sử dụng apt-cacher-ng

- Đối với những máy sử dụng hệ điều hành Ubuntu, tiến hành chạy dòng lệnh sau để khai báo repos:

`echo 'Acquire::http { Proxy "http://x.x.x.x:3142"; };' >  /etc/apt/apt.conf.d/01proxy`

Ví dụ:

`echo 'Acquire::http { Proxy "http://192.168.100.121:3142"; };' >  /etc/apt/apt.conf.d/01proxy`

- Đối với những máy sử dụng hệ điều hành CentOS: 

`echo "proxy=http://x.x.x.x:3142" >> /etc/yum.conf`

Ví dụ:

`echo "proxy=http://192.168.100.121:3142" >> /etc/yum.conf`

