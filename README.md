# hacking-huawei-HG8010H
Starting from the awesome guide of https://github.com/logon84/Hacking_Huawei_HG8012H_ONT, because I need to modding the firmware of my Huawei HG8010H GPON ONT, unfortunately this huge firm doesn't allow to download software update to users.

I want to replace  my very hot SFP module with this ONT. The problem is that my ONT refuses to match with the OLT, it doesn't establish connection (my ONT continue to slowly blink the LOS green led), I suspect because the webui interface in the ONT configuration doesn't permit more than 10 digits in the SN module (my GPON SN has 16 digits).

