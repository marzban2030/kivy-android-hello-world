# kivy-android-hello-world

Developing Android code is harder than Java code, Java code is harder than C++ code. The easiest code to developing is Python code, Build your Android APK application from Python kivy framework with few codes and steps by following instructions in this repository. No system and IDE is needed.

# Build APK in Google Colab

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
