# android-sdk-commandline-installation
```
https://linuxopsys.com/topics/install-android-sdk-without-android-studio-on-ubuntu
```

### error
```
 Failed to install the following Android SDK packages as some licences have not been accepted.
     platforms;android-33 Android SDK Platform 33
     build-tools;30.0.3 Android SDK Build-Tools 30.0.3
     platform-tools Android SDK Platform-Tools
     tools Android SDK Tools
     emulator Android Emulator
  To build this project, accept the SDK license agreements and install the missing components using the Android Studio SDK Manager.
  Alternatively, to transfer the license agreements from one workstation to another, see http://d.android.com/r/studio-ui/export-licenses.html
  
  Using Android SDK: /home/jenkins/android/sdk
```
sol:
```
cd /home/jenkins/android/sdk/tools/bin
./sdkmanager --licenses
```
