### 安装vsftpd
```
sudo apt install vsftpd
```

### 为FTP创建用户
- 创建用户
```
sudo useradd ftp_user
```
- 设置用户密码
```
sudo passwd ftp_user
```

### 创建FTP文件夹
- 创建FTP文件夹
```
mkdir <FTP_DIR路径>
```
- 修改FTP文件夹用户
```
sudo chown -R ftp_user.ftp_user <FTP_DIR路径>
```

### 修改配置文件
```
sudo vim /etc/vsftpd.conf
```
- 确保`local_enable=YES`、`write_enable=YES`，其他保持默认
- `chroot_local_user=YES`、`chroot_list_enable=YES`、`chroot_list_file=/etc/vsftpd.chroot_list`取消注释

    其中`/etc/vsftpd.chroot_list`文件指定了可以访问的用户，需要手动创建和修改，但是只有FTP文件夹的拥有者有写的权力
- 在最后一行指定FTP文件夹的路径：`local_root=/home/FTP_DIR`


### 重启ftp服务
`sudo /etc/init.d/vsftpd restart`或者`sudo service vsftpd restart`



