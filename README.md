# Wayne Dynamic Partition ROMS Flash guide

## Before you start...
- Be sure your partitions size is original, this is **IMPORTANT**, or you may brick your device.
- You need to backup your data, your data partition will be formatted.

## Preparations
- Android Debug Tools
- Dynamic Partition Supported Recovery. [**Download**](https://github.com/Diva-Room/DivaRelease/releases/download/wayne_TDA_v0.9.0/recovery.img)
- super_empty.img from [**latest build**](https://github.com/Diva-Room/DivaRelease/releases?q=wayne&expanded=true)
- Connet your device to PC

## Then...
1. Flash Dynamic Partition Supported Recovery into your device

```shell
fastboot flash recovery <RECOVERY_PATH>
```

2. Flash super_empty.img into your device

```shell
fastboot wipe-super <super_empty_PATH>
```

3. Reboot to recovery

```shell
fastboot reboot recovery
```

4. Format your data partiton in recovery

5. Install Dynamic Partition ROMS into your device by:

**Apply update—>Apply from ADB**

Now, be sure your device is connected to your PC, and run

```shell
adb sideload <ROM_PATH>
```

6. Reboot and enjoy

##Know issue and notes.
Some device will face issue, when trying to apply update, will face error install error 1/install aborted/couldn't read partition table and assert failed. To fix it follow this instruction below.
1. Format your data partition / format factory in recovery
2. Advance mode > reboot to recovery
3. Try apply update, it should work. If doesn't, try again from step 1-3.

