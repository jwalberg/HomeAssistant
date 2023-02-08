### NightScout
BloodSugarMonitor is how I monitor my kid's blood sugar. It broadcasts when there's a problem and(if it's night time) turns on some lights.

A second flow in this flow starts when I turn on an input boolean named input_boolean.bg_dka_timer. Every two hours, it reminds me (with pushbullet) to check their BG and ketones.

Monitoring is down with the Nightscout integration. I'm a big fan of Nightscout and Xdrip.

### KeepAlive
KeepAlive monitors my Zigbee routers, WIFI mesh nodes, and BLE presence devices and toggles the associated outlet if the device isn't connected. It also power cycles those devices overnight. I've found that helps with stability during the day.

### Appliances
From the bottom...
1.  5 minutes after I arrive in my home office, if my wife isn't home, the outlet powering the bedroom TV is turned off, then on again. No more forgetting to turn off the TV.
2.  An input button drives two Switchbots that I had intended to attach to the coffee maker, but there wasn't room.
3.  There is a vibration sensor on my dryer, a power meter on my washing machine, and door contact sensors on both. A few minutes after they start running, I get a message saying so, and (for the dryer) an input boolean named dryer_is_running is set. Once the power meter and vibration sensor stop registering for a few minutes, input_booleans (dryer_is_done, washer_is_done) are set. As long as those are set, I get a notifcation once per hour (during the day) telling me the washer or dryer are done. The notification loop is turned off when the door is opened on the relevant appliance.
