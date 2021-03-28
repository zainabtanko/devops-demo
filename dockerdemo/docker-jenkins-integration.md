# Enable jenkins to run sudo commands without password

Add below lines to sudoers file

`$ sudo visudo`
===
ALL     ALL=(ALL:ALL) ALL

jenkins ALL = NOPASSWD: /usr/bin/docker

===
