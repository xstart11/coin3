
Debian
====================
This directory contains files used to package Casaxd/Casax-qt
for Debian-based Linux systems. If you compile Casaxd/Casax-qt yourself, there are some useful files here.

## Casax: URI support ##


Casax-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install Casax-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your Casaxqt binary to `/usr/bin`
and the `../../share/pixmaps/Casax128.png` to `/usr/share/pixmaps`

Casax-qt.protocol (KDE)

