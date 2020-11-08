项目介绍

该项目使用Python提供的底层网络接口封装实现的一个应用程序, 使用Flask提供接口给前端使用

该项目可用于 机房管理, 集群管理, 分布式服务器管理等. 实现了: 性能/磁盘实时监控, 流量安全检查, 一对多同时控制, 文件分发.

博客/视频介绍/开发教程

哔哩哔哩 bilibili: 暂时没有上传视频个人空间: https://space.bilibili.com/274407612


使用的技术

前端: HTML5、CSS3、JavaScript、Echarts、SocketIO

后端: Python、Flask、底层网络接口 Socket, SocketIO

程序架构

我使用 Python 提供的底层网络接口实现了一个网络系统程序. Flask提供接口, 前端提供可视化web界面, 前端调用Flask接口, Flask调用网络系统程序

环境搭建

Python 3.8.2

附件中有 requirements.txt 里面有所用包, 双击运行安装所需环境.bat 建议使用管理员权限打开, 就一句话而已
```shell script
pip install --index-url https://pypi.douban.com/simple -r requirements.txt && pause
```
附件中还有 WinPcap_4_1_3.exe 也需要安装.

启动项目

使用Python执行manage.py即可
```shell script
python manage.py -[options]
```
服务端

服务端程序只有一个可选参数， port 端口, 
```python
opt, args = getopt.getopt(sys.argv[1:], 'p:')
```
开放的HOST为所有
```python
app.run(host="0.0.0.0", port=port)
```
客户端

客户端和服务端一样