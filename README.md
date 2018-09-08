# android-cordova-assign
Script for assign apk and generate keystore file

## Instructions

 - Put the keystore.sh file in the project root

#### REQUIREMENTS

- Have the `ANDROID_HOME` environment variable pointing to the Android SDK folder
- Have added the android platform to the project:
    ```sh
    $ ionic cordova platform add android
    ```

#### EXECUTION
- To generate the .keystore:
    ```sh
    $ sh keystore.sh generate
    ```
- To generate the signed app:
    ```sh
    $ sh keystore.sh assign
    ```

##### NOTE:

- The signature .keystore file will be created in the root of the project with the name that you put in the variable `APK_ID`
- The `PATH_FILE` constant tells you where the APK is generating the unsigned Android release APK
