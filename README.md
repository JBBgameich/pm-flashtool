# pm-flashtool
Tool for Flashing Plasma Mobile on top of Halium

# Typical workflow.. (How it works)

- Waits for device to be in fastboot mode,
- Downloads twrp recovery and flashes into recovery
- Boots into recovery
- Downloads Halium hybris-boot and systemimage
- Converts and pushes rootfs and systemimage to /data

# Howto use

To run..

```
git clone https://github.com/plasma-phone-packaging/pm-flashtool.git
cd pm-flashtool
./pm-flash
```

Without options pm-flash script downloads all files again, pass '-c' to let it use cache instead

```
./pm-flash -c
```

After that you can run

```
./halium-install/connect-ssh.sh
```

to get login console
