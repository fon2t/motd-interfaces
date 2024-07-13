# motd-interfaces
Shell script to be used in message-of-the-day (motd) to summarise interfaces on login.


# Installation
The easiest way to install is via wget.

For Ubuntu distros, MOTD is in /etc/update-motd.d/

Access the MOTD folder and perform wget using sudo:
```
cd /etc/update-motd.d/
sudo wget https://raw.githubusercontent.com/fon2t/motd-interfaces/main/01-interfaces
sudo chmod 744 01-interfaces
```

**That's it!** Logout from your terminal and log back in.

# Example

The output should be something like:
```
Current Network Configuration
+-----------+-------------------+-----------------------------------------+
| Interface | MAC Address       | IP Addresses                            |
+-----------+-------------------+-----------------------------------------+
| ens3      | 11:22:33:44:55:66 | 172.10.200.3                            |
|           |                   | 2123:e20d:9bbb:beef::3                  |
| ens4      | 11:22:33:44:55:77 | 172.10.300.4                            |
|           |                   | 2123:e20d:9bbb:deaf::4                  |
| ens5      | 11:22:33:44:55:88 | 172.10.400.5                            |
|           |                   | 2123:e20d:9bbb:dead::5                  |
+-----------+-------------------+-----------------------------------------+
```
