[Android Open Source Cypher Project]
====================================

Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Initiate core trees without any device/kernel/vendor:

    $ repo init -u https://github.com/CypherOS/platform_manifest.git -b oreo-release

Sync the repository:

    $ repo sync --force-sync

***

Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    . build/envsetup.sh
    
    brunch
    
    Pick your device by typing it's number followed by enter

You can also build for specific devices (eg. bullhead) like this:

    . build/envsetup.sh

    brunch aoscp_bullhead-userdebug

Remember to `make clobber` every now and then!