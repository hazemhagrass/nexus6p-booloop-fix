# nexus6p-booloop-fix

Several Smartphones models introduced between 2015, 2016 were discovered by users to have common problem, all of which eventually cause the device unstable , and stuck in a loop or reboots or wont turn on . this issue had been nicknamed as **bootloop** , This issue affected on mainly Nexus devices 6p and 5x.

This is mainly a hardware failure related to the BIG cluster has occurred. This fix remedies the problem by disabling the BIG cores. Unfortunately, this does mean that you will take a performance hit.

Thankfully [XCnathan32](https://forum.xda-developers.com/nexus-6p/general/guide-fix-nexus-6p-bootloop-death-blod-t3640279) with some XDA developers has rallied together and for now, it seems like a fix has been found However this fix does come at a cost in terms of performance as it essentially disables four of the cores on the Qualcomm snapdragon810 chipset, which means that in some instances, especially with more intensive applications, you will notice some lag.

**This repo is only gathering all info needed to get Nexus 6p up and running.**

### Prerequists:

1. Ubuntu/MacOS. these steps never tested over windows environment
2. Fastboot installed on your computer
3. Unlocked OEM Bootloader
	1. `fastboot oem unlock`
	2. `fastboot reboot`

### Steps(Nexus 6p):

1. `git clone git@github.com:hazemhagrass/nexus6p-booloop-fix.git`
2. `cd nexus6p-booloop-fix/`
3. Turn your device Off or wait until the battery dies.
4. Hold down power and volume down to start device bootloader.
5. Connect your device with USB to your compuer and make sure that it's listed in fastboot devices. run the following command on your comuter terminal to make sure that your device is visible to your computer.
	1. `fastboot devices` 
6. run the following command on your terminal `./init.sh `to flush the new kernel over it.

After these steps were completed I haven't experienced any random rebooting or Bootloops. Yes, this ”fix" hobbles your device but it is still quite functional.