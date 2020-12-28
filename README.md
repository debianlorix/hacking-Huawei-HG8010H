# hacking-huawei-HG8010H
Starting from the awesome guide of https://github.com/logon84/Hacking_Huawei_HG8012H_ONT, because I need to modding the firmware of my Huawei HG8010H GPON ONT, unfortunately this huge firm doesn't allow to download software update to users.

I want to replace  my very hot SFP module with this ONT. The problem is that my ONT refuses to match with the OLT, it doesn't establish connection (my ONT continue to slowly blink the LOS green led), I suspect because the webui interface in the ONT configuration has only the Password field and not the SN: my GPON SN has 16 digits with no password.

![ONT authentication](https://i.ibb.co/KhG0h0P/Screenshot-2020-12-15-HG8010-H-1.png)

The next step is open my ONT shell, so I found his NOR that I can confirm is a Spansion S25FL128P flash memory, identical to @Logon84 ONT; to make a flash dump I will use a specific utility for this type of flash chips called "Flashrom". I already had a CH341A mini-programmer, a SOIC16 clip, I use the same of @Logon84:

![NOR schematics](https://github.com/logon84/Hacking_Huawei_HG8012H_ONT/blob/master/pics/8pickit2-pinout.jpg)

Luckily, I had one of them, a Microchip Pickit2 that I had forgotten in a drawer. So, with the pinout of the chip extracted from the datasheet, and the router completely disconnected from the power source (the programmer powers the chip itself) I started connecting the programmer to the chip with  (Pomona 5252). The connection schematic is as follows:

