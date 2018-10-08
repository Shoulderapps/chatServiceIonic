# chatServiceIonic
chat Service

# set ANDROID_HOME before running ionic cordova
export ANDROID_HOME=/home/bchong/Android/Sdk


export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools



#Now, remove the default generated platform.
ionic cordova platform rm android
ionic cordova platform add android
ionic cordova platform rm ios
ionic cordova platform add ios

#To run on the Android/iOS
ionic cordova run android
ionic cordova run ios

# ionic cordova build ios example
$ ionic cordova build ios
$ ionic cordova build ios --prod --release
$ ionic cordova build ios --device --prod --release -- --developmentTeam="ABCD" --codeSignIdentity="iPhone Developer" --packageType="app-store"

# ionic cordova build android example
$ ionic cordova build android
$ ionic cordova build android --prod --release -- -- --keystore=filename.keystore --alias=myalias
$ ionic cordova build android --prod --release -- -- --minSdkVersion=21
$ ionic cordova build android --prod --release -- -- --versionCode=55
$ ionic cordova build android --prod --release -- -- --gradleArg=-PcdvBuildMultipleApks=true

# on nexus 5x
adb install V:\Webapps\chatServiceIonic\platforms\android\app\build\outputs\apk\debug\app-debug.apk
