#shadowsocks+SwitchyOmega
## 1.安装shadowsocks(ss)
```
apt-get install python-pip & pip install shadowsocks
```
### a.命令行启动
```
sslocal -s 123.123.213.213 -p 6666 -b 127.0.0.1 -l 1080 -k 23333 -t 600 -m aes-256-cfb 
```
### b.脚本启动
配置文件ss.conf
```
{
//服务器ip
"server" : "123.123.213.213",
//服务器端口
"server_port" : 6666,
//本地浏览器监听端口
"local_port" : 1080,
//服务器密码
"password" : "23333",
//超时
"timeout" : 600,
//加密方式
"method" : "aes-256-cfb"
}
```
*启动命令
```
sslocal -c /filepath/to/ss.conf
```
*后台运行，输出存入sslocallog
```
nohup sslocal -c ss.conf > sslocallog &
```
查看后台任务
```
jobs
```
结束后台任务
```
fg %n
```
