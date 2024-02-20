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
commands i run
```
   74  mkdir -p ~/android/sdk
   75  ls
   76  cd android/
   77  cd sdk/
   78  ls
   79  sudo wget https://dl.google.com/android/repository/commandlinetools-linux-9123335_latest.zip
   80  sudo unzip commandlinetools-linux-9123335_latest.zip
   81  cd cmdline-tools
   82  ls
   83  mkdir tools
   84  sudo mkdir tools
   85  mv -i * tools
   86  ls
   87  ls tools/
   88  sudo mv -i * tools
   89  ls tools/
   90  export ANDROID_HOME=$HOME/android/sdk
   91  export PATH=$ANDROID_HOME/cmdline-tools/tools/bin/:$PATH
   92  export PATH=$ANDROID_HOME/emulator/:$PATH
   93  export PATH=$ANDROID_HOME/platform-tools/:$PATH
   94  sdkmanager --list
   95  sdkmanager --install packages [options]
   96  sdkmanager --install "platform-tools" "build-tools;30.0.1" "emulator" "platforms:android-33"
   97  sdkmanager --list --channel=channel_id // Channels: 0 (stable), 1 (beta), 2 (dev), or 3 (canary)
   98  echo $ANDROID_HOME
   99  ./sdkmanager --licenses
  100  ls
  101  cd tools/
  102  ls
  103  cd bin/
  104  ls
  105  ./sdkmanager --licenses
```
