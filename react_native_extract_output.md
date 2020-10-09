# React Native (Android) - Extracting aab / apk file

### Debug mode:
 - Run following script in the root
    ```sh
    $ react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/
    ```
- Move to /android folder
  ```sh
    $ cd android
    ```
- Decide which output you want

    | Type | command |
    | ------ | ------ |
    | aab | gradlew buildDebug |
    | apk | gradlew assembleDebug |
    
- Finally you can get your output file from following locations

    | Type | Location |
    | ------ | ------ |
    | aab | your_project-> android-> app-> build-> outputs-> bundle-> debug-> app-debug.aab |
    | apk | your_project-> android-> app-> build-> outputs-> apk-> debug-> app-debug.apk |
    
    
### Release mode:
 - Run following script in the root
    ```sh
    $ react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/
    ```
- Move to /android folder
  ```sh
    $ cd android
    ```
- Decide which output you want

    | Type | command |
    | ------ | ------ |
    | aab | gradlew buildRelease |
    | apk | gradlew assembleRelease |
    
- Finally you can get your output file from following locations

    | Type | Location |
    | ------ | ------ |
    | aab | your_project-> android-> app-> build-> outputs-> bundle-> release-> app-release.aab |
    | apk | your_project-> android-> app-> build-> outputs-> apk-> release-> app-release.apk |
