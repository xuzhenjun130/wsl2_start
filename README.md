# wsl2_start
wsl2 开机启动docker，设置ip



> 放弃`docker-desktop-windows` ,wsl2 中手动安装docker，wsl 每次启动ip都是变动的，没有 `docker-desktop-windows` 帮自动做端口映射
>
> 因此要写这个程序，启动docker，顺便获取wsl中的ip,配一下windows 下的hosts 文件



- `/home/sherman/wsl_ip.sh`  

  ```shell
  rs=$(sudo service docker start)
  ip addr show eth0 | grep 'inet ' | cut -f 6 -d ' ' | cut -f 1 -d '/'
  ```



