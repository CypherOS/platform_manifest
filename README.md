[Android Open Source Cypher Project]
====================================

Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Initiate core trees without any device/kernel/vendor:

    $ repo init -u https://github.com/CypherOS/platform_manifest.git -b n7.0

Sync the repository:

    $ repo sync --force-sync

***

Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    . build/envsetup.sh
    lunch

You can also build for specific devices (eg. hammerhead) like this:

    . build/envsetup.sh
    lunch cypher_hammerhead-userdebug
    mka pizza

Remember to `make clobber && make clean` every now and then!
