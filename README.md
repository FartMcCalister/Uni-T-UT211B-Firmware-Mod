# Uni-T-UT211B-Firmware-Mod
A simple mod for the Uni-T UT211B clamp multimeter firmware

![uni-t-ut211b-60a-digital-clamp-meter-ac-dc-voltage-detector-plusbuyer](https://github.com/user-attachments/assets/7c94d777-5eeb-4a54-9264-b9fe3145fd66)


*ATTENTION! There is always the possibility of bricking or damaging your meter when messing around with it. I cannot be held responsible for anything you screw up with it. Don't be a dingus and you should be fine.*


I made some changes to the firmware that make this meter more useful as a electronics hobbyist. As it comes from the factory, it is more geared for an electrician, but its ability to measure DC current with the clamp makes it an appealing choice for hobbyists.

This meter is very similar to UT210E which is a popular subject for mods. I used the data provided by the UT210E modding community.

Here are the changes contained in 

 - DC is the first option on applicable switch positions
 - The modes on the Ω position rearranged (continuity, resistance, diode, capacitance)
 - The backlight will stay on for 255 seconds (4.25 minutes)

I used an [XGECU T76](https://www.aliexpress.com/item/3256808123535008.html) to flash this chip but this is way overkill as a [CH341A flasher](https://www.amazon.com/AiTrip-EEPROM-Programmer-CH341A-Adapter/dp/B07VNVVXW6/ref=sr_1_1) is more than capable. 

HOW TO MOD (using CH341A flasher):

 1. Follow the procedure in this [video](https://www.youtube.com/watch?v=fX-Fhq9R4uY) until the 2:00 minute mark.
 2. Upload your backup .BIN file to the [calculator]()
 3. Make your desired changes. You can press the "Recommended" button to automatically select the same changes I made above.
 4. Download the modified .BIN file.
 5. In the CH341A Programmer software, select the drop down next to "Auto" and make sure all options are checked.
 6. Upload to the meter's EEPROM chip by opening the modified .BIN file in the CH341A Programmer software and clicking the "Auto" button at the top. 


Resources:

How to flash Uni-T UT210E EEPROM: [video](https://www.youtube.com/watch?v=fX-Fhq9R4uY)
This procedure is virtually identical to the UT211B, just a slightly different board layout. Also I suggest using the calculator linked above to generate the .BIN file as it is easier and safer than modifying it by hand.

Info on the UT210E that was the basis for this mod: [link](https://github.com/af3556/UT210E)

Kerry Wong's datasheet on the DTM0660 ADC in the UT211B: [link](http://www.kerrywong.com/blog/wp-content/uploads/2016/04/DTM0660DataSheet.pdf)



Notes:

*ATTENTION! In order to flash the T24C02A EEPROM, you must put the rotary switch in a position other than OFF. I kept forgetting to do this and was getting errors trying to flash and I was pulling my hair out. Don't be a dingus like me.*


*ATTENTION! The file "Uni-T UT211B Backup.BIN" is a backup from my meter and thus contains calibration data specific to that meter. Do not use it as anything but a reference for the default function configuration HEX data (from address 0x80-0xBF)*
