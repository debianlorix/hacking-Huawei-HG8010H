# hacking-huawei-HG8010H
Starting from the awesome guide of https://github.com/logon84/Hacking_Huawei_HG8012H_ONT, because I need to modding the firmware of my Huawei HG8010H GPON ONT, unfortunately this huge firm doesn't allow to download software update to users.

I want to replace  my very hot SFP module with this ONT. The problem is that my ONT refuses to match with the OLT, it doesn't establish connection (my ONT continue to slowly blink the LOS green led), I suspect because the webui interface in the ONT configuration has only the Password field and not the SN: my GPON SN has 16 digits with no password.

![ONT authentication](https://i.ibb.co/KhG0h0P/Screenshot-2020-12-15-HG8010-H-1.png)

The next step is open my ONT shell: 

![ONT board ante](https://i.ibb.co/8MRtj6w/IMG-20201228-153427.jpg)

![ONT board retro](https://i.ibb.co/KLnZgny/IMG-20201228-153428.jpg)

This is the NOR flash chip, I can confirm is a Spansion S25FL128P flash memory, identical to those of @Logon84 ONT:

![8010H NOR](https://i.ibb.co/gw2C9fM/IMG-20201228-153429.jpg)

To make a flash dump I must use a specific utility for this type of flash chips called "Flashrom". I already had a CH341A mini-programmer, but only with a SOIC8 clip, so I bought a SOIC16 one, I use the same schematic posted by @Logon84:

![NOR schematics](https://github.com/logon84/Hacking_Huawei_HG8012H_ONT/blob/master/pics/8pickit2-pinout.jpg)

