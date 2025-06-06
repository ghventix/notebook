---

order: 80
title: 文件与IO管理

---

## 文件系统

::: info 文件系统的基本概念
- **文件**：是对磁盘等外部存储介质上数据的逻辑抽象
- **文件系统**：负责管理和存储文件的系统软件
- **目录**：由文件索引项组成的特殊文件

文件系统的主要功能：
1. 文件的存储、检索和修改
2. 文件的共享和保护
3. 文件的命名和组织
4. 提供用户接口
:::

### 文件管理

::: tip 文件的基本操作
1. **创建文件**
   - 申请目录项
   - 分配存储空间

2. **读写文件**
   - 顺序访问
   - 随机访问

3. **删除文件**
   - 释放目录项
   - 回收存储空间

4. **文件保护**
   - 访问控制列表（ACL）
   - 用户权限管理
:::

### 目录管理

::: info 目录结构
1. **单级目录**：所有文件在同一目录下
2. **两级目录**：区分系统文件和用户文件
3. **树形目录**：现代操作系统普遍采用
4. **图形目录**：允许文件共享的目录结构
:::

### 磁盘调度

::: tip 常见的磁盘调度算法
1. **先来先服务（FCFS）**
   - 按照请求到达的顺序进行调度
   - 公平但性能不佳

2. **最短寻道时间优先（SSTF）**
   - 优先处理距当前磁头最近的请求
   - 可能导致饥饿现象

3. **扫描算法（SCAN）**
   - 电梯算法
   - 磁头沿一个方向移动直到没有请求

4. **循环扫描（C-SCAN）**
   - 单向扫描
   - 返回时直接移动到起始位置
:::

## I/O管理

::: info I/O管理的基本功能
1. **设备管理**
   - 设备的分配与回收
   - 设备的启动与控制

2. **缓冲管理**
   - 减少CPU和I/O设备速度不匹配的影响
   - 提高系统的并发度

3. **设备驱动程序**
   - 实现设备的具体操作
   - 提供统一的设备接口
:::

### I/O控制方式

::: tip 主要的I/O控制方式
1. **程序直接控制**
   - CPU轮询检查I/O设备状态
   - 适用于简单的I/O操作

2. **中断驱动方式**
   - I/O完成时通过中断通知CPU
   - 减少CPU等待时间

3. **DMA方式**
   - 直接内存访问
   - 数据传输不需要CPU干预

4. **通道方式**
   - 专门的I/O处理器
   - 实现I/O操作的并行处理
:::