# RackNerd 洛杉矶DC02机房IPv4地址更换计划详解

## 重要通知：IPv4地址变更安排

RackNerd洛杉矶DC02机房将于2023年10月1日至11月15日期间分批次进行IPv4地址更换。此次变更**仅影响IPv4地址**，用户数据、设置和IPv6地址将保持不变。

### 变更背景说明
- **原因**：上游服务商Multacom（现属EdgeCentres旗下）启动IPv4网络重新编号项目
- **目的**：配合数据中心长期发展规划和扩展需求
- **影响范围**：仅限洛杉矶DC02机房的KVM VPS服务

👉 [【点击查看】2025年最新 Racknerd 优惠码及特价云服务器方案汇总](https://bit.ly/Rack_Nerd)

## 详细更换时间表

更换工作将按以下节点名称分批进行：

- **第一阶段**：10月1日-15日  
  节点名称以LAXSSD1*至LAXSSD3*开头的VPS
- **第二阶段**：10月15日-31日  
  节点名称以LAXSSD4*至LAXSSD6*开头的VPS
- **第三阶段**：11月1日-15日  
  节点名称以LAXSSD7*至LAXSSD9*或LAX0*开头的VPS

## 如何确认您的节点信息

1. 登录SolusVM控制面板：[https://nerdvm.racknerd.com/](https://nerdvm.racknerd.com/)
2. 点击对应VPS的"Manage"选项
3. 查看"Node"列信息即可确认所属节点

## 变更执行细节

### 自动化处理流程
- 工程团队将全程监控自动化更换过程
- 每台VPS平均停机时间不超过2分钟
- 系统将自动更新操作系统网络配置

### 通知方式
- 变更完成后会收到标题为"[RackNerd] New IP Address Assigned"的邮件
- 邮件包含新旧IP地址对照信息
- 也可通过SolusVM控制面板实时查看

## 长期发展优势

此次变更将为用户带来以下长期利益：
1. 解决Multacom数据中心空间和电力限制问题
2. 提高洛杉矶DC02机房的库存稳定性
3. 为未来扩展新数据中心位置奠定基础
4. 保持原有的优质网络性能（Multacom BGP混合网络）

## 技术支持与联系方式

如有特殊需求或问题，请通过以下方式联系：
- 邮箱：engineering@racknerd.com
- 建议在收到通知邮件后7天内提出特殊需求

> **温馨提示**：RackNerd承诺此次变更不会导致服务价格调整，持续为用户提供高性价比的云服务器解决方案。