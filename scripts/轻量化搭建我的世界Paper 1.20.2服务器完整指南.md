# 轻量化搭建我的世界Paper 1.20.2服务器完整指南

> 本文最后更新于352天前，部分配置可能随版本更新有所调整。建议结合最新官方文档进行操作。

## 一、开服方案对比

传统我的世界服务器搭建通常依赖第三方管理面板（如翼龙面板、MCSM面板等），虽然简化了操作流程，但会额外占用服务器资源。本教程将重点介绍**轻量化开服方案**，直接使用Paper核心搭建1.20.2版本插件服，特别适合**低配置云服务器**。

👉 [【点击查看】2025年最新雨云优惠码及特价云服务器方案汇总](https://bit.ly/RainYun)

## 二、服务器配置建议

### 基础硬件要求
- **CPU**：至少2核（推荐R9-5900X等游戏级处理器）
- **内存**：4GB起步（支持10-20人同时在线）
- **存储**：SSD固态硬盘优先

### 网络配置
- 选择NAT网络架构
- 需进行端口映射（后续步骤详解）
- 推荐系统：Debian 11

## 三、环境准备步骤

### 1. Java环境配置
bash
# 更新系统并安装Java17
apt update -y
apt install openjdk-17-jdk -y

# 验证安装
java -version

**常见问题处理**：
若系统预装Java8，可通过以下命令切换：
bash
# 雨云专用命令
set_java.sh 17

# 通用解决方案
vim /etc/profile  # 修改JAVA_HOME路径
source /etc/profile

## 四、Paper服务端部署

### 1. 下载安装
bash
mkdir ~/mc && cd ~/mc
wget https://api.papermc.io/v2/projects/paper/versions/1.20.4/builds/365/downloads/paper-1.20.4-365.jar

### 2. 首次启动配置
bash
java -jar paper-1.20.4-365.jar nogui

- 修改`eula.txt`将`false`改为`true`
- 建议配置`server.properties`：
  properties
  motd=我的私人服务器
  difficulty=normal
  max-players=20
  view-distance=10
  

## 五、服务器管理技巧

### 1. 持久化运行
bash
screen -S mc
java -jar paper-1.20.2-280.jar nogui
# 按Ctrl+A+D退出会话
screen -r mc  # 重新连接

### 2. 网络端口映射
- 内网端口：25565
- 外网端口：自定义未占用端口

## 六、连接测试
使用映射后的外网地址（IP:端口）即可通过游戏客户端连接。建议首次登录后立即设置OP权限：
mc
/op 你的游戏ID

> 小贴士：定期备份world文件夹可防止数据丢失

通过本方案搭建的服务器资源占用降低约40%，特别适合学生党和小型游戏社群。如需更高性能方案，可考虑专业游戏云服务器：

[【限时特惠】高性能我的世界专用服务器低至5折起](https://bit.ly/RainYun)