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
- docker container run: 生成一个正在运行的容器实例 
- docker container kill [containerID]:
对于不会自动终止的容器必须使用该命令手动终止
- docker container ls: 列出本机正在运行的容器
- docker container ls --all: 列出本机所用容器，包括终止运行的
- docker container rm [containerID]:
前面的kill命令虽然终止了运行的容器文件，却依然会占据硬盘空间，使用rm命令删除
- docker container start [containerID]: 重复使用容器
- docker container stop [containerID]:
终止容器运行，不同于kill命令直接发送SIGKILL，stop命令向主进程里发送SIGTERM，过一段时间再发送SIGKILL
- docker conatiner exec: 用于进入一个正在执行的容器
- docker container cp [containerID]:[PATH] .

## Dockerfile 文件
- .dockerignore   文件像github里的.gitignore一样用来忽略内容
- Dockerfile:
    - FROM image:tag    该文件继承自image的tag版本
    - COPY . /PATH
    将当前目录下的所有文件(除被.dockerignore忽略的）都拷贝到image 的/PATH路径下 
    - WORKDIR /PATH     指定接下来的工作路径为/PATH
    - RUN apt install   再/PATH目录下，运行apt
    install命令安装依赖，都将打包进image文件，该命令在image文件构建阶段执行
    - EXPOSE 3000   将容器3000端口暴露出来，允许外部链接
    - CMD   容器启动后自动自行的命令，该命令在容器启动后执行
有了Dockerfile文件以后，使用一下命令创建文件
- docker image build -t filename:tag . -t 参数用来指定image文件的名字
- docker container run  -p 8000:3000 -it image:tag /bin/bash    
   - -p 8000:3000 容器的3000端口映射到本机的8000端口
   - -it 容器的shell映射到本机的shell
   - /bin/bash　容器启动后内部执行的第一个命令


