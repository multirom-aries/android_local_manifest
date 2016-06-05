Local manifests to build AOSP for Xiaomi Mi2.

How to build:
-------------

Initialize repo:

    repo init -u git://codeaurora.org/quic/la/platform/manifest -b release -m 	LA.BF.1.1.3-01610-8x74.0.xml
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/mitwo-dev/android_local_manifest/android-6.0.1/local_manifest.xml
    repo sync

Compile:

    . build/envsetup.sh
    lunch aries-userdebug
    make -jX otapackage
