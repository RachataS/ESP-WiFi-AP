# Wi-Fi SoftAP Example

(See the README.md file in the upper level 'examples' directory for more information about examples.)

This example shows how to use the Wi-Fi SoftAP functionality of the Wi-Fi driver of ESP for serving as an Access Point.

## How to use example

### Configure the project

Open the project configuration menu (`idf.py menuconfig`). 

In the `Example Configuration` menu:

* Set the Wi-Fi configuration.
    * Set `WiFi SSID`.
    * Set `WiFi Password`.

Optional: If you need, change the other options according to your requirements.

### Build and Flash

Build the project and flash it to the board, then run the monitor tool to view the serial output:

Run `idf.py -p PORT flash monitor` to build, flash and monitor the project.

(To exit the serial monitor, type ``Ctrl-]``.)

See the Getting Started Guide for all the steps to configure and use the ESP-IDF to build projects.

* [ESP-IDF Getting Started Guide on ESP32](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html)
* [ESP-IDF Getting Started Guide on ESP32-S2](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s2/get-started/index.html)
* [ESP-IDF Getting Started Guide on ESP32-C3](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c3/get-started/index.html)

## Example Output

There is the console output for this example:

# Output
```css
entry 0x40080698
I (27) boot: ESP-IDF v4.4.5-dirty 2nd stage bootloader
I (27) boot: compile time 10:22:27
I (27) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 4MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00100000
I (83) boot: End of partition table
I (88) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=13de0h ( 81376) map
I (125) esp_image: segment 1: paddr=00023e08 vaddr=3ffb0000 size=03038h ( 12344) load
I (131) esp_image: segment 2: paddr=00026e48 vaddr=40080000 size=091d0h ( 37328) load
I (147) esp_image: segment 3: paddr=00030020 vaddr=400d0020 size=701cch (459212) map
I (313) esp_image: segment 4: paddr=000a01f4 vaddr=400891d0 size=0b6e8h ( 46824) load
I (342) boot: Loaded app from partition at offset 0x10000
I (343) boot: Disabling RNG early entropy source...
I (354) cpu_start: Pro cpu up.
I (354) cpu_start: Starting app cpu, entry point is 0x4008117c
0x4008117c: call_start_cpu1 at /Users/rachatasupanurak/esp/esp-idf/components/esp_system/port/cpu_start.c:147

I (0) cpu_start: App cpu up.
I (368) cpu_start: Pro cpu start user code
I (368) cpu_start: cpu freq: 160000000
I (368) cpu_start: Application information:
I (373) cpu_start: Project name:     ESP-WiFi-AP
I (378) cpu_start: App version:      c6aad5f-dirty
I (384) cpu_start: Compile time:     Sep 11 2023 10:33:53
I (390) cpu_start: ELF file SHA256:  991d38810c4f3268...
I (396) cpu_start: ESP-IDF:          v4.4.5-dirty
I (401) cpu_start: Min chip rev:     v0.0
I (406) cpu_start: Max chip rev:     v3.99 
I (411) cpu_start: Chip rev:         v3.0
I (416) heap_init: Initializing. RAM available for dynamic allocation:
I (423) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (429) heap_init: At 3FFB6CA0 len 00029360 (164 KiB): DRAM
I (435) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (441) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (448) heap_init: At 400948B8 len 0000B748 (45 KiB): IRAM
I (455) spi_flash: detected chip: generic
I (459) spi_flash: flash io: dio
I (464) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (550) wifi softAP: ESP_WIFI_MODE_AP
I (560) wifi:wifi driver task: 3ffbf210, prio:23, stack:6656, core=0
I (560) system_api: Base MAC address is not set
I (560) system_api: read default base MAC address from EFUSE
I (580) wifi:wifi firmware version: 0f80fa0
I (580) wifi:wifi certification version: v7.0
I (580) wifi:config NVS flash: enabled
I (580) wifi:config nano formating: disabled
I (590) wifi:Init data frame dynamic rx buffer num: 32
I (590) wifi:Init management frame dynamic rx buffer num: 32
I (600) wifi:Init management short buffer num: 32
I (600) wifi:Init dynamic tx buffer num: 32
I (600) wifi:Init static rx buffer size: 1600
I (610) wifi:Init static rx buffer num: 10
I (610) wifi:Init dynamic rx buffer num: 32
I (620) wifi_init: rx ba win: 6
I (620) wifi_init: tcpip mbox: 32
I (620) wifi_init: udp mbox: 6
I (630) wifi_init: tcp mbox: 6
I (630) wifi_init: tcp tx win: 5744
I (640) wifi_init: tcp rx win: 5744
I (640) wifi_init: tcp mss: 1440
I (640) wifi_init: WiFi IRAM OP enabled
I (650) wifi_init: WiFi RX IRAM OP enabled
I (1400) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (1500) wifi:mode : softAP (24:d7:eb:0e:cb:21)
I (1500) wifi:Total power save buffer number: 16
I (1500) wifi:Init max length of beacon: 752/752
I (1500) wifi:Init max length of beacon: 752/752
I (1500) wifi softAP: wifi_init_softap finished. SSID:myssid_161 password:64030161 channel:1
I (21310) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (21310) wifi:station: 46:4c:17:ef:ea:b2 join, AID=1, bgn, 20
I (21330) wifi softAP: station 46:4c:17:ef:ea:b2 join, AID=1
I (21690) wifi:<ba-add>idx:2 (ifx:1, 46:4c:17:ef:ea:b2), tid:0, ssn:2, winSize:64
I (21840) wifi:<ba-add>idx:3 (ifx:1, 46:4c:17:ef:ea:b2), tid:1, ssn:0, winSize:64
I (22950) esp_netif_lwip: DHCP server assigned IP to a station, IP is: 192.168.4.2
I (24740) wifi:<ba-del>idx
I (24740) wifi:<ba-add>idx:2 (ifx:1, 46:4c:17:ef:ea:b2), tid:0, ssn:52, winSize:64
I (26850) wifi:station: 46:4c:17:ef:ea:b2 leave, AID = 1, bss_flags is 658531, bss:0x3ffb89b0
I (26850) wifi:new:<1,0>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (26850) wifi:<ba-del>idx
I (26850) wifi:<ba-del>idx
I (26860) wifi softAP: station 46:4c:17:ef:ea:b2 leave, AID=1
I (28060) wifi:new:<1,0>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (28070) wifi:station: 46:4c:17:ef:ea:b2 join, AID=1, bgn, 20
I (28090) wifi softAP: station 46:4c:17:ef:ea:b2 join, AID=1
I (28220) esp_netif_lwip: DHCP server assigned IP to a station, IP is: 192.168.4.2
I (28630) wifi:<ba-add>idx:2 (ifx:1, 46:4c:17:ef:ea:b2), tid:0, ssn:2, winSize:64
```

## Troubleshooting

For any technical queries, please open an [issue](https://github.com/espressif/esp-idf/issues) on GitHub. We will get back to you soon.
