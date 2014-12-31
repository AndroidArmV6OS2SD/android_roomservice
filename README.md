roomservice.xml for p500 OS2SD

to build:

init androidarmv6 repo

directions here: https://github.com/androidarmv6/android

cd to your androidarmv6 directory, then

git clone https://github.com/HardLight/android_roomservice.git .repo/local_manifests/ -b cm-11.0

then

repo sync

. build/envsetup.sh

then

lunch cm_p500-userdebug 

or  for recovery build

lunch cm_p500-eng

then

time mka

or  for recovery.img only

time mka recoveryimage

(mka instead of make -j* will supposedly optimize the number of threads based on your cpu, and then time will display total time when it finishes your build.)

output zip in out/target/product/p500
