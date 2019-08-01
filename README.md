# MountChecker
Little script that check mounted files systems and start/stop service.

If a filsystem is not mounted, this script will stop the configured service, try to do `mount -a` and restart the services if the mounts are back.

Compatible with [Gotify](https://gotify.net) for notification.

## Install

 1. Download `mount_checker` into `/opt/mountChecker/`.
 2. Change the settings inside the file to match you'r need.
 3. Make it executable: `chmox +x /opt/mountChecker/mount_checker`
 4. Check if everything work fine: `/opt/mountChecker/mount_checker`
 5. Download ` mountChecker.service` into `/etc/systemd/system/`
 6. Enable the service `systemctl enable mountChecker.service`
 7. Finaly start it `service mountChecker start` and check the logs `journalctl -u mountChecker.service`


