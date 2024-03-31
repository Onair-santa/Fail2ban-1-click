## <a href="#"><img src="https://github.com/vpnhood/VpnHood/wiki/images/logo-linux.png" width="32" height="32"></a>(Debian, Ubuntu) Fail2ban-1-click
###  Bash script installs Fail2ban and settings file, and installs nftables to block IP addresses
![Xshell_ehIc7oGPEE](https://github.com/Onair-santa/Fail2ban-1-click/assets/42511409/6ab6b3dc-62a4-4a0c-8b8f-be8f6d2fb222)
#### 💠  Ensure that the `sudo` and `wget` packages are installed on your system:

```
apt install -y sudo wget
```

#### 💠 Root Access is Required. If the user is not root, first run:

```
sudo -i
```

#### 💠 Then:

```
wget "https://raw.githubusercontent.com/Onair-santa/Fail2ban-1-click/main/fail2ban.sh" -O fail2ban.sh && chmod +x fail2ban.sh && bash fail2ban.sh
```
#### It performs the following tasks:
- Remove firewalld, ufw or iptables
- Install nftables
- Open ports 22, 443, 80
- Install Fail2ban
- install config jail.local
- Starting fail2ban
#### Config Fail2ban:
- jail enabled: sshd(port 22), recidive(allport)
- Status command:
  
  ```
  fail2ban-client status
  fail2ban-client status sshd
  fail2ban-client status recidive
  ```

#### 💠 Thanks
https://github.com/fail2ban/fail2ban
