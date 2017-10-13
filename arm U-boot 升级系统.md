####1. 文件通过tftp下载到Uboot内存中
	
	>> setenv ipaddr 192.168.129.2
	>> setenv serverip 192.168.129.253
	>> tftp 0x2000000 zImage
	>> tftp 0x1000000 dtb
	>> setenv bootargs console=ttyS0,115200 root=/dev/nfs rw nfsroot=192.168.129.253:/root/rootfs ip=192.168.129.2:192.168.129.253:192.168.129.254:255.255.255.0:armada38x:eth1:none init=/linuxrc
	>> bootz 0x2000000 - 0x1000000
    
	uboot命令
	tftp mem_addr file_name

	tftp 0x2000000 zImage
	zImage保存到Uboot的内存地址0x2000000

####2. NFS
    
	Uboot中设置ip地址、ip子网掩码、网关
	nfs 0x30008000 192.168.1.4:/nfs/zImage
















参考：
1.[固件烧写方式](https://www.crifan.com/files/doc/docbook/firmware_download/release/htmls/ch03_download_method.html)








