
Debian
====================
This directory contains files used to package mochachaind/mochachain-qt
for Debian-based Linux systems. If you compile mochachaind/mochachain-qt yourself, there are some useful files here.

## mochachain: URI support ##


mochachain-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install mochachain-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your mochachainqt binary to `/usr/bin`
and the `../../share/pixmaps/mochachain128.png` to `/usr/share/pixmaps`

mochachain-qt.protocol (KDE)

