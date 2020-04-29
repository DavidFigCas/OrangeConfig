# OrangeConfig

Apuntes para la instalacion y configuración de la Orange Pi Zero con Armbian y Node-RED

Para autologin
https://forum.armbian.com/topic/1903-autologin-to-armbian-console/

under armbian 5.35 Debian Jessie 3.4.113-sun8i I added the following file /lib/systemd/system/getty@tty1.service.d/20-autologin.conf with root privileges pi is the user, could be root:

# /lib/systemd/system/getty@tty1.service.d/20-autologin.conf

[Service]
ExecStart=
ExecStart=-/sbin/agetty --autologin pi --noclear %I $TERM
If needed, change 'pi' with another username. Then reboot.

Para instalar NR
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)

