# **QEMU-Termux**
Termux QEMU package with SPICE support without ```chroot``` or ```proot```

### Note: Requires Android 7 or newer

## How to install this packages ?

1) ```pkg update && pkg upgrade```
2) Download the ```*.deb``` packages from Releases and enable storage access permission for termux
3) ```apt install /sdcard/Download/liborc-0.4.32_aarch64.deb```
   
   ```apt install /sdcard/Download/libspice-server-0.14.91_aarch64.deb```
   
   ```apt install /sdcard/Download/qemu-system-*```
   
   If ```apt``` didn't work try ```dpkg -i /path/to/debfile.deb```

### QEMU Supported architecture list:
  Android ARM64: i386, x86_64, RISCv32, RISCv64, ARM, AArch64, SPARC, SPARC64, PPC, PPC64
 
## How to use spice with ```qemu```?
 1) Install ```aSPICE``` client from Google Play Store:
  [https://play.google.com/store/apps/details?id=com.iiordanov.freeaSPICE](https://play.google.com/store/apps/details?id=com.iiordanov.freeaSPICE)
 2) In your ```qemu``` command line, remove ```-vnc``` and add 
   ```-spice port=5900,disable-ticketing```
 3) Now open the ```aSPICE``` app and add the address as ```127.0.0.1``` and port ```5900```
