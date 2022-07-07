# nspanel
# Newbie to Home Assistant, with NSPanel being my first ESPHome device, first time flashing with usb to serial adapter, and, ofc, first time using Nextion Editor
# This is my final, I suppose, but I've said that a dozen times and I still can't help adding new features, breaking everything, rinsing and repeating. 
# I started with MarkWattTech's youtube tutorial on how to flash the custom firmware and upload the custom gui, and from that I modified, added and removed various features
# 
# In the .yaml file, a big part of the code is commented out, since I ended up handling the commands and automations through home assistant. 
# The way dynamic icons and sensor updates was configured in the original configuration that I used as baseline, forced most of the processing to be done on the esp module itself, pulling data from HA entities with sensor objects. 
# After adding some components, I stumbled accross a wall, having the device in bootloop because the esp module couldn't handle all those objects
# So I ended up using A LOT the "send command" service in HA, and created all the button actions, status updates, and automations in HA.
# Since HA sensor values were pulled nevertheless, and HA handled all the outputs, I saw no better way than to set all the conditions, iflese's etc in HA, and send the appropriate values
# as commands to the display, ofc using templates. 

# Hope this helps and inspires some of you to tinker with your NSPanel and create the configuration that suits you best. 
