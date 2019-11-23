# Docker
- Docker将应用程序与该程序的依赖,打包在一个image文件里面，属于linux一种容器的封装。image文件生成的容器实例，本身也是一个文件，成为容器文件。即一旦容器生成，会生成两个文件，image文件和容器文件。容器可以进行版本管理、复制、分享、修改，就像管理普通代码一样。

- Docker和虚拟机基本上都是用于解决环境配置的问题，相对于虚拟机，Docker有以下优点：
    1. Docker就是底层系统的一个进程，启动快(虚拟机需要启动操作系统）
    2. Docker只占用需要的资源，占用资源少(虚拟机需要独占一部分内存和空间）
    3. Docker只包含用到的组件即可，体积小(虚拟机是整个系统的打包）
## Docker常用命令：
- docker info/version: 验证Docker是否安装成功
- docker image ls: 列出本机所有image文件
- docker image rm [image]: 删除image文件    
- docker image pull [image]: 将image文件从远程抓取到本地
- docker container run (-it) [image] /bin/bash:
生成一个正在运行的容器实例，带参数(-it)，表示提供服务，不会自动终止。 
- docker container kill [containerID]:
对于不会自动终止的容器必须使用该命令手动终止
- docker container ls: 列出本机正在运行的容器
- docker container ls --all: 列出本机所用容器，包括终止运行的
- docker container rm [containerID]:
前面的kill命令虽然终止了运行的容器文件，却依然会占据硬盘空间，使用rm命令删除

