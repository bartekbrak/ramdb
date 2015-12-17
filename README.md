# RAMDB - move whole mysql to RAM for speed.

This is work in progress. I have used and tested this script for
over two years and eliminated common problems but you should use it 
at your own risk. If you don't know bash and don't know how mysql
is structred on your disk, you risk loosing data.

The only system supported now is Ubuntu. MacOs support will come one day.

The script will create backups each time it's run but the risk is still there.

Don't use it if you hold importand data locally. This script is most useful
for debug and development which relies on mysql. 

# Usage:

```
$ ramdb -h
mysql ramdisk switcher, bartek.rychlicki@gmail.com, version 1387128242

this script has been tested but do not trust it, actual db damage 
is likely and indeed happened to me, so be warned

usage:
    sudo ramdb [-q] action
actions:
    on
    off
    status|st
    remove_backups
    force_backup
    recover
```

# Instalation

```
wget https://raw.githubusercontent.com/bartekbrak/ramdb/master/ramdb
chmod +x ramdb
vim ramdb  # adjust the size, change SIZE
# copy to wherever you have your executables, I like ~/bin
```
