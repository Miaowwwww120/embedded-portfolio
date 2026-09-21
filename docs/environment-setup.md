# 开发环境信息

| 项目 | 值 |
|---|---|
| Ubuntu | 22.04.5 LTS (jammy), 内核 5.15 |
| 虚拟机 | VMware Workstation Pro 26H1u1 |
| 虚拟机位置 | D:\VMs\ubuntu-dev |
| 磁盘 | 200GB SCSI，拆分为多个文件 |
| 网卡 1 | NAT (ens33, 192.168.116.128) |
| 网卡 2 | 桥接（W5 前添加） |
| 串口别名 | /dev/ttyUSB_board (udev 规则) |
| 交叉工具链 | arm-linux-gnueabihf-gcc 11.4.0 |
| TFTP 根目录 | /srv/tftp |
| NFS 导出 | /srv/nfs/rootfs |
| 快照 | 01-系统装好 / 02-环境就绪 / 03-工具链就绪 |
