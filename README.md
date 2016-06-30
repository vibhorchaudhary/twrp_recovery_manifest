#Setting up a minimal tree for building TWRP
##TWRP branch

###To initialize the main repository:

````
repo init -u https://github.com/vibhu0009/twrp_recovery_manifest.git -b twrp
````
Then add any device trees/kernels you need to a file (one XML for each device) and add them to the .repo/local_manifests folder of your initialized repo folder.

Once added:
````
repo sync
````
Done

To build recovery:
````
. build/envsetup.sh
lunch (devicename)
make installclean
time make recoveryimage showcommands
````
