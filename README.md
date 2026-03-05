## What's this

This is a GitHub Actions repository that detects and automatically builds the latest Sing-box APK package for OpenWRT version 25.x every six hours.

## How to use

First, you need to add this key to make your software package trusted by OpenWRT
```
wget -O /etc/apk/keys/dichgrem.pem   https://dichgrem.github.io/openwrt-singbox/aarch64_cortex-a53/key.pub.pem
```

Then you need to add the repository link; note that it must be the first one
```
nano /etc/apk/repositories

## Add the following link
https://dichgrem.github.io/openwrt-singbox/aarch64_cortex-a53/packages.adb
```

Finally, use the following command to update and install
```
apk update
apk add sing-box
```
