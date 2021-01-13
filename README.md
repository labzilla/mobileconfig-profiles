# Useful Configuration Profiles
 
 This is a respository of various .mobileconfig profiles for macOS, iOS, and iPadOS that might be of interest.
 
### How to install:
 
**iOS/iPadOS:**
 
AirDrop the .mobileconfig file to your device, or send it to yourself as an email attachment (and open the attachment). Navigate to Settings > General > Profiles and tap Install. 

**macOS** 
 
 Double click the .mobileconfig file to load the profile. Then, navigate to System Preferences > Profiles and click Install. 
 
# DNS over HTTPS

This profile allows you to configure DNS over HTTPS (encrypted DNS) on devices running iOS/iPadOS 14 and macOS Big Sur. 

The ``OnDemandRules`` section allows you to disable encrypted DNS (and fall back to DHCP provided DNS) when connected to specified wireless networks (such as your home network):

	<dict>
	   <key>InterfaceTypeMatch</key>
	   <string>WiFi</string>
	 <key>SSIDMatch</key>
	   <array>
	      <string>SSID 1</string>
	      <string>SSID 2</string>
	      <string>SSID 3</string>
	      <string>SSID 4</string>
	   </array>
	 <key>Action</key>
	   <string>Disconnect</string>
	</dict>
	
You can disable this by removing the above section from the .mobileconfig file.


