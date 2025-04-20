# Uni-T-UT211B-Firmware-Mod
A simple mod for the Uni-T UT211B clamp multimeter firmware

![uni-t-ut211b-60a-digital-clamp-meter-ac-dc-voltage-detector-plusbuyer](https://github.com/user-attachments/assets/d41e2ccb-750a-410e-ad94-869359009ffc)

*ATTENTION! There is always the possibility of bricking or damaging your meter when messing around with it. I cannot be held responsible for anything you screw up with it. Don't be a dingus and you should be fine.*

I made some changes to the firmware that make this meter more useful as a electronics hobbyist. As it comes from the factory, it is more geared for an electrician, but its ability to measure DC current with the clamp makes it an appealing choice for hobbyists.

This meter is very similar to UT210E which is a popular subject for mods. I used the data provided by the UT210E modding community.

Here are the changes contained in 

 - DC is the first option on applicable switch positions
 - The modes on the Ω position rearranged (continuity, resistance, diode, capacitance)
 - The backlight will stay on for 255 seconds (4.25 minutes)

I used an [XGECU T76](https://www.aliexpress.com/item/3256808123535008.html) to flash this chip but this is way overkill as a [CH341A flasher](https://www.amazon.com/AiTrip-EEPROM-Programmer-CH341A-Adapter/dp/B07VNVVXW6/ref=sr_1_1) is more than capable. 

*ATTENTION! In order to flash the T24C02A EEPROM, you must put the rotary switch in a position other than OFF. I kept forgetting to do this and was getting errors trying to flash and I was pulling my hair out. Don't be a dingus like me.*
