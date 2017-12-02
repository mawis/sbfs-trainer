Trainer German Sportbootführerschein See
========================================

This Android app is for the preparation to driving licences for German pleasure
crafts on water ways. Essentially these are six copies of the same source code,
that is able to train the correct responses to multiple choice questions. The
user gets asked until he is able to correctly answer the question five
consecutive times.

This is the source code of the Android application. You can install the
applications in compiled form directly from the Google Play Store:

https://play.google.com/store/apps/details?id=eu.wimmerinformatik.sbfs

I have published the code on GitHub because some people asked me if they can
play with it. (Yes, you can.)


Build how-to
------------

This app is built using Gradle. To build it you need the following tools
installed:

- Java JDK (tested with version 8)
- Android SDK

Before being able to compile you also will have to generate a key that is used
for signing the Android apps. A self-signed key is absolutely suficient for
signing on Android. The key is mainly used by the device to check if you are
allowed to distribute updates for an application.

How to generate your key is described on
http://developer.android.com/tools/publishing/app-signing.html#signing-manually

(You only have to follow step one of this description. Signing of the
application will be done automatically by Maven.)

After creating the key, you have to tell Gradle the password of the key you
generated. This is done in the file ~/.gradle/gradle.properties by adding
a line of the following form: `TRAINER_SIGNING_PASSWORD=your_password`.

After all these preparations are done you can build the trainer with the
following command:

    ./gradlew build

Afterwards you have the compiled app as the following file:
build/outputs/apk/sbfs-trainer-release.apk

This resulting file can now be distributed.


Matthias Wimmer, 2017-12-01
