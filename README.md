# goTest
go test code


├── api(项目对外提供和依赖的 API 文件。)

├── assets(项目中使用的其他资源（图像、logo 等）)

├── build(打包和持续集成所需的文件。)

│   ├── ci(存放持续集成的配置和脚本，如果持续集成平台(例如 Travis CI)对配置文件有路径要求，则可将其 link 到指定位置。)

│   └── package(存放 AMI、Docker、系统包（deb、rpm、pkg）的配置和脚本等。)

├── cmd(当前项目的可执行文件。保证 main 函数中的代码尽可能简单和少。只有一个可执行文件时去掉cmd，直接main.go)

│   └── _your_app_

├── configs(配置文件模板或默认配置。)

├── deployments(IaaS，PaaS，系统和容器编排部署配置和模板,如果是用 kubernetes 部署，建议改成 deploy)

├── docs(设计和用户文档)

├── examples(应用程序或公共库的示例程序)

├── githooks(Git 钩子)

├── init(系统初始化（systemd、upstart、sysv）和进程管理（runit、supervisord）配置。)

├── internal(私有的应用程序代码库。这些是不希望被其他人导入的代码。)

│   ├── app

│   │   └── _your_app_

│   └── pkg

│       └── _your_private_lib_

├── pkg(外部应用程序可以使用的库代码，微服务不使用)

│   └── _your_public_lib_

├── scripts(用于执行各种构建，安装，分析等操作的脚本。)

├── test(外部测试应用程序和测试数据。)

├── third_party(外部辅助工具，fork 的代码和其他第三方工具)

├── tools(此项目的支持工具。请注意，这些工具可以从 /pkg 和 /internal 目录导入代码。)

├── vendor（应用程序的依赖关系,如果 Go Module 满足需要，那么就不需要 vendor 目录。）

├── web(Web 应用程序特定的组件：静态 Web 资源，服务器端模板和单页应用)

│   ├── app

│   ├── static

│   └── template

├── website(项目的网站数据)

├── .gitignore

├── CONTRIBUTING.md(用来说明如何贡献代码，如何开源协同等)

├── LICENSE.md(常用的开源协议有：Apache 2.0、MIT、BSD、GPL、Mozilla、LGPL)

├── Makefile()在任何一个项目中都会存在一些需要运行的脚本，这些脚本文件应该被放到 /scripts 目录中并由 Makefile 触发。

├── README.md

└── go.mod(定义module path和依赖库的版本)

