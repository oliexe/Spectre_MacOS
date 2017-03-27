# Yaroze.NET
<img src="https://www.tonymacx86.com/proxy.php?image=http%3A%2F%2Foi67.tinypic.com%2Fj7ffqt.jpg&hash=d314a87e96e65e94d70e69eb2823274a" width="640" width="480">

The new redesigned late-2016 (HP Spectre 13-w0xx ) / early-2017 (HP Spectre 13-ac0xx) HP Spectre x360 2-in-1 is a STUNNING machine 
and looks even better when runs latest macOS. 

Please use the "Issues" tab for **Spectre 13 x360 late-16 related** issues only. If you need support please search on [tonymacx86.com](http://tonymacx86.com) before posting a question there.


## YAROZE.NET Builds

| Version | Download | SHA1 |
|---------|----------|------|
| Beta 1  | [Link]() | b2e0bdd31566f876d67cba036b5d29aef7ff257d  |


## Preparation:

Update your machine BIOS to latest version
Turn off Secure Boot in BIOS !

What you will need:
USB thumb drives (One for clover one for macOS installer is in my opinion better)
macOS machine to work with
Knowledge of booting the macOS installer using Clover

!! Following configs and kexts are needed to boot and use the installer !!

nVME Patch (RehabMan/patch-nvme) (RehabMan, Pike R. Alpha, Mork vom Ork)
Otherwise internal SSD will NOT be detected by installer
HD620 clover config file (RehabMan)
Otherwise installer wont even boot
USBInjectAll.kext (RehabMan)
Nice to have that one USB port working
VoodooPS2Controller.kext (RehabMan)
Otherwise no keyboard or touchpad for u
FakeSMC.kext (netkas, RehabMan)
duh...

Post-Installation:

Step 1 : Add Kexts after installation:
VoodooHDA (autumnrain, slice2009) - Makes audio work
ACPIBatteryManager.kext (RehabMan)- Battery indicator fix
FakePCIID.kext + FakePCIID_Intel_HD_Graphics.kext (RehabMan)- Graphics acceleration
Intel Backlight (RehabMan)- LCD brightness regulation

Step 2: DSDT Patching:

DSDT patching is necessary, in order to continue please read following guide !
https://www.tonymacx86.com/threads/guide-patching-laptop-dsdt-ssdts.152573/

Apply:
Brightness Fix
Battery Fix (battery_HP-G6-2221ss)
HPET Fix
SMBUS Fix
IRQ Fix
RTC Fix
OS Check Fix


Step 3 : Fix graphical glitches in right top corner:

Credit/Source:
https://pikeralpha.wordpress.com/2016/10/30/aapl-properties-for-skylake-graphics/


Step 4 (Optional) : Install Recommended software:
Intel Power Gadget

Step 5 (Optional) : Wi-Fi Adapter replacement:
(source)

Chnage to NGFF BCM94352Z
- Buy the WIFI Card from eBay (M.2 VERSION)
- Ignore the compatibility warning (Does not work for HP Laptops)
- Install the card. Follow instructions (p.24+)
http://h10032.www1.hp.com/ctg/Manual/c04679496
-Finally boot into OS X
http://www.tonymacx86.com/network/104850-guide-airport-pcie-half-mini-v2.html
