The files were dumped using [`NiceAesth/xppen-tools-builds`](https://github.com/NiceAesth/xppen-tools-builds) from Deco mini7.

```
Runtime device: 6 inch PenTablet [28BD:0928]
Identity: manufacturer=UGTABLET serial=000000
Firmware: UG901_BPU0605L_A (23-08-02_Release01)
```
### **How to flash:**
1. Connect the tablet
2. `xppen-tools dfu`
3. `xppen-tools ihex ic901-code.bin --ic 901 -o ic901-code.hex`
4. `xppen-tools update ic901-code.hex`

**custom** contains `ic901-code.hex`, patched using [`xCuri0/ic901_firmware_tool`](https://github.com/xCuri0/ic901_firmware_tool) with following settings, resulting in 340hz report rate and disabled hardware smoothing:
```
[CoilScan]
coilOnTicks = 30
scanArea = 7x7
adcSampleCount = 15
adcMidSample = 4

[Smoothing]
deadzone = 0

[USB]
bInterval = 1
```
