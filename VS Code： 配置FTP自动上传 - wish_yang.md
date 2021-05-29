一：安装扩展 sftp 。

二：重启vs code软件。

三：快捷键Ctrl+shift+p，输入sftp:config回车进入配置文件。此时会在当前目录下生成一个 .sftp.json文件。

![](https://img2020.cnblogs.com/blog/2033033/202008/2033033-20200803105312929-1162495932.png)

四：修改json文件的配置：

```java
{
    "name": "centos7",
    "host": "192.168.64.ip",
    "protocol": "sftp",
    "port": 22,
    "username": "root",
    "password": "******", 
    "passive": false, 
    "interactiveAuth": true,
    "remotePath": "/flink1124",
    "ignore": [
        "**/.vscode/**",
        "**/.git/**",
        "**/.DS_Store"
    ],
    "uploadOnSave": true,
    "syncMode": "update",
    "watcher": {
        "files": "glob",
        "autoUpload": true,
        "autoDelete": true
    }
}

五：可以点击左侧红框看到上传的文件。

![](https://img2020.cnblogs.com/blog/2033033/202008/2033033-20200803105659917-1369503246.png)
