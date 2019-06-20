FROM dorowu/ubuntu-desktop-lxde-vnc:bionic-lxqt

RUN apt-get update; \
    apt-get install -y alien wget; \
    cd /tmp; \
    wget https://issuecdn.baidupcs.com/issue/netdisk/LinuxGuanjia/baidunetdisk_linux_2.0.1.rpm; \
    alien -i baidunetdisk_linux_2.0.1.rpm; \
    rm baidunetdisk_linux_2.0.1.rpm; \
    apt-get --purge remove -y alien wget; \
    apt-get autoclean; \
    apt-get clean all; \
    apt-get autoremove -y
