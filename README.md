#Setting up a minimal tree for building TWRP
##Android 5.1 branch
This repo is ~2.6GB
###To initialize the main repository:

````
repo init -u https://github.com/finley-/recovery_manifest.git -b android-5.1
````
Then add any recovery/device trees/kernels you need to a file (one XML for each device) and add them to the .repo/local_manifests folder of your initialized repo folder.

Once added:
````
repo sync -c --no-tags -j8
````
Done

To build recovery:
````
. build/envsetup.sh
lunch (devicename)
make installclean
time make recoveryimage showcommands -j8
````


Devices tested:

````
Google Nexus 4 (mako)
Pantech Burst p9070 (presto)
HTC Desire 610 (a3ul)
````
