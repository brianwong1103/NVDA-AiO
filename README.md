# NVDA-AiO
This repo contains Nvidia web driver which was cracked and it can be able to install under all Mac OS version.
## How to install
Just double click and install it as how you install .pkg file first.
### Patch the .kext file
Go to /Library/Extensions/ and find "*NVDAStartupWeb.kext*"
Right click "*Show Package Contents*"
Open "*Info.plist*" and find the codes below:
```*<key>NVDARequiredOS</key>
        <string>Replace this with your system version for example High Sierra is 17G65</string>
```
### Clover KextToPatch
```
 <dict>
            <key>Comment</key>
            <string>Disable NVDARequiredOS</string>
            <key>Disabled</key>
            <false/>
            <key>Find</key>
            <data>
            TlZEQVJlcXVpcmVkT1MA
            </data>
            <key>InfoPlistPatch</key>
            <false/>
            <key>Name</key>
            <string>NVDAStartupWeb</string>
            <key>Replace</key>
            <data>
            AAAAAAAAAAAAAAAAAAAA
            </data>
        </dict>
        
```

