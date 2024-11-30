# EaseLife

---

## Android
    1) App name - 
    2) Package name - 
    3) Short Desc (80 character)
    4) Long desc (4000 words)
    5) App icon(512*512px, 1024*500px)
    6) Phone Screenshot (Upload 2-8 phone screenshots. Screenshots must be PNG or JPEG, up to 8 MB each, 16:9 or 9:16 aspect ratio, with each side between 320 px and 3,840 px) Tab(1080*1920) and mobile(720*1600)
    7) Email
    8) Mobile Number
    9) privacy policy url
    10) App Category 
    11) login details for play store testing
    12. Account deletion url
    13. Feature like (upload Photo/video, Webview, location, file upload, financial) etc

## Android close testing details

    **How did you recruit users for your closed test**
    Friends and family members helped me to test my app.
          
    **How easy was it to recruit testers for your app?**
    Easy
          
    **Describe the engagement  you received from testers**
    Most of my testers have tested all the features.
          
    **Provide a summary of the feedback that you received**
    I have collected the feedback through the play store section.Most of my testers were happy to have the app on their devices.
          
    **Who is the intended audience of your app?**
    Anybody who wants to translate the text or speech or images to their telugi language or vice versa.
          
    **Describe how your app provides value to users.**
    My app is a useful app for the end users. It is free and easy to use.
          
    **How many installs in first years**
    10k-100k
          
    **What changes did you make to your app bases on what you learned during closed testing?**
    Fixed UI issues for the battery saver mode on.
          
    **How did you decide that your app is ready for prod?**
    All the features were tested throughly. No issues found or crashed are found on closed testing.
      
---

## Flutter iOS

    **iOS Account Creation**
    Name
    DOB
    Gmail
    Mobile number
    UPI
    Address 
         
    **Upload iOS IPA**
        
    For 6.7’’ Screenshots(1290*2796) 4-10
    For 5.5’’ Screenshots(1242*2208) 4-10
    For 13’’ Screenshots(2048*2732) 4-10
    For 12.9’’ Screenshots(2048*2732) 4-10
        
    170 character description
    4000 long description
    Keyword
    Support url
    Logo 1800*1200
    Contact info (name, number, email)
    AppStore Credential for testing
    Privacy Policy url

        

### Basic Install Process
Remove ios folder then reinstall after completion project **flutter create -i swift --platforms ios .**

    Pod install (zsh: command not found: pod)
    sudo gem install cocoapods
    sudo gem install activesupport -v 6.1.7.7
    ruby -v
    gem -v
    gem update --system
    
    pod install(In iOS Folder)
    pod clean 
    pod install
    pod update

In iOS folder Pod file not present then 

    Pod init
    Pod install

    export PATH=“$PATH:/Users/mac/Desktop/flutter/bin
    export PATH=“$PATH:/Users/deepak.sharma/flutter/bin
    flutter build ios
    
If it's fail then provide full access from setting to Xcode app terminal app

    /bin/sh "$FLUTTER_ROOT/packages/flutter_tools/bin/xcode_backend.sh" build provide in runner >build phases >run script
    
    flutterfire configure  recreate iOS folder 
    flutter create -i swift --platforms ios .
    
    flutter build ios
    flutter build apk
    flutter build web --release
    //for local version
    flutter run --release 
    flutterfire configure

**Flutter Migration process**

    https://dart.dev/resources/dart-3-migration

**For g.dart  **

    flutter pub run build_runner build

### Permission In Info.plist (runner -> Info.Plist)


**Location add in info.plist**

  	<key>NSLocationAlwaysAndWhenInUseUsageDescription</key>
  	<string>This app uses your location to offer location specific deals. It&apos;s completely private and secure.</string>
  	<key>NSLocationAlwaysUsageDescription</key>
  	<string>This app uses your location to offer location specific deals. It&apos;s completely private and secure.</string>
  	<key>NSLocationUsageDescription</key>
  	<string>This app uses your location to offer location specific deals. It&apos;s completely private and secure.</string>
  	<key>NSLocationWhenInUseUsageDescription</key>
  	<string>This app uses your location to offer location specific deals. It&apos;s completely private and secure.</string>

**Camera**

    <key>NSCameraUsageDescription</key>
    <string>This app uses Camera to customize their profile picture. This information is not shared anywhere.</string>

**Photos**

    <key>NSMicrophoneUsageDescription</key>
    <string>This app require permission to access microphone</string>
  	<key>NSPhotoLibraryAddUsageDescription</key>
  	<string>This app uses Camera to customize their profile picture. This information is not shared anywhere</string>
  	<key>NSPhotoLibraryUsageDescription</key>
  	<string>This app uses Camera to customize their profile picture. This information is not shared anywhere</string>


### Update Pod File (In Bottom)

        
    post_install do |installer|
      installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
              config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] ||= [
                '$(inherited)',
    
                ## dart: PermissionGroup.camera
                'PERMISSION_CAMERA=1',
    
                ## dart: PermissionGroup.photos
                'PERMISSION_PHOTOS=1',
    
                ## dart: [PermissionGroup.location, PermissionGroup.locationAlways, PermissionGroup.locationWhenInUse]
                'PERMISSION_LOCATION=1',
    
                ## dart: PermissionGroup.contacts
                'PERMISSION_CONTACTS=1',
    
                ## dart: PermissionGroup.microphone
                'PERMISSION_MICROPHONE=1',
    
                ## dart: PermissionGroup.notification
                'PERMISSION_NOTIFICATIONS=1',
    
                ## dart: PermissionGroup.mediaLibrary
                'PERMISSION_MEDIA_LIBRARY=1',
    
                ## dart: PermissionGroup.bluetooth
                'PERMISSION_BLUETOOTH=1',
    
                ]
            end
            flutter_additional_ios_build_settings(target)
      end
    end

### Certificate Generate

   * [iOS Profile and Certificate Generate](https://www.youtube.com/watch?v=wSt8VSwwuIs)

    Open https://developer.apple.com/account/resources/profiles/add
    And open profile -> generate profile -> App Store Connect Disruption -> Select Apple ID -> create certificate - > Apple Disruption -> Upload a Certificate Signing Request (CSR) 
    Open keychain-> click on top left -> keychain certificate -> certificate assistance -> Request a certificate from a certificate authority click -> type gmail and save to disk continue.
    Then upload save disk file on CSR website -> and download profile certificate.
    If provisioning certificate is not download then again go to profile and generate with name EzeerideProvisioningProfile

---

### iOS Icon Generator (Drag & Drop runner -> Assets)

[App Icon](https://www.appicon.co/)

### Developer Account 
[Apple Developer Account](https://developer.apple.com/account)

[Apple Support](https://getsupport.apple.com/products)


## Other Assets

### UI Design Library

   * [Awesome UI Design](https://github.com/thanhtoan1196/awesome-android-ui)
   * [Awesome Android](https://github.com/vimalcvs/Awesome-Android-UI#UI)
   * [Awesome UI](https://github.com/XPGSnail/awesome-android-ui)

### Coding library

   * [Awesome Code](https://github.com/JStumpp/awesome-android)


### Image Resources

   * [icons8](https://icons8.com/illustrations)
   * [undraw](https://undraw.co/illustrations)

### Convert Video into GIF
 
  * [Video to GIF](https://www.onlineconverter.com/video-to-gif)
  * [Video to GIF](https://hnet.com/video-to-gif)
  * [Tinypng Compress Image](https://tinypng.com/)
  * [Resize Image](https://resizeimage.net/)
  * [Logo Creator](https://www.freelogoservices.com/)
  * [App Logo](https://app.logo.com/editor/preview?editing_logo=logo_8ac6ce10-7d5c-41f1-8843-c54e08548d19&logo=logo_8ac6ce10-7d5c-41f1-8843-c54e08548d19)
  * [Png Image Crop](https://onlinepngtools.com/crop-png)
  * [Image Create For PlayStore](https://www.appstorescreenshot.com/)
  * [Merge Image Horizontally](https://www.filesmerge.com/merge-images)
  * [Fake Mail](https://www.mailinator.com/)
  * [Fake Mail](https://yopmail.com/en/wm)
  * [Fake OTP](http://receivefreesms.com/)
  * [Fake OTP](https://www.freeonlinephone.org/)
  * [Fake OTP and mail](Use Telegram Channel)
  * [Apk upload and link](https://www.diawi.com/)
  * [Ads Mob](https://admob.google.com/home/)
  * [For Ads](https://www.app-ads-txt.com/appadstxt/edit)
  * [Mock Location](https://play.google.com/store/apps/details?id=ru.gavrikov.mocklocations&hl=en_IN&gl=US)
  * [SHA KEY Steps](https://stackoverflow.com/questions/27609442/how-to-get-the-sha-1-fingerprint-certificate-in-android-studio-for-debug-mode)
    
         1) Click on the gradle. Top right on the Android Studio. As you can see in this picture.
         2) Now click on icon as seen in below picture. A new searchable windows/screen will open.
         3) Now type,gradle signingreport and press Enter to start generating SHA KEY as seen in below.
         4) Your SHA Key will generate as seen in this picture. Using these steps you can generate SHA KEY in Android Studio 4.2.
    

## Beautiful UI design

  * [UI](https://github.com/lohanidamodar/flutter_ui_challenges)
  * [Awesome Flutter UI](https://github.com/basarozcan/awesome-flutter)
  * [Flutter Design](https://github.com/Solido/awesome-flutter)
  * [Design](https://github.com/avirias/awesome-flutter)
  * [Flutter UI](https://github.com/avirias/flutter_ui_challenges)
  * [UI Kit](https://github.com/avirias/Flutter-UI-Kit)
  * [Flutter packages](https://github.com/leisim/awesome-flutter-packages)
  * [UI Templates](https://github.com/mitesh77/Best-Flutter-UI-Templates)
  * [UI Design Page](https://github.com/basarozcan/awesome-flutter)
  * [UI Design Pages](https://github.com/kalismeras61/flutter_awesome_design_pages)
  * [Flutter Apps](https://github.com/pacifio/flutter_apps)



## Free Software for android and mac and windows
  * [Free Software](https://filecr.com/en/?id=666012000000)
  * [DiskGenius For Partition](https://filecr.com/windows/diskgenius/)


