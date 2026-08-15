# CommonTools 常用工具集合

个人开发与运维常用工具软件收集仓库，优先收录绿色免安装版本。

> 由于 GitHub 对单文件有 100MB 上限、对仓库总体积有限制，本仓库仅上传绿色免安装工具；系统镜像（ISO）与安装包（exe/msi/zip/rar）仅保留在本地，详细说明见文末「未上传内容」。

## 已上传的工具

| 工具 | 版本 | 说明 |
|------|------|------|
| [apache-tomcat-10.1.20](apache-tomcat-10.1.20/) | 10.1.20 | Java Web 应用服务器（免安装版） |
| [Bandizip](Bandizip/) | - | 压缩/解压软件（绿色便携版） |
| [Maven](Maven/) | 3.3.9 / 3.8.1 / 3.8.4 / 3.9.4 | Java 项目构建与依赖管理（含本地仓库 myrepo） |
| [nacos](nacos/nacos/) | 2.5.2 | 阿里微服务注册/配置中心（已解压目录，仅含配置与启动脚本） |
| [MQTT](MQTT/) | - | MQTT 协议学习笔记（`MQTT协议.txt`） |

## 仅本地保存（未上传）的工具

| 工具 | 说明 | 未上传原因 |
|------|------|-----------|
| CentOs | CentOS 7 / Ubuntu 20.04 系统镜像 | ISO 镜像 4GB+，超出 GitHub 限制 |
| Datagrip | 数据库管理 IDE（JetBrains） | 安装包 425MB |
| Everything | 本地文件极速搜索 | 安装包 |
| FastStone Capture | 截图/录屏工具 | 空目录 |
| FinahShell (FinalShell) | SSH/SFTP 终端工具 | 安装包 |
| HBuilder | 前端开发 IDE | 压缩包 205MB |
| MySql | MySQL 数据库 | 安装包 |
| node | Node.js 运行时 | 压缩包 |
| Notepad++ | 轻量级文本编辑器 | 安装包 |
| Postman | API 接口调试工具 | 安装包 |
| Redis-5.0.14 | 内存缓存数据库 | 压缩包 |
| SQLyog | MySQL 图形化管理工具 | 安装包 |
| Typora | Markdown 编辑器 | 安装包 |
| VMwareWorkstationPro17.6.4 | 虚拟机软件 | 安装包 405MB |
| VSCode | 代码编辑器 | 安装包 |
| Xshell70421 | SSH 远程连接终端 | 压缩包 |

## 使用说明

### Maven

- 目录内含 4 个版本：`apache-maven-3.3.9`、`apache-maven-3.8.1`、`apache-maven-3.8.4`、`apache-maven-3.9.4`。
- `apache-maven-3.3.9/myrepo/` 为本地仓库缓存（Spring Boot / Thymeleaf 等依赖），可配置 `settings.xml` 的 `localRepository` 指向该目录实现离线构建。
- 使用时将对应版本的 `bin` 目录加入 `PATH` 环境变量即可。

### Nacos

- 解压目录缺少 `nacos-server.jar`（202MB，超出 GitHub 上限），如需运行请从官方下载完整包：
  <https://github.com/alibaba/nacos/releases>
- 目录中已保留 `conf/`（`application.properties`、`mysql-schema.sql` 等）与 `bin/` 启动脚本，可用于快速恢复配置。

### Tomcat

- 免安装版，解压即可使用。启动：`bin/startup.bat`；停止：`bin/shutdown.bat`。

## 版权声明

本仓库中的工具软件版权归各自原作者/公司所有，仅用于个人学习与备份，请勿用于商业用途。如有版权问题，请联系仓库所有者删除。
