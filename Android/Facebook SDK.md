# Android Facebook SDK Integration

Generate a key hash for your local development environment:

```
keytool -exportcert -alias androiddebugkey -keystore ~/.android/debug.keystore | openssl sha1 -binary | openssl base64
```
Go to your [Facebook Developer settings](https://developers.facebook.com/settings/developer/sample-app/) and add the key hash.

```
keytool -exportcert -alias <RELEASE_KEY_ALIAS> -keystore <RELEASE_KEY_PATH> | openssl sha1 -binary | openssl base64
```

Add the cordova plugin
```
meteor add cordova:cordova-plugin-facebook4@1.7.1
```

In the file mobile-config.js add
```
App.configurePlugin('cordova-plugin-facebook4', {
  APP_ID: '#####',
  APP_NAME: '####'
});
```
Ensure do you have in the android sdk manager the `Android Support Library` and `Google Reposository`.

Use the package 
```
meteor add jsep:facebook-native-login
```
