## <a href="#"><img src="https://github.com/vpnhood/VpnHood/wiki/images/logo-linux.png" width="32" height="32"></a>(Debian11, Ubuntu20) Fail2ban-1-click
### Fail2ban - the open-source security solution for youre server
###  Bash script installs Fail2ban and settings file, and installs nftables to block IP addresses
![image](https://github.com/Onair-santa/Fail2ban-1-click/assets/42511409/0d8d0f7e-4e6f-4d31-8d59-81049d15137a)
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
