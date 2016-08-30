roomservice.xml for Optimus One, S, V OS2SD

to build:

initialize cm12 repo:

    repo init -u https://github.com/CyanogenMod/android.git -b cm-12.0

clone android_roomservice into your os2sd repo directory:

    git clone https://github.com/androidarmv6os2sd/android_roomservice.git .repo/local_manifests/ -b cm-12.0

then

    repo sync
    sh vendor/cm/get-prebuilts
    . build/envsetup.sh

then lunch your device

    lunch cm_p500-userdebug
    or
    lunch cm_thunderc-userdebug

or  for recovery build

    lunch cm_p500-eng
    or
    lunch cm_thunderc-userdebug

then

    time mka bacon

or  for recovery.img only

    time mka recoveryimage

(mka instead of make -j* will supposedly optimize the number of threads based on your cpu, and then time will display total time when it finishes your build.)

output zip in
    out/target/product/p500
    or
    out/target/product/thunderc
