# motd Interfaces
Shell script to be used in message-of-the-day (motd) to summarise interfaces on login.

The script will parse all interfaces on a linux host ignoring the loopback interface.
Link-local IPv6 addresses will also be ignored.

# Installation
The easiest way to install is via wget.

For Ubuntu distros, motd is in /etc/update-motd.d/

Access the MOTD folder and perform wget using sudo:
```bash
cd /etc/update-motd.d/
sudo wget https://raw.githubusercontent.com/fon2t/motd-interfaces/main/01-interfaces
sudo chmod 744 01-interfaces
```

**That's it!** Logout from your terminal and log back in.

# Example

The output should be something like:
```bash
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
# Further information

If you want to tidy up some of the noise in motd, change the permissions on the following files:
```bash
sudo chmod 644 50-motd-news
sudo chmod 644 85-fwupd
sudo chmod 644 90-updates-available
```
