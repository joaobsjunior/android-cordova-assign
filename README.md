# android-cordova-assign
Script for assign apk and generate keystore file

## Instructions

 - Put the keystore.sh file in the project root

#### REQUIREMENTS

- Running only in Java SDK 8 (Searching a soluction for Java SDK 10)
- Have the `ANDROID_HOME` environment variable pointing to the Android SDK folder
- Have added the android platform to the project:
    ```sh
    $ ionic cordova platform add android
    ```
- Change the variables in keystore.sh file:
    ```sh
    APK_ID="MyApp" # application name (no spaces or special characters)
    APK_KEYSTORE_PASSWORD="password" # keystore password
    APK_KEYSTORE_NAME="Name" # owner name
    APK_KEYSTORE_ORG_UNIT="CompanyX" # company nickname 
    APK_KEYSTORE_ORG_NAME="Company X" # company name
    APK_KEYSTORE_CITY="city" # city
    APK_KEYSTORE_STATE="state" # state
    APK_KEYSTORE_COUNTRY="country" # country
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

- The .keystore file will be created in the root of the project with the name that you put in the variable `APK_ID`
- The signed APK file is saved in the project root with the name used in the variable `APK_ID`
- The `PATH_FILE` constant tells you where the APK is generating the unsigned Android release APK
