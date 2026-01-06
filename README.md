Steps -
1. Run `pacman -S python python-beautifulsoup4 python-requests`
2. Clone and cd into the repo
3. Run `makepkg -si`
4. Enable service `systemctl enable nessusagent.service`
5. Start service `systemctl start nessusagent.service`
6. `cd /opt/nessus-agent/sbin/`
7. `sudo su`
8. `./nessuscli agent link --key=<key> --name=<name> --groups=<group> --host=<host> --port=<port>`
9. Check agent link status `./nessuscli agent status`
