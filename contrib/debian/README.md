
Debian
====================
This directory contains files used to package atomd/atom-qt
for Debian-based Linux systems. If you compile atomd/atom-qt yourself, there are some useful files here.

## atom: URI support ##


atom-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install atom-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your atom-qt binary to `/usr/bin`
and the `../../share/pixmaps/atom128.png` to `/usr/share/pixmaps`

atom-qt.protocol (KDE)

