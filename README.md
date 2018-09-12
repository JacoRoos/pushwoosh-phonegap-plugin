Public Fork
===================================================

This fork removes the reference to the pushwoosh-gcm library which causes duplicate push notifications on Android when used in conjunction with the cordova-firebase-plugin.

NB: In order to preserve the Pushwoosh functionality, the Firebase router should not catch the notifications.
In order to achieve this, install the cordova-custom-config plugin (https://github.com/dpa99c/cordova-custom-config) and add the following lines to the android section of your config.xml:

```
<custom-preference delete="true" name="android-manifest/application/service @android:name='org.apache.cordova.firebase.FirebasePluginMessagingService']" />
<custom-preference delete="true" name="android-manifest/application/service[@android:name='org.apache.cordova.firebase.FirebasePluginInstanceIDService']" />
```

Cordova Pushwoosh Push Notifications plugin
===================================================

[![GitHub release](https://img.shields.io/github/release/Pushwoosh/pushwoosh-phonegap-plugin.svg?style=flat-square)](https://github.com/Pushwoosh/pushwoosh-phonegap-plugin/releases) 
[![npm](https://img.shields.io/npm/v/pushwoosh-cordova-plugin.svg)](https://www.npmjs.com/package/pushwoosh-cordova-plugin)
[![license](https://img.shields.io/npm/l/pushwoosh-cordova-plugin.svg)](https://www.npmjs.com/package/pushwoosh-cordova-plugin)

![platforms](https://img.shields.io/badge/platforms-android%20%7C%20ios%20%7C%20wp8%20%7C%20windows%20-yellowgreen.svg)

Cross-Platform push notifications by Pushwoosh for Cordova / PhoneGap

#### Cordova

Using npm (requires cordova 7.0+):

```
cordova plugin add pushwoosh-cordova-plugin@7.8.7
```

Using git:

```
cordova plugin add https://github.com/Pushwoosh/pushwoosh-phonegap-plugin.git#7.8.7
```

#### Phonegap

Using npm (requires phonegap 7.1+):

```
cordova plugin add pushwoosh-pgb-plugin@7.1.1
```

### Guide

http://docs.pushwoosh.com/docs/cordova-phonegap

### Documentation

http://docs.pushwoosh.com/docs/cordova-api-reference

### Acknowledgments
Plugman support by Platogo

HUGE thanks to Eddy Verbruggen for all the help with WP8 Phonegap support!!!
https://github.com/EddyVerbruggen
