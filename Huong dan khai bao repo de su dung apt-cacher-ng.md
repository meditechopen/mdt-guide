# Hướng dẫn khai báo repo trên clients để sử dụng apt-cacher-ng

- Apt-Cacher-NG là một caching proxy server, sau khi cài đặt, nó sẽ "cache" các gói đã download từ trên internet về và đặt tại server. Nhờ vậy, các máy khác lần sau sẽ không cần phải mất thời gian tải các packages này từ trên internet về nữa.
- Sau đây là hướng dẫn khai báo repo trên các máy client để sử dụng apt-cacher-ng:

## Ubuntu

- Tiến hành chạy dòng lệnh sau để khai báo repos:

`echo 'Acquire::http { Proxy "http://x.x.x.x:3142"; };' >  /etc/apt/apt.conf.d/01proxy`

Ví dụ:

`echo 'Acquire::http { Proxy "http://192.168.100.121:3142"; };' >  /etc/apt/apt.conf.d/01proxy`

- Tiến hành update trước khi cài đặt các packages bằng câu lệnh:

`apt-get update -y`

## CentOS

- Tiến hành khai báo repo bằng câu lệnh: 

`echo "proxy=http://x.x.x.x:3142" >> /etc/yum.conf`

Ví dụ:

`echo "proxy=http://192.168.100.121:3142" >> /etc/yum.conf`

- Update trước khi tiến hành tải các packages:

`yum update -y`