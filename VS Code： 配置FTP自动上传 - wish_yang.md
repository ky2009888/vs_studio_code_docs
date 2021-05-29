一：安装扩展 sftp 。

二：重启vs code软件。

三：快捷键Ctrl+shift+p，输入sftp:config回车进入配置文件。此时会在当前目录下生成一个 .sftp.json文件。

![](https://img2020.cnblogs.com/blog/2033033/202008/2033033-20200803105312929-1162495932.png)

四：修改json文件的配置：

![复制代码](https://common.cnblogs.com/images/copycode.gif)

{ "name": "centos7",//设置名字 "host": "192.168.244.111",//服务器IP "protocol": "sftp",//ftp模式还是sftp模式 "port": 22,//ftp:21 sftp:22 "username": "root", //ftp用户名 "password": "123456", //ftp密码 "passive": false, "interactiveAuth": true, "remotePath": "/root/ftp",//服务器目录 "ignore": \[ "\*\*/.vscode/\*\*", "\*\*/.git/\*\*", "\*\*/.DS\_Store" \],//忽略文件 "uploadOnSave": true, "syncMode": "update", "watcher": { "files": "glob", "autoUpload": true, "autoDelete": true }
}

![复制代码](https://common.cnblogs.com/images/copycode.gif)

五：可以点击左侧红框看到上传的文件。

![](https://img2020.cnblogs.com/blog/2033033/202008/2033033-20200803105659917-1369503246.png)