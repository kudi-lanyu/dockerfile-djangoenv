当前目录Dockerfile 文件创建的 基础镜像包含: python3, django==1.10.5, uwsgi
    该镜像为 django + uwsgi 应用镜像


    vim, passwd
    iptables, netstat 安装在net-tools中



当前目录项目可以通过多种方式部署到docker容器中：
    1.本示例采用的是：
        将项目同步到服务器的一个固定目录中，然后通过文件挂载的方式挂载到docker容器中
        特别要注意，在容器中修改文件，要在服务器目录递归修改文件所有者，否则同步时会报权限问题。

该镜像没有配置python3 虚拟环境virtualenv virtualenvwrapper，是出于一个站点一个镜像的考虑。

基于此镜像，可以快速上手开发 python3 web应用。

考虑docker组件应用栈的实践， 本镜像相当于在 mysql等数据镜像基础上， 构建中间层，将要展示或者交互的信息呈现给实际使用者。

