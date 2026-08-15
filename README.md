# CommonTools 常用工具集合

个人开发与运维常用工具软件收集仓库，优先收录绿色免安装版本。

> 由于 GitHub 对单文件有 100MB 上限，本仓库中：
>
> - 绿色免安装工具（Tomcat、Maven、Bandizip 等）直接上传；
> - 体积较大的安装包/系统镜像（CentOS、DataGrip、VMware 等）以 **90MB 分卷压缩包** 形式存放在 [`archives/`](archives/) 目录，合并解压即可还原；
> - 其余安装包仅保留在本地，详见文末「未上传内容」。

## 已上传的绿色工具

| 工具 | 版本 | 说明 |
|------|------|------|
| [apache-tomcat-10.1.20](apache-tomcat-10.1.20/) | 10.1.20 | Java Web 应用服务器（免安装版） |
| [Bandizip](Bandizip/) | 7.29 | 压缩/解压软件（绿色便携版） |
| [Maven](Maven/) | 3.3.9 / 3.8.1 / 3.8.4 / 3.9.4 | Java 项目构建与依赖管理（含本地仓库 myrepo） |
| [nacos](nacos/nacos/) | 2.5.2 | 阿里微服务注册/配置中心（已解压目录，仅含配置与启动脚本） |
| [MQTT](MQTT/) | - | MQTT 协议学习笔记（`MQTT协议.txt`） |

## 分卷压缩包（archives/）

以下大文件已按 90MB/卷 分卷压缩，每个工具一组，每组含多个分卷（`.z01`、`.z02`、…、`.zip`）：

| 压缩包 | 内容 | 分卷数 | 总大小 |
|--------|------|--------|--------|
| CentOs | CentOS-7 DVD 2009/1611、Ubuntu 20.04 桌面版 三个系统镜像 | 143 | ~12.8 GB |
| Datagrip | datagrip-2023.2.3 安装包 | 5 | 425 MB |
| VMwareWorkstationPro17.6.4 | VMware Workstation Pro 17.6.4 安装包 | 5 | 406 MB |
| nacos | nacos-server-2.5.2.zip + nacos-server.jar | 4 | 350 MB |
| HBuilder | HBuilder_8.8.0 安装包 | 3 | 205 MB |
| MySql | mysql-8.1.0 安装包 | 2 | 147 MB |
| Postman | Postman-win64 安装包 | 2 | 130 MB |
| Xshell70421 | Xshell 7 安装包 | 2 | 102 MB |

### 分卷包还原方法

将某一组的**所有分卷文件**（`.z01` ~ `.zip`）下载到同一目录，任选一种方式还原：

- **方式一（推荐）**：用 Bandizip / 7-Zip 打开该组的 `xxx.zip` 文件直接解压，软件会自动合并所有分卷；
- **方式二（命令行合并）**：按顺序将分卷拼接为一个完整 zip 再解压：

  ```cmd
  copy /b CentOs.z01 + CentOs.z02 + CentOs.z03 + CentOs.zip CentOs_full.zip
  ```

## 仅本地保存（未上传）的工具

| 工具 | 说明 | 未上传原因 |
|------|------|-----------|
| Everything | 本地文件极速搜索 | 安装包 |
| FastStone Capture | 截图/录屏工具 | 空目录 |
| FinahShell (FinalShell) | SSH/SFTP 终端工具 | 安装包 |
| node | Node.js 运行时 | 压缩包 |
| Notepad++ | 轻量级文本编辑器 | 安装包 |
| Redis-5.0.14 | 内存缓存数据库 | 压缩包 |
| SQLyog | MySQL 图形化管理工具 | 安装包 |
| Typora | Markdown 编辑器 | 安装包 |
| VSCode | 代码编辑器 | 安装包 |

## 使用说明

### Maven

- 目录内含 4 个版本：`apache-maven-3.3.9`、`apache-maven-3.8.1`、`apache-maven-3.8.4`、`apache-maven-3.9.4`。
- `apache-maven-3.3.9/myrepo/` 为本地仓库缓存（Spring Boot / Thymeleaf 等依赖），可配置 `settings.xml` 的 `localRepository` 指向该目录实现离线构建。
- 使用时将对应版本的 `bin` 目录加入 `PATH` 环境变量即可。

### Nacos

- 解压目录缺少 `nacos-server.jar`，可从 [`archives/nacos.zip`](archives/) 分卷包中还原，或从官方下载完整包：
  <https://github.com/alibaba/nacos/releases>
- 目录中已保留 `conf/`（`application.properties`、`mysql-schema.sql` 等）与 `bin/` 启动脚本，可用于快速恢复配置。

### Tomcat

- 免安装版，解压即可使用。启动：`bin/startup.bat`；停止：`bin/shutdown.bat`。

## 版权声明

本仓库中的工具软件版权归各自原作者/公司所有，仅用于个人学习与备份，请勿用于商业用途。如有版权问题，请联系仓库所有者删除。
