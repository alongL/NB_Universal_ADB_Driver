NB_Universal_ADB_Driver
=======================

NB(NewBee) Universal ADB Driver


1.FOR WHAT
An universal adb driver for windows.

2.USE
Double click dpinst.exe to install the driver. 
After the windows pops up a window asking you "If you would like to install ther driver", click YES.
If you sign the driver use a certificate which is signed by a CA, there will no window to ask you YES or NO.
More to see http://www.richud.com/wiki/Windows_7_Install_Unsigned_Drivers_CAT_fix

3.INTERNAL
In the android_winusb.inf, 
[Google.NTx86]
;AlongL
%CompositeAdbInterface% = USB_Install, USB\Class_FF&SubClass_42&Prot_01
%SingleAdbInterface% = USB_Install, USB\Class_FF&SubClass_42&Prot_03

This is the most important.
It instructs the devices this driver works for.
It is compatible device ID in windows.

4.HOW to sign the driver.
Please download signTools from	http://www.trustasia.com/solutions/signtools/
Why use this but not inf2cat.exe?
Yes, because we use the compatible ID as USB\Class_FF&SubClass_42&Prot_01 .
First, import your certificate.
Second, new a sign rule.
Third, sign the driver.
You can get some pic in "How to sign it" dir.

5.TODO

6.REFERENCE
http://www.richud.com/wiki/Windows_7_Install_Unsigned_Drivers_CAT_fix
http://blog.csdn.net/v6543210/article/details/37918257
https://github.com/koush/UniversalAdbDriver
http://cdnpic.mgyun.com/files/wdj_drivers/mgyun_driver_64_1.zip
http://cdnpic.mgyun.com/files/wdj_drivers/mgyun_driver_32_1.zip	

