# libu2f-udev-dummy
Dummy package to substitute the missing dependency of google-chrome-stable on ubuntu 16.

# Reproduction
_Instructions copied from [SO](https://stackoverflow.com/a/75407138)._  

> Creating a dummy package which provides libu2f-udev fixes the issue. I followed below steps for Ubuntu 16.04. Install equivs package `sudo apt install equivs`.  
```bash
equivs-control libu2f-udev
```
> This creates a file libu2f-udev. Edit this file and give libu2f-udev as value of "Package" and "Provides" keys. Then execute

```bash
equivs-build libu2f-udev
```
> This creates dummy package libu2f-udev_1.0_all.deb. Install it by `sudo dpkg -i libu2f-udev_1.0_all.deb`
> All set.