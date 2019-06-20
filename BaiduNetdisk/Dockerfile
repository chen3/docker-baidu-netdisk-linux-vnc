FROM dorowu/ubuntu-desktop-lxde-vnc:bionic-lxqt

RUN apt-get update; \
    apt-get install -y alien wget; \
    cd /tmp; \
    wget https://issuecdn.baidupcs.com/issue/netdisk/LinuxGuanjia/baidunetdisk_linux_2.0.1.rpm; \
    [ -f baidunetdisk_linux_2.0.1.rpm ] || exit 1; \
    alien -i baidunetdisk_linux_2.0.1.rpm; \
    [ -f /opt/baidunetdisk/baidunetdisk ] || exit 2; \
    rm baidunetdisk_linux_2.0.1.rpm; \
    apt-get --purge remove -y alien wget; \
    apt-get autoclean; \
    apt-get clean all; \
    apt-get autoremove -y
