1 export DEBIAN_FRONTEND=noninteractive

2 apt update

3 apt upgrade

4 apt install git vim sudo

5 vi /etc/ssh/sshd_config

6 reboot

7 adduser isora

8 whereis sudoers

9 chmod +w /etc/sudoers

10 vim /etc/sudoers

11 chmod -w /etc/sudoers

12 passwd root

13 su isora

14 reboot

15 vi /etc/ssh/sshd_config

16 reboot

17 history

18 apt install fail2ban

19 vi /etc/fail2ban/jail.local

20 systemctl start fail2ban

21 systemctl enable fail2ban

22 reboot

23 sh -c 'printf "deb http://deb.debian.org/debian stretch-backports main" > /etc/apt/sources.list.d/stretch-backports.list'

24 apt update

25 apt -t stretch-backports install shadowsocks-libev

26 apt-get install --no-install-recommends build-essential autoconf libtool libssl-dev libpcre3-dev libev-dev asciidoc xmlto automake

27 git clone https://github.com/shadowsocks/simple-obfs.git

28 cd simple-obfs

29 git submodule update --init --recursive

30 ./autogen.sh

31 ./configure && make

32 make install

33 cd ..

34 cd ..

35 reboot

36 vi /etc/shadowsocks-libev/config.json

37 systemctl start shadowsocks-libev

38 systemctl enable shadowsocks-libev

39 systemctl status shadowsocks-libev

40 lsmod | grep bbr

41 echo 'net.ipv4.tcp_fastopen = 3' | sudo tee -a /etc/sysctl.conf

42 echo 'net.core.default_qdisc = fq' | sudo tee -a /etc/sysctl.conf

43 echo 'net.ipv4.tcp_congestion_control = bbr' | sudo tee -a /etc/sysctl.conf

44 sysctl -p

45 lsmod | grep bbr

46 reboot

47 uname -a

48 dpkg –get-selections|grep linux

49 reboot

50 history


