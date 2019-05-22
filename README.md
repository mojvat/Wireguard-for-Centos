# Wireguard
one key insstalltion for centos 7

WireGuard one-click installation script CentOS version
prompt:

At present, most of the systems have older kernel versions and do not support WireGuard. You need to upgrade the kernel as follows.
Installation process:

1. Connect to the VPS server using Putty , copy the following command to run:

yum install -y wget && wget https://github.com/mojvat/Wireguard-for-Centos/raw/master/wireguard_install.sh && chmod +x wireguard_install.sh && ./wireguard_install.sh
 

2. When the following interface appears, enter the number 1 and press Enter to start upgrading the kernel:

![alt tag](https://github.com/mojvat/Wireguard-for-Centos/blob/master/p1.jpg?raw=true)

 

3. Wait patiently for the kernel upgrade to complete, the following figure will appear, enter Y as required to restart the system.



 

4. After the system restart is complete, re-use the Putty connection and enter the following command to run the script again:

./wireguard_install.sh

 

5. When the following message appears, enter the number 2 and press Enter to start installing WireGuard:



 

6. Wait patiently, after the installation of WireGuard is completed, the following prompt will appear, where the QR code is used for the mobile client scan code connection. If you have not installed the WireGuard mobile client, you can save the backup by taking a screenshot.



 

7. Proceed to this step, indicating that the WireGuard server has been successfully built, and then use the WireGuard client connection. Once the connection is successful, you can start science online


How to verify that WireGuard is installed successfully
Putty enters wg and returns the following information, including the various connection parameters of WireGuard. Includes public key, private key, port, link, client IP and port, runtime, traffic transfer, and more.



 

Or you can run the following command:

lsmod | grep wireguard

Will get the results of the following picture:


