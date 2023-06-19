# ubuntu安装配置内容

## 安装tar vim

```shell
sudo apt install tar
sudo apt install vim
sudo apt install git
git config --global user.name "ChenyuLy"
git config --global user.email "chenzeyuyuze@outlook.com"
ssh-keygen -t rsa -C "chenzeyuyuze@outlook.com" 
```

## Vmware tool

```shell
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install open-vm-tools-desktop -y
```

##  安装c++环境 

```shell
sudo apt update
sudo apt install build-essential gdb
gcc --version
g++ --version
gdb --version
sudo apt install cmake
cmake --version
```

## 安装vscode

```shell
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
code .

```

## 中文输入法

## mysql 

```shell
sudo aptitude search  mysql
sudo apt install  mysql-server
sudo mysql -u root -p
show databases;
use mysql;
show tables;
select host,user from user;
```

## 启用共享文件夹

```shell
sudo vmhgfs-fuse .host:/ /mnt/hgfs -o allow_other
```

## 配置coredump文件保存位置

```
ulimit -c  //检查coredump是否打开
ulimit -c unlimited

//修改/etc/sysctl.conf 文件尾行添加 core文件保存路径
kernel.core_pattern=/corefile/core_%e_%p_%t

sudo sysctl -p /etc/sysctl.conf


coredomp 调试网址 https://blog.csdn.net/qq_51604330/article/details/125753438
```

