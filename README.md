![Aoscp for Devs](http://i.imgur.com/A0jUjxO.png)

Downloading the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing the Repository
-----------------------

Init core trees without any device/kernel/vendor :

    $ repo init -u https://github.com/CypherOS/platform_manifest.git -b macchiato-release

Sync our repository :

    $ repo sync

***

Building AOSCP
==============

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.
To build AOSCP first execute this command:

    . build/envsetup.sh
	
This command will load all of our proprietary makefiles for compiling! After the files are initiated,
Run this command:

    brunch
	
No need to generate your device manually. If we official support your device, or if your device is in our vendor/aoscp.devices list
it will be appear on our brunch menu. Next, all you have to do is pick the number beside your device eg.

    1. aoscp_angler-userdebug (Type "1" and press enter)
	
Now sit back and wait for your compilation to complete successfully!
Remember to `make clobber` every now and then!

***

Creating your thread
==================

You got your build to compile. Congrats! Now it's time to share it with the world! AOSCP threads simple so it's not much work left to do here.
Let's start with your thread name. If you are creating a thread for a device that's officially supported by CypherOS, here's how you need to format it:

    [ROM][OFFICIAL][ANDROID VERSION_TAG]CypherOS "Version"[DEVICE]
	
For example: [ROM][UNOFFICIAL][9.0.0_r3]CypherOS 7.0.0[Angler]
Simple right? Now, if you're creating a thread for a device that's not officially supported by CypherOS, [OFFICIAL] needs to be replaced with [UNOFFICIAL]
to ensure users know what kind of build they're running. This is important, as it prevents alot of questions and concerns about bugs etc. that weren't generated
by our team. 

Now that you've gotten the important part out of the way, copy and paste [THIS](https://raw.githubusercontent.com/CypherOS/vendor_aoscp/oreo-mr1-release/BuildAThread.txt)
into your thread. This is not to be modified! You can only add your own acceptable additions to provide more information to your users.

That's it! Thread complete! Thank you for jumping on board with us!
