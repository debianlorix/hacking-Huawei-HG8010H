# hacking-huawei-HG8010H
Starting from the awesome guide of https://github.com/logon84/Hacking_Huawei_HG8012H_ONT, because I need to modding the firmware of my Huawei HG8010H GPON ONT, unfortunately this huge firm doesn't allow to download software update to users.

I want to replace  my very hot SFP module with this ONT. The problem is that my ONT refuses to match with the OLT, it doesn't establish connection (my ONT continue to slowly blink the LOS green led), I suspect because the webui interface in the ONT configuration has only the Password field and not the SN: my GPON SN has 16 digits with no password.

![ONT authentication](https://i.ibb.co/KhG0h0P/Screenshot-2020-12-15-HG8010-H-1.png)

The next step is open my ONT shell and found his NOR; 

![NOR](https://www.kynix.com/Detail/794449/FL128SAIF01.html)

