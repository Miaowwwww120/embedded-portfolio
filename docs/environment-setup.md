# 开发环境信息

## 虚拟机

| 项目 | 值 |
|---|---|
| 宿主环境 | Windows + VMware Workstation Pro 26H1u1 |
| 虚拟机位置 | D:\VMs\ubuntu-dev |
| CPU / 内存 | 4 核 / 8 GB |
| 磁盘 | 200 GB SCSI（拆分多文件，瘦分配） |
| 快照 | 01-系统装好 / 02-环境就绪 / 03-工具链就绪 |

## 系统

| 项目 | 值 |
|---|---|
| 发行版 | Ubuntu 22.04.5 LTS (jammy) |
| 内核 | 5.15 |
| 用户 | dev |
| 软件源 | 清华 TUNA（sources.list 20 行） |

## 网络

| 位置 | 网卡 | 模式 | IP | 用途 |
|---|---|---|---|---|
| 虚拟机 | ens33 | NAT | 192.168.116.128/24 | 上网 apt/pip |
| 虚拟机 | ens37 | 桥接 | 10.137.121.37/24 | 开发板 tftp/nfs（W5） |
| Windows 主机 | 物理网卡 | — | 10.137.121.253/24 | 与虚拟机同网段，ping 0% 丢包 |

## 工具链

| 项目 | 值 |
|---|---|
| 交叉编译器 | arm-linux-gnueabihf-gcc 11.4.0 |
| 串口别名 | /dev/ttyUSB_board（udev 规则） |
| TFTP 根目录 | /srv/tftp |
| NFS 导出目录 | /srv/nfs/rootfs |
| Python | ~/venv（pyserial / cantools / pytest） |
