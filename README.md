# Daily Expenses - Android project

## Build the app (on a computer)
1. Install Android Studio (free): https://developer.android.com/studio
2. File > Open > choose this DailyExpenses folder. Wait for Gradle sync (needs internet the first time).
   If Android Studio offers to update Gradle/plugin versions, accept.
3. Test: plug in your phone (USB debugging on) or use an emulator, press the green Run button.
4. Change applicationId in app/build.gradle.kts to your own unique id (e.g. com.yourname.dailyexpenses).

## Make the Play Store file
1. Build > Generate Signed App Bundle / APK > Android App Bundle.
2. Create a new keystore, set passwords, and BACK UP the keystore file and passwords (you cannot publish updates without them).
3. Choose "release" and finish. You get app-release.aab.

## Publish on Google Play
1. Create a Google Play Console developer account (one-time registration fee): https://play.google.com/console
2. Create app > upload the .aab to a testing track first, then production.
3. Fill the store listing: name, short and full description, icon 512x512, 2+ phone screenshots, feature graphic 1024x500.
4. Fill the Data safety form: the app collects no data and has no internet permission; everything stays on the phone.
5. Add a privacy policy link (a simple page saying data stays on the device is enough).
6. Submit for review. New personal accounts may have to run a closed test with a number of testers first; Play Console shows the current requirement.

## Update the app later
Replace app/src/main/assets/index.html, raise versionCode by 1 in app/build.gradle.kts, build a new bundle, upload it.
