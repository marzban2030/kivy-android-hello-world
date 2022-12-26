# kivy-android-hello-world

Developing Android code is harder than Java code, Java code is harder than C++ code. The easiest code to developing is Python code, Build your Android APK application from Python kivy framework with few codes and steps by following instructions in this repository. Common way to building APK file from Kotlin and Java codes is Android Studio IDE however buildozer do this (on Python codes) like as gradle in command line, Android SDK and NDK will be used here by buildozer to building APK. No system and IDE is needed here however there is need to a system with strong hardwares.

# Build

You can Change Android API and Minimum Android NDK API version numbers in "buildozer.spec" file optionally. In this case android API version number should be set to highest available Android API version number from Google and Android NDK API version number must be set to latest Google supported Android NDK API version number, Pay attention that Python-for-Android (p4a) recommend you to use supported Android NDK API version certainly during build process and will be encouraged with an error if Android NDK API version number has not been set to recommended supported version.

Run below commands in Colab:
```
!sudo apt update
!sudo apt install -y git zip unzip build-essential openjdk-8-jdk python3-pip autoconf libtool pkg-config zlib1g-dev libncurses5-dev libncursesw5-dev libtinfo5 cmake libffi-dev libssl-dev libltdl-dev lld
!pip install --upgrade Cython==0.29.19 virtualenv
!git clone https://github.com/marzban2030/kivy-android-hello-world
!pip install --upgrade buildozer kivy
!cd kivy-android-hello-world && yes | buildozer -v android debug
```

Finally run:
```
from google.colab import files
files.download('path_to_APK')
```

The path to APK was "/content/kivy-android-hello-world/bin/hello-0.0.1-arm64-v8a-debug.apk" for me, Maybe it is different for you.

# Learn more

It's long task to building APK from Python and in most cases doesn't work properly:

Cython cythonize python codes to C++ codes!

buildozer with Android NDK (Native Development Kit) translate C++ codes to Kotlin and Java codes!

gradle with Android SDK build APK from Kotlin and Java codes!

Around 1GB packages with about 6GB installation size in a system with AMD RYZEN CPU and 12GB ram will be used to building a 14MB APK file from 8 lines of a Python code with 200 Bytes size during 30 minutes to showing a simple "Hello, World!" text in an Android device at moment.

Anyway, Building APK file from Kivy Python has some limits and in most cases doesn't work properly, I recommend you that use Android Studio IDE with Kotlin and Java codes to building APK file.
