# kivy-android-hello-world

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
