####1. U-Boot 命令执行过程
    
	>> setenv ipaddr 192.168.129.2
	>> setenv serverip 192.168.129.253
	>> tftp 0x2000000 zImage
	>> tftp 0x1000000 dtb
	>> setenv bootargs console=ttyS0,115200 root=/dev/nfs rw nfsroot=192.168.129.253:/root/rootfs ip=192.168.129.2:192.168.129.253:192.168.129.254:255.255.255.0:armada38x:eth1:none init=/linuxrc
	>> bootz 0x2000000 - 0x1000000
####2. U-Boot脚本编写过程
    
	
	setenv haha "setenv ipaddr 192.168.129.2; setenv serverip 192.168.129.253;tftp 0x2000000 zImage;tftp 0x1000000 dtb;setenv bootargs console=ttyS0,115200 root=/dev/nfs rw nfsroot=192.168.129.253:/root/rootfs ip=192.168.129.2:192.168.129.253:192.168.129.254:255.255.255.0:armada38x:eth1:none init=/linuxrc;bootz 0x2000000 - 0x1000000"



	setenv haha "setenv ipaddr 192.168.129.2; setenv serverip 192.168.129.253;tftp 0x2000000 zImage;tftp 0x1000000 dtb;setenv bootargs console=ttyS0,115200 root=/dev/nfs rw nfsroot=192.168.129.253:/root/rootfs ip=192.168.129.2:192.168.129.253:192.168.129.254:255.255.255.0:armada38x:eth1:none init=/linuxrc;bootz 0x2000000 - 0x1000000"