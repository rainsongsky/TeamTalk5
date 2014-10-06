# TeamTalk 5 SDK

Repository for TeamTalk 5 SDK development.

## Download TeamTalk 5 SDK

To build the TeamTalk client projects you must first download the TeamTalk 5 SDK to obtain the client and server binaries.

* TeamTalk 5 SDK Standard Edition - **Alpha** releases
  * [Windows 32-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3389/tt5sdk_v5.0.0.3389_alpha2_win32.zip) **rev. 3389**
  * [Windows 64-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3389/tt5sdk_v5.0.0.3389_alpha2_win64.zip) **rev. 3389**
  * [Mac 64-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5sdk_v5.0alpha1_macos_amd64.tar.gz)
  * [Debian 7 32-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5sdk_v5.0alpha1_debian7_i386.tar.gz)
  * [Debian 7 64-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5sdk_v5.0alpha1_debian7_amd64.tar.gz)
  * [Raspberry Pi (armhf)](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5sdk_v5.0alpha1_raspbian_armhf.tar.gz)
  * [Android arm-v7](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3387/tt5sdk_v5.0.0.3387_alpha1_android_armv7a.tar.gz) **rev. 3387**
* TeamTalk 5 SDK Professional Edition - **Alpha** releases
  * [Windows 32-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3389/tt5prosdk_v5.0.0.3389_alpha2_win32.zip) **rev. 3389**
  * [Windows 64-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3389/tt5prosdk_v5.0.0.3389_alpha2_win64.zip) **rev. 3389**
  * [Mac 64-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5prosdk_v5.0alpha1_macos_amd64.tar.gz)
  * [Debian 7 32-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5prosdk_v5.0alpha1_debian7_i386.tar.gz)
  * [Debian 7 64-bit](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5prosdk_v5.0alpha1_debian7_amd64.tar.gz)
  * [Raspberry Pi](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/tt5prosdk_v5.0alpha1_raspbian_armhf.tar.gz)

## TeamTalk 5 Libraries
Projects wrapping the client DLL file in the TeamTalk SDK.
* **TeamTalk_DLL**
  * TeamTalk 5 C-API DLL project 
  * C-API header file for TeamTalk 5 DLL
    * Preliminary API [Documentation](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/docs/C-API/)
* **TeamTalk.NET** (dependency: **TeamTalk_DLL**)
  * TeamTalk 5 .NET DLL wrapper for C-API TeamTalk 5 DLL (**TeamTalk_DLL**)
    * Preliminary API [Documentation](http://bearware.dk/test/TeamTalk5SDK/v5.0.0.3331/docs/NET/)
  * Requires DLL file from **TeamTalk_DLL** project, either 32-bit or 64-bit
* **TeamTalkJNI**
  * TeamTalk 5 JNI project with Java wrapper classes
  * Import in Eclipse using [Android SDK](http://developer.android.com/sdk/index.html)
  * Requires ARM-v7a JNI shared object in sub-folder *TeamTalkJNI/libs/armeabi-v7a*
    * Based on Android API Level 16
  * The following features are currently *not* supported in the JNI API:
    * Desktop sharing
    * Video capture (webcam)
    * Media file streaming

## TeamTalk 5 Clients
Projects containing client applications which use the TeamTalk 5 client DLL.
* **qtTeamTalk** (dependency: **TeamTalk_DLL**)
  * TeamTalk 5 client application written in C++ and based on [Qt](http://www.qt-project.org)
  * Requires **TeamTalk_DLL** project for DLL dependency
* **TeamTalkClassic** (dependency: **TeamTalk_DLL**)
  * TeamTalk 5 accessible client application written in C++ and based on MFC
    * Works well with screen-readers
  * Requires **TeamTalk_DLL** project for DLL dependency
* **TeamTalkApp.NET** (dependency: **TeamTalk.NET**)
  * TeamTalk 5 .NET client application written in C#
  * Requires **TeamTalk.NET** project for DLL dependency
* **TeamTalkAndroid** (dependency: **TeamTalkJNI**)
  * TeamTalk 5 Android client application written in Java
  * Requires **TeamTalkJNI** project as library dependency
  * Import in Eclipse using [Android SDK](http://developer.android.com/sdk/index.html)
  * Copy the following files to *TeamTalkAndroid/libs* directory:
    * android-support-v4.jar
      * Located in {Eclipse ADT install-dir}/sdk/extras/android/support/v4
    * gson-2.2.4.jar
      * Download from http://code.google.com/p/google-gson/
* **ttphpadmin**
  * Console PHP-script for administrating a TeamTalk 5 server.
