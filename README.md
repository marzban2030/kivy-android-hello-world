# kivy-android-hello-world

Developing Android code is harder than Java code, Java code is harder than C++ code. The easiest code to developing is Python code, Build your Android APK application from Python kivy framework with few codes and steps by following instructions in this repository. Common way to building APK file from Kotlin and Java codes is Android Studio IDE however buildozer do this (on Python codes) like as gradle in command line, Android SDK and NDK will be used here by buildozer to building APK. No system and IDE is needed here however there is need to a system with strong hardwares.

# Build APK in Google Colab

Firstly, Change Android API and Minimum Android NDK API version numbers in "buildozer.spec" file. Android API version number should be set to highest available Android API version number from Google and Android NDK API version number must be set to latest Google supported Android NDK API version number, Pay attention that Python-for-Android (p4a) recommend you to use supported Android NDK API version certainly during build and encouraged with an error if Android NDK API version number has not been set to recommended supported version.

Run below commands in Google Colab:
```
!sudo apt update
!sudo apt install -y git zip unzip build-essential openjdk-8-jdk python3-pip autoconf libtool pkg-config zlib1g-dev libncurses5-dev libncursesw5-dev libtinfo5 cmake libffi-dev libssl-dev libltdl-dev lld
!pip install --upgrade Cython==0.29.19 virtualenv
!git clone https://github.com/marzban2030/kivy-android-hello-world
!pip install --upgrade buildozer kivy colab-xterm
%load_ext colabxterm
```

Then run:
```
%xterm
```

Then run below commands in loaded X-terminal:
```
cd kivy-android-hello-world
buildozer -v android debug
```

Finally after several minutes, To downloading built-in APK file run below command in Google Colab:
```
from google.colab import files
files.download('path_to_APK')
```

The path to APK was "/content/kivy-android-hello-world/bin/hello-0.0.1-arm64-v8a-debug.apk" for me, Maybe it is different for you.

Note: Avoid to license and copyright issues, The built-in APK file is not released here.

![Image1](https://github.com/marzban2030/kivy-android-hello-world/raw/master/Screenshot.jpg)

# Learn more

It's long task to building APK from Python:

Cython cythonize python codes to C++ codes!

buildozer with Android NDK (Native Development Kit) translate C++ codes to Kotlin and Java codes!

gradle with Android SDK build APK from Kotlin and Java codes!

Around 1GB packages with about 6GB installation size in a system with AMD RYZEN CPU and 12GB ram will be used to building a 14MB APK file from 8 lines of a Python code with 200 Bytes size during 30 minutes to showing a simple "Hello, World!" text in an Android device at moment.

Anyway, Building APK file from Kivy Python has some limits and in most cases doesn't work, I recommend you that use Android Studio IDE with Kotlin and Java codes to building APK file.
