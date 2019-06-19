FROM dorowu/ubuntu-desktop-lxde-vnc:bionic-lxqt

ENV LANG=zh_CN.UTF-8 \
    LC_ALL=zh_CN.UTF-8
    
# download BaiduNetdisk
RUN apt-get update; \
    apt-get install -y alien wget; \
    cd /tmp; \
    wget https://issuecdn.baidupcs.com/issue/netdisk/LinuxGuanjia/baidunetdisk_linux_2.0.1.rpm; \
    alien baidunetdisk_linux_2.0.1.rpm; \
    dpkg -i baidunetdisk_linux_2.0.1.deb; \
    rm baidunetdisk_linux_2.0.1.rpm; \
    rm baidunetdisk_linux_2.0.1.deb; \
    apt-get --purge remove alien wget; \
    apt-get autoclean; \
    apt-get clean all; \
    apt-get autoremove
