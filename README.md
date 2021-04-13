# install
```
yum update -y
yum install epel-release -y
yum update -y
yum groupinstall development tools -y
yum install net-tools vim lrzsz httpd-tools screen wget -y 
yum install -y ncurses-libs zlib-devel mysql-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel libcurl-devel libffi-devel
yum install gcc gettext autoconf libtool automake make pcre-devel asciidoc xmlto c-ares-devel libev-devel libsodium-devel mbedtls-devel -y

wget https://www.python.org/ftp/python/3.9.2/Python-3.9.2.tar.xz
xz -d Python-3.9.2.tar.xz
tar xfv Python-3.9.2.tar
cd Python-3.9.2 && ./configure --prefix=/root/bin/python392 
make && make install
rm -rf Python-3.9.2 Python-3.9.2.tar
/root/bin/python392/bin/python3 -m venv /root/bin/env392


yum install https://download.postgresql.org/pub/repos/yum/reporpms/EL-7-x86_64/pgdg-redhat-repo-latest.noarch.rpm -y 
yum install postgresql12 postgresql12-server -y 
/usr/pgsql-12/bin/postgresql-12-setup initdb
systemctl start postgresql-12
systemctl enable postgresql-12

```

```
cd /var/lib/pgsql/12/data/
ALTER USER postgres WITH PASSWORD '1234';
CREATE USER dbuser WITH PASSWORD '*****';
CREATE database accelerator owner = "youth" template = "template0" encoding = 'UTF8' lc_collate =
'zh_CN.utf8' lc_ctype = 'zh_CN.utf8' TABLESPACE = "pg_default"

```
