openmediavault-rsnapshot
========================

This is a plugin for OpenMediaVault 0.5x.
It allows the user to configure incremental backups of any shared folder to any other shared folder.

It uses rsnapshot for creating the backups, which uses hardlinks to save disk space, and also
automatically rotates the backups.

The created backups can be browsed using SMB/NFS/... by the user.

More information and screenshots at: http://forums.openmediavault.org/viewtopic.php?f=13&t=2726&p=18450#p18450


Developing Guide (for me only ;))
======

Lesen:

http://wiki.ubuntuusers.de/Grundlagen_der_Paketerstellung

http://en.wikipedia.org/wiki/Debian_build_toolchain

Installieren:

sudo apt-get install build-essential debhelper dh-make quilt fakeroot lintian 
sudo apt-get install python-pip devscripts
pip install transifex-client

Dann dieses repo clonen.

Im Modulverzeichnis aufrufen:

dpkg-buildpackage -us -uc 

Plugin installieren!

Installation fehlgeschlagen/hängt? vermutlich konnte der omv-engined nicht starten:

/usr/sbin/omv-engined -fd