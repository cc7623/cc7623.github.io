
### AppleInternal List
#### A list of a bit of AppleInternal software. Found from multiple sources- Reddit, archive.org, Twitter, and Telegram. *Note- there are more people which have uploaded software, I just forgot to credit them here. All credits to original uploaders.*
Engaging in illegal activity is not condoned. This information is provided for __*educational purposes only*__. Use at your ***OWN RISK***. If anything is missing or you would like to add to the list (please, if you can), [create an issue](https://github.com/cc7623/cc7623.github.io/labels/appleinternal%20addition%2Ffix) and I'll get to it.

```
Added InternalUI instructions for MacOS and Platoon for Artists. Uploading Demo Apps now...
-cc7623, 2024-03-11 12.47pm
```

***

#### Sections
[40GB AppleInternal Collection, and how to extract](https://cc7623.github.io/appleinternal-list#40gb-appleinternal-collection)  
[Put device in or out of DemoMode](https://cc7623.github.io/appleinternal-list#put-device-in-demomode)  
[Firmwares/Updates](https://cc7623.github.io/appleinternal-list#internaluiswitchboarddemo-firmwares)  
[Applications](https://cc7623.github.io/appleinternal-list#applications)  
[DemoLoops (enroll and non-enroll methods)](https://cc7623.github.io/appleinternal-list#demoloops)  
[Links (can't be used w/out AppleConnect acct.)](https://cc7623.github.io/appleinternal-list#links-credit)

***

#### 40GB AppleInternal Collection

Download [here](https://archive.org/details/apple-internal-collection).  

========How to extract it?========  
`Windows:`  
1. Download LinuxFileViewer or Transmac.
2. Right click the DMG file and open.
(Thanks to [/u/Codix_](https://www.reddit.com/r/Apple_Internal/comments/tfvwh1/comment/kjbn81z/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button).)

`Mac:`
1. Double-click the DMG
2. Click on the drive icon named "AppleInternal Collection." It should be on your desktop.

`Linux:`
1. Just double-click it.

***

#### Put device in DemoMode:

WARNING- This will erase all data on the device and you might not be able to unenroll.

*1 - go to demounit.Apple.com ( on a spare device not on the one you wanna install demo mode on )  
2 - sign in with your Apple ID  
3 - install the app  
4 - choose a random Apple Store ( doesn’t matter )  
5 - tap enroll a new device  
6 - click manual entry  
7 - enter the serial number of your device ( the device you’re trying to put demo mode on )  
8 - click submit  
9 - click confirm then it will show you a code. **write down/save for later**  
10 - reset all content and settings {on the device you wanna install demo mode on not the device you have the demounit app on)  
11 - continue setup until you’re asked for a code enter the code you got at step 9  
12 - wait until the demo update finishes  
13 - you’re good to go !*  
([credit](https://web.archive.org/web/20240205022229/http://web.archive.org/screenshot/https://www.reddit.com/r/Apple_Internal/comments/13ixfa7/comment/jkehx91/?utm_name=web3xcss))

#### Get device out of DemoMode

- Go to the admin menu (three fingers in the corner. picture link at the bottom)
- Press unenroll, it will work fine! However, if the store is enrolled in the Demo Device Lock Theft Deterrence Program, you have to use the web app, which you don't have the password to, so you can't unenroll it.  
Here is an image on how to do the admin menu:  
Just put your three fingers in the areas there, and then choose reset.  
[https://imgur.com/a/yOlphSe](https://web.archive.org/web/20240205021858/http://web.archive.org/screenshot/https://imgur.com/a/yOlphSe) (2nd image)

***

#### InternalUI/Switchboard/Demo Firmwares

[How to install InternalUI Firmwares](https://cc7623.github.io/internaluifirmware.html):

```
WARNING! IF SOMETHING GOES WRONG, YOUR
DEVICE WILL HAVE TO BE RESET. ONLY ATTEMPT THIS ON A TEST DEVICE OR SECONDARY DEVICE.
Check down below for an InternalUI build. NONUI DUMPS WILL NOT WORK.

This tutorial has been tested for iOS 13 and 7. It might work on other versions as well.
Visit the link above where you can download the InternalUI builds.
This will take up from 2GB extra to 6GB extra.

========PART I: INSTALLING INTERNAL SETTINGS========

1. Download InternalUI dump (link above)
2. Extract it (7zip or WinRAR work)
3. In root folder [DEVICE], create a folder called “AppleInternal” (don’t include these “”)
4. Go to /AppleInternal/ [DUMP] and copy the Library folder to
/AppleInternal/ [DEVICE]

5. Go to /System/library/CoreServices/systemversion.plist [DEVICE]
6. Add “ReleaseType” string = “Internal” and “ProductType” string = “Internal”

<key>ReleaseType</key>
<string>Internal</string>
<key>ProductType</key>
<string>Internal</string>

7. Go to /System/Library/PrivateFrameworks [DUMP]

8. Copy everything in there to /System/Library/PrivateFrameworks [DEVICE]
USE 3UTOOLS! DO NOT USE iFUNBOX! IT WILL REPLACE EVERYTHING WITHOUT ASKING.
DO NOT PRESS REPLACE! JUST SKIP ANY DUPLICATE FOLDERS/FILES.
9. Open a terminal for your device. Mterm or SSH works. Run:
$ su
$ alpine (if asked for passcode)
$ ldrestart
10. Done.

========PART II: INSTALLING APPS========

11. Go to http://ios-repo-updates.com
12. Search Appsync Unified, then download the latest available .deb file.

FOR IOS 7:
"You don't have to edit anything in Appsync package,
just install the latest version of Appsync Unified. [...]"
(italic text taken from Reddit)

NOT IOS 7:
13. Change the name from .deb to .zip and extract it
14. Find the control file and change the firmware to 30
15. Rezip the folder and rename to .deb
16. Install it via Filza or iFile

17. Copy everything from /AppleInternal/Applications in your dump to /Applications/ on device

FOR IOS 7:
"[...] Also, after copying over all the internal apps,
make sure to open terminal on the iPhone, cd to /Applications/ and run "chown 755 ." (without quotes, include period), otherwise all internal apps would
crash with exit code 13." After running chown, run uicache and reboot.
(italic text taken from Reddit)

18. Run these commands via SSH or MTerminal:
$ su
$ alpine (if needs password)
$ ldrestart (wait for respring)
$ uicache
19. Reboot.
20. Done. Some apps might not launch on some versions of iOS.

CREDIT: @angelXwind (twitter) for appsync, @ThermalDOE (twitter) for parts of method, @itstrant (twitter) for most writing, and /u/Andreyhg (Reddit) for iOS 7 app instructions.
```

#### [How to](https://archive.org/details/videoplayback_20240310_2212) install InternalUI on MacOS // [credit](https://twitter.com/timi2506/status/1762188612513198157)
For the video above, [download](https://www.icloud.com/shortcuts/7469466c176445f3ab36e4c8ba87ab65) the shortcut on your iPhone or iPad.


[Sw1tchBoard/Demo Firmwares](https://archive.org/download/appintfirmwar3s)

InternalUI Dumps:  
- iPhone 4S: [9A2306f, iOS 5.0](https://iarchive.app/Download/9A2306f.zpaq)
- iPhone 5: [11A465, iOS 7.0](https://iarchive.app/Download/11A465.dmg)
- iPhone 6S Plus: [15C50, iOS 11.0.2](https://iarchive.app/Download/15C50.zpaq)
- iPhone 8: [17A508, iOS 13.0](https://iarchive.app/Download/17A508.tar.gz)
- iPhone X: [16C49, iOS 12.1.1](https://iarchive.app/Download/16C49.tar.gz) / [17A512, iOS 13.0](https://iarchive.app/Download/17A512.tar.gz)
- iPhone XS: [16B92, iOS 12.1](https://iarchive.app/Download/16B92.zpaq)
- iPhone XS Max: [17B45a, iOS 13.2](https://iarchive.app/Download/17B45a.zpa)
- iPhone 11: [18A188, iOS 14.0](https://iarchive.app/Download/18A188.tar.gz)
- iPhone 12 Pro: [18C57, iOS 14.3](https://iarchive.app/Download/18C57.tar.gz)  
- iPad 2: [11B554a, iOS 7.0.4](https://iarchive.app/Download/11B554a.zip)  
- iPod Touch 4: [8B117, iOS 4.1](https://iarchive.app/Download/8B117.zpaq)

NonUI Dumps:
- iPhone 2G: [1A420](https://iarchive.app/Download/1A420.tar.bz2)
- iPhone 3GS: [8A2180g](https://iarchive.app/Download/8A2180g_3GS.ipsw) / [9B3176n](https://iarchive.app/Download/9B3176n_3GS.ipsw)
- iPhone 4: [8A133](https://iarchive.app/Download/8A133.zip) / [8A2180g](https://iarchive.app/Download/8A2180g_4.ipsw) / [9B3176n](https://iarchive.app/Download/9B3176n_4.ipsw)
- iPhone 4S: [9A2264r](https://iarchive.app/Download/9A2264r.zpaq) / [10A23941a](https://iarchive.app/Download/10A23941a.zpaq)
- iPhone 5: [10A23110z](https://iarchive.app/Download/10A23110z.tar.gz) / [10A316](https://iarchive.app/Download/10A316.zpaq)
- iPhone 5C: [11A63840h](https://iarchive.app/Download/11A63840h.dmg) / [11A93840l](https://iarchive.app/Download/11A93840l.zpaq) / [11D31620l](https://iarchive.app/Download/11D31620l.dmg) / [11D31620u](https://iarchive.app/Download/11D31620u.zpaq)
- iPhone 5S: [11A24580o](https://iarchive.app/Download/11A24580o.zip) / [11A24581c](https://iarchive.app/Download/11A24581c.zpaq)
- iPhone 6: [12A93311h](https://iarchive.app/Download/12A93311h.zip) / [12A93650o](https://iarchive.app/Download/12A93650o.zip) / [12A93651a](https://iarchive.app/Download/12A93651a.zpaq)
- iPhone 6S: [13A93051l](https://iarchive.app/Download/13A93051l.zip)
- iPhone 7: [14A93012r](https://iarchive.app/Download/14A93012r.zpaq) / [14Z1062](https://iarchive.app/Download/14Z1062.zip)
- iPhone 8: [15A93720r](https://iarchive.app/Download/15A93720r.zpaq) / [15A93261h](https://iarchive.app/Download/15A93261h.tgz)
- iPhone 8 Plus: [15A23061c](https://iarchive.app/Download/15A23061c.tar.gz)
- iPhone X: [15A783601y](https://iarchive.app/Download/15A783601y.zip)
- iPhone XR: [16A13580x](https://iarchive.app/Download/16A13580x.tar.xz) / [16A13580z](https://iarchive.app/Download/16A13580z.zpaq) / [16A13581a](https://iarchive.app/Download/16A13581a.zpaq)
- iPad 2: [8F3191d](https://iarchive.app/Download/8F3191d.dmg)
- iPad 5: [14E61810k](https://iarchive.app/Download/14E61810k.tar.gz) / [14F60900l](https://iarchive.app/Download/14F60900l.zpaq)
- iPad 6: [15E61120i](https://iarchive.app/Download/15E61120i.tar.gz)
- iPad Mini 1: [10A63971b](https://iarchive.app/Download/10A63971b.dmg)
- iPod Touch 6: [12H10570d](https://iarchive.app/Download/12H10570d.tar.xz)
- Watch Series 1: [14S32871w](https://iarchive.app/Download/14S32871w.dmg)
- T2 Security Chip: [16P25070u](https://iarchive.app/Download/16P25070u.zpaq)

Internal OTA Updates (credits to [@Endermanch](https://www.youtube.com/@Endermanch)):
- [iPhone 5S, iOS 7](http://appldnld.apple.com/iOS7/031-3154.20140204.D0c34/com_apple_MobileAsset_SoftwareUpdate/4f43251820ad962540755d270efc2fa2ec6bf1b0.zip)
- [iPhone 4S, iOS 7](http://appldnld.apple.com/iOS7/031-3154.20140204.D0c34/com_apple_MobileAsset_SoftwareUpdate/7f76d243a8371570b999e51b68186679c6294dc0.zip)
- [iPhone 5C, iOS 7](http://appldnld.apple.com/iOS7/031-3154.20140204.D0c34/com_apple_MobileAsset_SoftwareUpdate/4f43251820ad962540755d270efc2fa2ec6bf1b0.zip)

***

#### Applications:  

It takes a long time to look for these so you don't have to, a follow would be appreciated :)

MOST APPS HERE are for AppleConnect, which are used (or were once used) by Apple employees to communicate and use in a business environment. Some apps here are for prototype purposes (*Also goes by InternalUI*) or DemoUnit apps (*installed on demo devices which are displayed in the Apple Store*), but most are for the communication among Apple Employees and are for business. For actual InternalUI apps, check up above for the tutorial "how to install InternalUI firmware".

(`Unknown` versions aren't unknown- there are either too many to look through or I do not have enough time to manually add each and every iOS version.)

##### x32 apps (IPAs)  
###### Some links here might have x64 apps in their archives, but around 90% of the apps in this section are 32-bit for iOS 6.
- [Apple Internal Apps `6-10`](https://archive.org/download/troubleshoot-plan-genius-v-1.0)
- [listing of Apple_internal.zip, `6-10`](https://ia601203.us.archive.org/view_archive.php?archive=/7/items/apple-internal/Apple_internal.zip)
- [listing of AppleInternal.rar, `6-10`](https://ia800502.us.archive.org/view_archive.php?archive=/11/items/Apple-Internal-IPAs/AppleInternal.rar)
- [32-bit AppleInternal Apps, `6-10`](https://ia902607.us.archive.org/view_archive.php?archive=/12/items/i-os-apps-20230603-t-195539-z-001/iOS%20Apps-20230603T195539Z-001.zip)
- [Google Drive Backup Backups `unknown`](https://archive.org/details/i-os-apps-20240227-t-053954-z-001)
- [Some prototype app dumps , `6`](https://github.com/cc7623/AppleIntApps/releases/tag/v1.0)
- [My own upload (github, iOS `6`)](https://github.com/cc7623/AppleIntApps/releases/tag/v2.0)
- [My own upload (archive.org, iOS `6`)](https://archive.org/details/apple-internal-collection-reupload)

##### x64 apps (IPAs)
- [DemoUnit, ACS, and NetworkCheck IPA, `unknown version`](https://archive.org/download/demo-unit-v-2.3-5496-prod)
- [iPad DemoApps, `16.4.1`](https://web.archive.org/web/20230815000000*/https://cdn.thanos.lol/demoapps.zip)
- [iosdmpkgs, `14.5`](https://archive.org/download/iosdmpkgs)
- [iPhone 6s dump, `9.2.1`](https://archive.org/details/imovie_202401)
- [DemoUnit dumps; (version of IPA in alphabetical order) `17.0`, `unknown`, `15.2`](https://archive.org/download/appledemounit)
- [Meet iPhone/iPad(4.4.0.8), Face ID Demo(2.0.0), DemoLoop(5.6.1) `unknown version(s)`](https://archive.org/details/ipa_20240226)
- [FaceID Demo `unknown app ver./iOS ver.`](https://web.archive.org/web/20221130114944/https://cdn.discordapp.com/attachments/928854715603746886/1047315894906400909/pearlstoredemo.ipa)
- [TouchID Demo 3.2.0 `unknown version`](https://archive.org/details/com.apple.MesaStoreDemo)
- [Unknown_Tag's Archive (original, mega.nz) `multiple versions`](https://mega.nz/folder/RIwwhYiL#gBtcgj5jfhJFuxO9bv4L2A)
- [Unknown_Tag's Archive (reuploaded, archive.org) `multiple versions`](https://archive.org/download/unknown-tags-archive)
- [Internal .app dumps `14.0`](https://archive.org/details/apple-internal-app-dumps)

##### App Store Links, x64 [credit](https://web.archive.org/web/20240212231956/https://old.reddit.com/r/Apple_Internal/comments/1ao7u00/the_apple_internal_apps_ive_got_installed/)
- [SEED `16.0`](https://apps.apple.com/us/app/seed/id6449049254)
- [Reality Composer `17.0`](https://apps.apple.com/us/app/reality-composer/id1462358802)
- [Business Essentials `15.0`](https://apps.apple.com/us/app/apple-business-essentials/id1588151344)
- [Apple Research `15.0`](https://apps.apple.com/us/app/apple-research/id1463884356)
- [Platoon for Artists `13.0`](https://apps.apple.com/us/app/platoon-for-artists/id1550671751)
- [Apple Music for Artists `16.0`](https://apps.apple.com/us/app/apple-music-for-artists/id1366467972)
- [App Store Connect `15.0`](https://apps.apple.com/us/app/app-store-connect/id1234793120)
- [Apple Developer `16.0`](https://apps.apple.com/us/app/apple-developer/id640199958)
- [Testflight `14.0`](https://apps.apple.com/us/app/testflight/id899247664)
- [JAMF Self-Service `15.0`](https://apps.apple.com/us/app/jamf-self-service/id718509958)
- [Configurator `16.0`](https://apps.apple.com/us/app/apple-configurator/id1588794674)
- [Indoor Survey `15.5`](https://apps.apple.com/us/app/indoor-survey/id994269367)
- [Classroom `14.5`](https://apps.apple.com/us/app/classroom/id1085319084)
- [Siri Speech Study `14.0`](https://apps.apple.com/us/app/siri-speech-study/id1564003829)
- [Find My Certification Asst. `16.0`](https://apps.apple.com/us/app/find-my-certification-asst/id1532296125)
- [Car Keys Test `16.1`](https://apps.apple.com/us/app/car-keys-tests/id1635860023)
- [MagSafe Certification Asst. `15.0`](https://apps.apple.com/us/app/magsafe-certification-asst/id1533467908)
- [Accessory Developer Assistant `16.1`](https://apps.apple.com/us/app/accessory-developer-assistant/id1635862694)
- [GymKit Certification Assistant `16.1`](https://apps.apple.com/de/app/gymkit-certification-assistant/id1537439501)
- [Apple Health Studies `16.0`](https://apps.apple.com/us/app/apple-health-studies/id1666409057)
- [DemoUnit `IPA, 17.0`](https://demounit.apple.com/views/com.apple.ist.DemoUnit-iOS/download)
- [DemoUnit ACS `IPA, 17.0`](https://demounit.apple.com/views/com.apple.ist.acs/download)
- [DemoUnit Network Check `IPA, 16.1`](https://demounit.apple.com/views/com.apple.ist.networkcheck/download)

##### Shortcuts [credit for most of them from @Unknown_Tags](https://twitter.com/Unknown_tags), more shortcuts from him are [here](https://unknownarchive.univer.se/shortcuts)
- [iCrowd App Installation `iOS <16.0`](https://www.icloud.com/shortcuts/721d2c6b605f4f2ebfc9e14a82edb3ca)
- [Magic Portal V.4 `iOS unknown version`](https://www.icloud.com/shortcuts/88676e38eb24464bbe978ef85292a7e8)
- [MyMessage Installation `iOS x64, unknown version`](https://www.icloud.com/shortcuts/719da519c3c6484ca8ba1641adfc6bb9)
- [Internal Downloads `iOS unknown version`](https://www.icloud.com/shortcuts/c389265109794743bbfd85acf135c9e1)
- [Xcode Previews App, can't be turned off `iOS non-legacy (>10)`](https://unknownarchive.netlify.app/page11#:~:text=Xcode%20Previews%20Application%20Shortcut%C2%A0)
- [Setup AppleInternal Folders on Mac `macOS, unknown version`](https://www.icloud.com/shortcuts/0d1146fc06db4cb4b7781e1526a4edbc), from [@timi2506](https://twitter.com/timi2506)

##### macOS Apps
- [https://archive.org/download/macOSInternalApplications `unknown version`](https://archive.org/download/macOSInternalApplications)
- [Reupload (from above)](https://github.com/cc7623/AppleIntApps/releases/tag/3.0) (taken from 40gb appleinternal dump)
- [Random MacOS DemoApp `unknown version`](https://archive.org/details/macdoesthat)
- [Pricing v2.1.4 `unknown version`](https://archive.org/download/com.apple.ist.windward-mac)
- [Angry Birds Retail Demo `MacOSX12.3`](https://archive.org/download/com.rovio.abreloaded.retaildemo)
- [Some MacOS DemoUnit apps `unknown version`](https://archive.org/download/appledemounit)
- [PurpleRestore 3 `unknown version`](https://archive.org/details/PurpleRestore_3)
- [Diagnosic Resources `unknown version(s)`](https://archive.org/download/diagnostic-resources)
- [Enterprise Connect 2.0.2 `unknown version`](https://archive.org/download/enterprise-connect-2.0.2)
- [PurplePRO_0.1.1b1 `unknown version`](https://mega.nz/file/yUIQTRqB#M9FYAJ-8vPgfw4wTet6gDoOHBNql78akskWPTKz4kDk)

***

#### DemoLoops:

[A Few DemoLoop Videos](https://archive.org/details/iphone_portrait_202402)

[AppleTV, Enroll](https://www.idownloadblog.com/2016/01/18/apple-tv-store-demo-mode/#:~:text=How%20to%20get%20into%20retail%20Demo%20Mode%20on%20Apple%20TV)

[Mac Tutorial, No Enroll](https://archive.org/details/no-enroll-mac-os-demoloop-apple-store-screen-saver-tutorial) (to view files used in video, scroll down & click `SHOW ALL`. `xmlfile.xml` is from the pastebin link shown in the video. export & rename to `ScreenSaver.plist`. you will have to find the demoloop video by yourself for now. making a quick list of existing demoloop videos and uploading it soon.)  

[Mac Tutorial, Enroll](https://archive.org/details/audioless-mac-os-dcota-demounit-tutorial)

[iOS Tutorial, Enroll](https://www.theiphonewiki.com/wiki/Screen_Saver#:~:text=Installation%20Link%3A%0Ahttps%3A//demoupdate.apple.com/index.html) *ONLY WORKS ON DEVICES WHICH APPLE CURRENTLY SELLS NEW OR REFURBISHED.*

[iOS Tutorial, No Enroll, Non-Jailbroken `14.0 - 16.1.2`](https://github.com/swifticul/StoreControl)
1. Download the [StoreControl](https://github.com/swifticul/StoreControl/releases/latest) IPA.
2. Download the mobileprovision profile from [here](https://web.archive.org/web/20240304053546/https://raw.githubusercontent.com/swifticul/StoreControl/main/Downloads/Profiles/profile.mobileprovision).
3. Download [AppleConfigurator2](https://apps.apple.com/us/app/apple-configurator/id1037126344?mt=12) for MacOS or [iMazing](https://downloads.imazing.com/windows/iMazing/iMazing2forWindows.exe) for Windows.
4. AppleConfigurator:
  - Connect iOS device to your Mac
  - Once you see the device pop up, drag and drop the mobileprovision file onto the image of your device.
  - Restart your iOS device.
5. iMazing:
  - Connect iOS device to your Mac
  - Once you see the device pop up, drag and drop the mobileprovision file onto the image of your device. If prompted, select the Settings icon with the name "Profiles" as the target.
  - Restart your iOS device.
6. Go to [https://demoupdate.apple.com/](https://demoupdate.apple.com/) to install DemoLoop.


[iOS Tutorial, No Enroll, Requires Jailbreak (x64 devices *only*)](https://web.archive.org/web/20240224055252/https://old.reddit.com/r/Apple_Internal/comments/14bzt93/demoloop/?rdt=43013) Steph's twitter tutorial is down below:

DemoLoops for iOS <=16.1.2 [credit to Steph63163](https://twitter.com/Steph63163/status/1627215122308497408):
- Alright, here's how to get DemoLoop for iOS 16-16.1.2.  First install this profile using [Apple Configurator](https://ia800200.us.archive.org/view_archive.php?archive=/31/items/apple-partner-demo-june-2024v-1.mobileprovision_202402/Apple%20Partner%20Demo%20June%202024v1.mobileprovision.zip).
- Then install the DemoLoop application on the following site: https://demoupdate.apple.com/index.html
- Once acquired, using AltStore or other, install FilzaEscaped16.
- After that, when Filza is installed, get this [ApplicationSupport](https://archive.org/details/application-support_202402) folder, unzip it and add it instead of the existing one in the following directory: `/Var/mobile/Containers/Data/Application/com.Apple.ist.DemoLoop/Library`

***

#### Links [credit](https://www.reddit.com/media?url=https%3A%2F%2Fpreview.redd.it%2Fb4tobsdpu1cc1.jpg%3Fwidth%3D1179%26format%3Dpjpg%26auto%3Dwebp%26s%3Dad181109c5a79bb7fc3cae8ea8c76824ae170930):

- [https://chirp.apple.com](https://chirp.apple.com)
- [https://esign.apple.com](https://esign.apple.com)
- [https://asw.apple.com](https://asw.apple.com)
- [https://appleweb.apple.com](https://appleweb.apple.com)
- [https://mfi.apple.com](https://mfi.apple.com)
- [https://sb.apple.com](https://sb.apple.com)
- [https://baseline.apple.com](https://baseline.apple.com)
- [https://plec.apple.com](https://plec.apple.com)
- [https://unibox.apple.com](https://unibox.apple.com)
- [https://idmsa.apple.com](https://idmsa.apple.com)
- [https://onepulse.apple.com](https://onepulse.apple.com)
- [https://hrweb.apple.com](https://hrweb.apple.com)
- [https://people.apple.com](https://people.apple.com)
- [https://demounit.apple.com](https://demounit.apple.com)
- [https://mymessage.apple.com](https://mymessage.apple.com)
- [https://manage.apple.com](https://manage.apple.com)
- [https://ahflex.apple.com](https://ahflex.apple.com)
- [https://partner-relay-uat.apple.com](https://partner-relay-uat.apple.com)
- [https://afsweb-msc.apple.com](https://afsweb-msc.apple.com)
- [https://iwork.ai](https://iwork.ai) / [article](https://appleinsider.com/articles/24/02/12/apple-buys-domain-suggesting-generative-ai-additions-may-come-to-iwork)
- [https://iwork.com](http://iwork.com/) / [article](https://appleinsider.com/articles/09/01/06/apple_introduces_iwork_09_iwork_com)
- [meet://](meet://)
- [tap-to-radar://new](tap-to-radar://new)
