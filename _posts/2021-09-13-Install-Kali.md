---
layout: post
title: Install Kali
subtitle: Installation
date: 2020-04-12
author: TD
cover-img: /assets/img/walle_rubiks.jpg
thumbnail-img: /assets/img/walle_a.png
share-img: /assets/img/walle_rubiks.jpg
tags: [kali, Linux]
---
You can use the `dpkg` command to see a list of all installed packages on your computer.
```
dpkg --list
```
To uninstall a program use `apt` command. For example, the following command uninstall gimp
and deletes all the configuration file, using the `--purge` command.
```
sudo apt --purge remove gimp
```
If you don't want to remove the configuration files, simply leave out the `--purge` command,
as shown int the following command.
```
sudo apt remove gimp
```
When you uninstall a program, there may be packages that the uninstalled program depended upon that are no longer used. To remove nay unused packages, use the `automove` command, as shown in the following command.
```
sudo apt-get autoremove
```
You can combine the two commands for removing a program and removing dependencies that are no longer being used into one, as shown below.
```
sudo apt purge --auto-remove gimp
```
If you're short on space, you can use the `clean` command to remove downloaded archive files,as shown below.
```
sudo apt clean
```
This command removes the aptitude cache in `/var/cache/apt/archives`. When you install a program, the package file is downloaded and stored in that directory. You don't need to keep the files in that directory. However, the only drawback of deleting them, is that if you decide to install any of those programs again, the packages would have to be downloaded again.

