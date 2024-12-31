Steps -
- Run `pacman -S python python-beautifulsoup4 python-requests`
- Clone and cd into the repo
- Run `makepkg -si`
- Enable service `systemctl enable nessusagent.service`
- Start service `systemctl start nessusagent.service`
- `cd /opt/nessus-agent/sbin/`
- `sudo su`
- `./nessuscli agent link --key=<key> --name=<name> --groups=<group> --host=<host> --port=<port>`
- Check agent link status `./nessuscli agent status`
