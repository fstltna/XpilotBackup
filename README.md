# XpilotBackup - backup script for the Xpilot game Server (1.0)
Creates a hot backup of your Xpilot game server installation and optionally copies it to a offsite server.

Official support sites: [Official Github Repo](https://github.com/fstltna/XpilotBackup) - [Official Forum](https://gameplayer.club/index.php/forum/operator-scripts) ![XPilot Sample Screen](https://gameplayer.club/images/XPilot.png) 

[![Visit our IRC channel](https://kiwiirc.com/buttons/irc.freenode.net/XPilotFans.png)](https://kiwiirc.com/client/irc.freenode.net/?nick=guest|?#XPilotFans)

---

1. Make sure ssh-keygen is installed: "apt install ssh-keygen"
2. Run "ssh-keygen" and when asked for the password just press enter twice
3. Run "ssh-copy-id -i ~/.ssh/id_rsa.pub your-destination-server" - This will ask you for your remote password. This is normal.
4. Edit the settings at the top of xpilotbackup.pl if needed
5. After the first run edit the ~/.xpilotbackuprc and change your settings if you want to use the offsite backup feature. The next run it should save to your remote host.
6. create a cron job like this:

        1 1 * * * /root/XpilotBackup/xpilotbackup.pl

7. This will back up your Xpilot installation at 1:01am each day, and keep the last 5 backups.

If you need more help visit https://GamePlayer.club/ and check out this website: https://superuser.com/questions/555799/how-to-setup-rsync-without-password-with-ssh-on-unix-linux

