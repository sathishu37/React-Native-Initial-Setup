# React Native Setup - Linux
React Native combines the best parts of native development with React, a best-in-class JavaScript library for building user interfaces.

## Installing dependencies

* Node
* JDK
* Android development environment

## Node
React Native requires Node 14 or a newer version to be compatible.

```sh
# You can install any of these versions just by replacing version number (14, 16, 18)
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs
```

## JDK
React Native requires at least the version 8 of the Java SE Development Kit (JDK).

```sh
# You can install any of these versions just by replacing version number (8, 11)
sudo apt-get install openjdk-11-jdk

# To check the java version type the below command in your terminal.
javac -version
```

## Android development environment
Setting up your development environment can be somewhat tedious if you're new to Android development. If you're already familiar with Android development, there are a few things you may need to configure. In either case, please make sure to carefully follow the next few steps.

**1. Install Android Studio**

[Download and install Android Studio.](https://developer.android.com/studio/index.html) While on Android Studio installation wizard, make sure the boxes next to all of the following items are checked:

* Android SDK
* Android SDK Platform
* Android Virtual Device

Then, click "Next" to install all of these components.

**2. Install the Android SDK**

Android Studio installs the latest Android SDK by default. Building a React Native app with native code, however, requires the Android 12 (S) SDK in particular. Additional Android SDKs can be installed through the SDK Manager in Android Studio.

To do that, open Android Studio, click on "Configure" button and select "SDK Manager".
> The SDK Manager can also be found within the Android Studio "Preferences" dialog, under **Appearance & Behavior → System Settings → Android SDK.**

**3. Configure the ANDROID_SDK_ROOT environment variable**

The React Native tools require some environment variables to be set up in order to build apps with native code.

Add the following lines to your $HOME/.bash_profile or $HOME/.bashrc (if you are using zsh then ~/.zprofile or ~/.zshrc) config file:

```
export ANDROID_SDK_ROOT=$HOME/Library/Android/Sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
```
> Please make sure you use the correct Android SDK path. You can find the actual location of the SDK in the Android Studio "Preferences" dialog, under **Appearance & Behavior → System Settings → Android SDK.**



